---
layout: page
permalink: /people/
title: Team
nav: true
nav_order: 7
sitemap: false

# Add confirmed current members below; category, affiliation, and year control
# the roster grouping. A url is optional for a LinkedIn profile or personal site.
# current_members:
#   - name: Full Name
#     category: PhD Students
#     affiliation: University of Oxford
#     year: "2026–now"
#     url: https://example.com
# alumni:
#   - name: Full Name
#     work: MSc project on a research topic (2024)
# Add an optional url to any person below for a LinkedIn profile or personal site.
current_members:
  - name: Bohang Sun
    category: PhD Students
    affiliation: University of Cambridge
    year: "2026–now"
    url: https://www.linkedin.com/in/bob-sun-b35108344/
# Add confirmed mentees here using the same category, affiliation, year, and
# optional url fields as current_members. For PhD mentees, use PhD Students.
mentees:
  - name: Angira Sharma
    category: PhD Students
    affiliation: University of Oxford
    year: "2025–2026"
    url: https://www.linkedin.com/in/angira-sharma/
alumni: []
msc_students:
  - institution: University of Oxford
    cohorts:
      - year: "2025–2026"
        students:
          - name: Cheng Ma
            url: https://www.linkedin.com/in/cheng-ma-508b93295/
          - name: Liheng Chen
            url: https://www.linkedin.com/in/simonlhchen/
          - name: Fabian Degen
            url: https://www.linkedin.com/in/fabiandegen/
          - name: Hongxin Zhen
      - year: "2024–2025"
        students:
          - name: Thierry Blankenstein
            url: https://www.linkedin.com/in/thierry-blankenstein/
          - name: Jonathan Sneh
            url: https://www.linkedin.com/in/jonathan-sneh/
          - name: Louis Roche
            url: https://www.linkedin.com/in/louisrch/
          - name: Toomas Roosma
            url: https://www.linkedin.com/in/toomas-roosma/
  - institution: University College London
    cohorts:
      - year: "2023–2024"
        students:
          - name: Honggeon Yoon
            url: https://www.linkedin.com/in/hg-dbs/
          - name: Boris Marinov
            url: https://www.linkedin.com/in/boris-marinov-54947614a/
      - year: "2022–2023"
        students:
          - name: Jingyun Su
          - name: Nanda Smith
research_assistants:
  - institution: University of Oxford
    cohorts:
      - year: "2025–2026"
        students:
          - name: Yupeng Chen
            url: https://www.linkedin.com/in/yupeng-chen-107b732b1/
undergraduate_students:
  - institution: University of Oxford
    cohorts:
      - year: "2025–2026"
        students:
          - name: Zeyuan He
            url: https://www.linkedin.com/in/zeyuan-he-741026378/
---

<style>
.team-section {
  width: 100%;
  margin: 2rem 0;
}

.team-section h2 {
  border-bottom: 2px solid var(--global-divider-color);
  padding-bottom: 0.5rem;
  margin-bottom: 2rem;
}

.profile-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 1.5rem;
  justify-content: flex-start;
  max-width: 1000px;
  margin: 0 auto;
}

.profile-card {
  width: 250px;
  text-align: center;
}

.profile-card h3 {
  margin: 10px 0 5px;
}

.profile-card p {
  margin: 5px 0;
  font-size: 0.9em;
}

.team-empty {
  color: var(--global-text-color-light);
}

.team-roster {
  font-size: 0.8125rem;
  line-height: 1.45;
}

.team-roster h3 {
  font-size: 1rem;
  margin-bottom: 0.85rem;
}

.team-roster + .team-roster {
  margin-top: 1.5rem;
}

.team-institution + .team-institution {
  margin-top: 1.25rem;
}

.team-institution h4 {
  font-size: 0.9rem;
  margin-bottom: 0.5rem;
}

.team-cohorts {
  margin: 0;
}

.team-cohort {
  display: grid;
  grid-template-columns: 6.5rem minmax(0, 1fr);
  column-gap: 0.75rem;
  margin-bottom: 0.35rem;
}

.team-cohort dt {
  color: var(--global-theme-color);
  font-weight: 600;
  white-space: nowrap;
}

.team-cohort dd {
  margin: 0;
}

.team-cohort a {
  text-decoration: underline;
  text-underline-offset: 0.15em;
}

@media (max-width: 575px) {
  .team-roster {
    font-size: 0.875rem;
  }

  .team-cohort {
    grid-template-columns: 1fr;
    row-gap: 0.1rem;
  }
}
</style>

<section class="team-section" aria-labelledby="current-members-heading">
  <h2 id="current-members-heading">Current Members</h2>
  {% if page.current_members.size > 0 %}
    {% assign member_groups = page.current_members | group_by: 'category' %}
    {% for member_group in member_groups %}
      <div class="team-roster">
        <h3>{{ member_group.name | escape }}</h3>
        {% assign institutions = member_group.items | group_by: 'affiliation' %}
        {% for institution in institutions %}
          <div class="team-institution">
            <h4>{{ institution.name | escape }}</h4>
            <dl class="team-cohorts">
              {% assign cohorts = institution.items | group_by: 'year' %}
              {% for cohort in cohorts %}
                <div class="team-cohort">
                  <dt>{{ cohort.name | escape }}</dt>
                  <dd>{% for person in cohort.items %}{% assign person_url = person.url | default: person.website %}{% if person_url %}<a href="{{ person_url | escape }}">{{ person.name | escape }}</a>{% else %}{{ person.name | escape }}{% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}.</dd>
                </div>
              {% endfor %}
            </dl>
          </div>
        {% endfor %}
      </div>
    {% endfor %}
  {% else %}
    <p class="team-empty">Current members will be added here.</p>
  {% endif %}
</section>

<section class="team-section" aria-labelledby="mentees-heading">
  <h2 id="mentees-heading">Mentees</h2>
  {% if page.mentees.size > 0 %}
    {% assign mentee_groups = page.mentees | group_by: 'category' %}
    {% for mentee_group in mentee_groups %}
      <div class="team-roster">
        <h3>{{ mentee_group.name | escape }}</h3>
        {% assign institutions = mentee_group.items | group_by: 'affiliation' %}
        {% for institution in institutions %}
          <div class="team-institution">
            <h4>{{ institution.name | escape }}</h4>
            <dl class="team-cohorts">
              {% assign cohorts = institution.items | group_by: 'year' %}
              {% for cohort in cohorts %}
                <div class="team-cohort">
                  <dt>{{ cohort.name | escape }}</dt>
                  <dd>{% for person in cohort.items %}{% assign person_url = person.url | default: person.website %}{% if person_url %}<a href="{{ person_url | escape }}">{{ person.name | escape }}</a>{% else %}{{ person.name | escape }}{% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}.</dd>
                </div>
              {% endfor %}
            </dl>
          </div>
        {% endfor %}
      </div>
    {% endfor %}
  {% else %}
    <div class="team-roster">
      <h3>PhD Students</h3>
      <p class="team-empty">Mentee names will be added here.</p>
    </div>
  {% endif %}
</section>

<section class="team-section" aria-labelledby="alumni-heading">
  <h2 id="alumni-heading">Alumni</h2>
  {% if page.alumni.size > 0 %}
  <div class="profile-grid">
    {% for person in page.alumni %}
      {% assign person_url = person.url | default: person.website %}
      <div class="profile-card">
        <h3>{% if person_url %}<a href="{{ person_url | escape }}">{{ person.name | escape }}</a>{% else %}{{ person.name | escape }}{% endif %}</h3>
        {% if person.work %}<p>{{ person.work | escape }}</p>{% endif %}
      </div>
    {% endfor %}
  </div>
  {% endif %}

  {% if page.research_assistants.size > 0 %}
  <div class="team-roster">
    <h3>Research Assistants</h3>
    {% for group in page.research_assistants %}
      <div class="team-institution">
        <h4>{{ group.institution | escape }}</h4>
        <dl class="team-cohorts">
          {% for cohort in group.cohorts %}
            <div class="team-cohort">
              <dt>{{ cohort.year | escape }}</dt>
              <dd>{% for student in cohort.students %}{% if student.url %}<a href="{{ student.url | escape }}">{{ student.name | escape }}</a>{% else %}{{ student.name | escape }}{% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}.</dd>
            </div>
          {% endfor %}
        </dl>
      </div>
    {% endfor %}
  </div>
  {% endif %}

  {% if page.msc_students.size > 0 %}
  <div class="team-roster">
    <h3>MSc Students</h3>
    {% for group in page.msc_students %}
      <div class="team-institution">
        <h4>{{ group.institution | escape }}</h4>
        <dl class="team-cohorts">
          {% for cohort in group.cohorts %}
            <div class="team-cohort">
              <dt>{{ cohort.year | escape }}</dt>
              <dd>{% for student in cohort.students %}{% if student.url %}<a href="{{ student.url | escape }}">{{ student.name | escape }}</a>{% else %}{{ student.name | escape }}{% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}.</dd>
            </div>
          {% endfor %}
        </dl>
      </div>
    {% endfor %}
  </div>
  {% endif %}

  {% if page.undergraduate_students.size > 0 %}
  <div class="team-roster">
    <h3>Undergraduate Students</h3>
    {% for group in page.undergraduate_students %}
      <div class="team-institution">
        <h4>{{ group.institution | escape }}</h4>
        <dl class="team-cohorts">
          {% for cohort in group.cohorts %}
            <div class="team-cohort">
              <dt>{{ cohort.year | escape }}</dt>
              <dd>{% for student in cohort.students %}{% if student.url %}<a href="{{ student.url | escape }}">{{ student.name | escape }}</a>{% else %}{{ student.name | escape }}{% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}.</dd>
            </div>
          {% endfor %}
        </dl>
      </div>
    {% endfor %}
  </div>
  {% endif %}
</section>
