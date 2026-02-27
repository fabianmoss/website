---
# Research Areas Section
widget: blank
active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 25

title: "Research Areas"
subtitle: 'My main areas of research'

design:
  columns: '3'
---

<div class="research-cards">
  <div class="card-container">
    <a href="/research/computational-musicology/" class="card-link">
      <div class="card research-card">
        <div class="card-image computational-musicology"></div>
        <div class="card-body">
          <h3 class="card-title">Computational Musicology</h3>
          <p class="card-text">Exploring music through data and algorithms</p>
        </div>
      </div>
    </a>
  </div>
  
  <div class="card-container">
    <a href="/research/music-theory/" class="card-link">
      <div class="card research-card">
        <div class="card-image music-theory"></div>
        <div class="card-body">
          <h3 class="card-title">Music Theory</h3>
          <p class="card-text">Understanding the structures and systems of music</p>
        </div>
      </div>
    </a>
  </div>
  
  <div class="card-container">
    <a href="/research/cultural-evolution/" class="card-link">
      <div class="card research-card">
        <div class="card-image cultural-evolution"></div>
        <div class="card-body">
          <h3 class="card-title">Cultural Evolution</h3>
          <p class="card-text">Tracing the transmission and transformation of musical traditions</p>
        </div>
      </div>
    </a>
  </div>
  
  <div class="card-container">
    <a href="/research/digital-humanities/" class="card-link">
      <div class="card research-card">
        <div class="card-image digital-humanities"></div>
        <div class="card-body">
          <h3 class="card-title">Digital Humanities</h3>
          <p class="card-text">Applying digital methods to humanities research</p>
        </div>
      </div>
    </a>
  </div>
</div>

<style>
.research-cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  margin-top: 2rem;
}

.card-container {
  perspective: 1000px;
}

.card-link {
  text-decoration: none;
  color: inherit;
}

.research-card {
  background: #fff;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  height: 100%;
}

.research-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 24px rgba(0,0,0,0.15);
}

.card-image {
  height: 180px;
  background-size: cover;
  background-position: center;
}

.card-image.computational-musicology {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.card-image.music-theory {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}

.card-image.cultural-evolution {
  background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
}

.card-image.digital-humanities {
  background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);
}

.card-body {
  padding: 1.5rem;
}

.card-title {
  margin: 0 0 0.5rem 0;
  font-size: 1.25rem;
  font-weight: 600;
}

.card-text {
  margin: 0;
  color: #666;
  font-size: 0.9rem;
}

@media (max-width: 768px) {
  .research-cards {
    grid-template-columns: 1fr;
  }
}
</style>
