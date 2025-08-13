---
layout: default
title: All Reports
permalink: /reports/
---

# Research Reports

Browse our complete collection of game market research reports. Each report follows our systematic 8-step research pipeline with comprehensive data validation and source documentation.

<div class="report-filters">
  <div class="filter-group">
    <label for="genre-filter">Filter by Genre:</label>
    <select id="genre-filter" onchange="filterReports()">
      <option value="all">All Genres</option>
      <option value="match-3">Match-3</option>
      <option value="hybrid-casual">Hybrid-Casual</option>
      <option value="puzzle">Puzzle</option>
      <option value="strategy">Strategy</option>
    </select>
  </div>
</div>

<div class="reports-list" id="reports-container">
  {% assign sorted_reports = site.reports | sort: 'date' | reverse %}
  {% for report in sorted_reports %}
    <article class="report-item" data-genre="{{ report.genre | downcase }}">
      <header class="report-item-header">
        <h2><a href="{{ report.url | relative_url }}">{{ report.title }}</a></h2>
        <div class="report-item-meta">
          <span class="genre-tag">{{ report.genre | default: "General" }}</span>
          <span class="date-tag">{{ report.date | date: "%B %Y" }}</span>
          {% if report.market_size %}
            <span class="market-size-tag">${{ report.market_size }}</span>
          {% endif %}
        </div>
      </header>
      
      <div class="report-item-content">
        {% if report.summary %}
          <p class="summary">{{ report.summary }}</p>
        {% else %}
          <p class="excerpt">{{ report.excerpt | strip_html | truncate: 200 }}</p>
        {% endif %}
        
        {% if report.key_findings %}
          <div class="quick-findings">
            <strong>Key Findings:</strong>
            <ul>
              {% for finding in report.key_findings limit: 3 %}
                <li>{{ finding | truncate: 80 }}</li>
              {% endfor %}
            </ul>
          </div>
        {% endif %}
      </div>
      
      <footer class="report-item-footer">
        <a href="{{ report.url | relative_url }}" class="read-report-btn">Read Full Report</a>
        {% if report.methodology %}
          <span class="methodology-tag">{{ report.methodology }}</span>
        {% endif %}
      </footer>
    </article>
  {% endfor %}
</div>

<script>
function filterReports() {
  const filter = document.getElementById('genre-filter').value;
  const reports = document.querySelectorAll('.report-item');
  
  reports.forEach(report => {
    const genre = report.getAttribute('data-genre');
    if (filter === 'all' || genre === filter || genre.includes(filter)) {
      report.style.display = 'block';
    } else {
      report.style.display = 'none';
    }
  });
}
</script>

<style>
.report-filters {
  margin-bottom: 2rem;
  padding: 1rem;
  background: var(--surface-color);
  border-radius: 8px;
}

.filter-group {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.filter-group select {
  padding: 0.5rem 1rem;
  border: 1px solid var(--border-color);
  border-radius: 6px;
  font-family: inherit;
}

.reports-list {
  display: grid;
  gap: 2rem;
}

.report-item {
  background: var(--background-color);
  border: 1px solid var(--border-color);
  border-radius: 8px;
  padding: 2rem;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.report-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
}

.report-item-header h2 {
  margin-bottom: 1rem;
}

.report-item-header h2 a {
  color: var(--primary-color);
  text-decoration: none;
}

.report-item-header h2 a:hover {
  text-decoration: underline;
}

.report-item-meta {
  display: flex;
  flex-wrap: wrap;
  gap: 0.75rem;
  margin-bottom: 1.5rem;
}

.genre-tag, .date-tag, .market-size-tag, .methodology-tag {
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  font-size: 0.85rem;
  font-weight: 500;
}

.genre-tag {
  background: var(--primary-color);
  color: white;
}

.date-tag {
  background: var(--surface-color);
  color: var(--text-muted);
}

.market-size-tag {
  background: var(--success-color);
  color: white;
}

.methodology-tag {
  background: var(--accent-color);
  color: white;
}

.report-item-content .summary,
.report-item-content .excerpt {
  margin-bottom: 1rem;
  color: var(--text-muted);
  line-height: 1.6;
}

.quick-findings {
  background: var(--surface-color);
  padding: 1rem;
  border-radius: 6px;
  margin-bottom: 1rem;
}

.quick-findings ul {
  margin: 0.5rem 0 0 0;
  padding-left: 1rem;
}

.quick-findings li {
  margin-bottom: 0.25rem;
  font-size: 0.9rem;
}

.report-item-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-top: 1px solid var(--border-color);
  padding-top: 1rem;
}

.read-report-btn {
  padding: 0.75rem 1.5rem;
  background: var(--primary-color);
  color: white;
  text-decoration: none;
  border-radius: 6px;
  font-weight: 500;
  transition: background-color 0.2s ease;
}

.read-report-btn:hover {
  background: #1d4ed8;
}

@media (max-width: 768px) {
  .report-item-footer {
    flex-direction: column;
    gap: 1rem;
    align-items: flex-start;
  }
}
</style>