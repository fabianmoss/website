---
# Research Areas Section
widget: blank
active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 2 

title: "Research areas"
subtitle: '(under construction)'

design:
  columns: '1'
---

<div class="research-cards">
  <div class="card-container">
    <a href="/research/computational-musicology/" class="card-link">
      <div class="card research-card">
        <div class="card-image computational-musicology">
          <h3 class="card-title">Computational Musicology</h3>
        </div>
        <div class="card-body">
          <p class="card-text">Modeling musical patterns in large corpora</p>
        </div>
      </div>
    </a>
  </div>
  
   <div class="card-container">
    <a href="/research/music-theory/" class="card-link">
      <div class="card research-card">
        <div class="card-image music-theory">
          <h3 class="card-title">Music Theory & Analysis</h3>
        </div>
        <div class="card-body">
          <p class="card-text">How algorithms reveal musical structure</p>
        </div>
      </div>
    </a>
  </div>
  
  <div class="card-container">
    <a href="/research/digital-humanities/" class="card-link">
      <div class="card research-card">
        <div class="card-image digital-humanities">
          <h3 class="card-title">Music Encoding & Digital Humanities</h3>
        </div>
        <div class="card-body">
          <p class="card-text">Building digital editions and research tools</p>
        </div>
      </div>
    </a>
  </div>
  <div class="card-container">
    <a href="/research/cultural-evolution/" class="card-link">
      <div class="card research-card">
        <div class="card-image cultural-evolution">
          <h3 class="card-title">Cultural Evolution & Music</h3>
        </div>
        <div class="card-body">
          <p class="card-text">How musical traditions change and spread</p>
        </div>
      </div>
    </a>
  </div>
</div>

<style>
.research-cards {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.5rem;
}

.card-container {
  perspective: 1000px;
  height: 100%;
}

.card-link {
  display: block;
  height: 100%;
  text-decoration: none;
  color: inherit;
}

.research-card {
  display: flex;
  flex-direction: column;
  height: 100%;
  margin-bottom: 0;
  background: #fff;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.research-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 24px rgba(0,0,0,0.15);
}

.card.research-card .card-image {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100px;
  padding: 0.9rem 1.25rem;
  text-align: center;
  background-size: cover;
  background-position: center;
}

.card-image.computational-musicology {
  background: linear-gradient(135deg, #4f46e5 0%, #7c3aed 100%);
}

.card-image.cultural-evolution {
  background: linear-gradient(135deg, #92400e 0%, #b45309 100%);
}

.card-image.music-theory {
  background: linear-gradient(135deg, #be123c 0%, #db2777 100%);
}

.card-image.digital-humanities {
  background: linear-gradient(135deg, #075985 0%, #0e7490 100%);
}

.card.research-card .card-body {
  flex: 1;
  padding: 1rem 1.25rem;
}

.card.research-card .card-title {
  margin: 0;
  color: #fff;
  font-size: clamp(1.1rem, 1.5vw, 1.35rem);
  font-weight: 600;
  line-height: 1.25;
  text-shadow: 0 1px 4px rgba(0, 0, 0, 0.35);
}

.card.research-card .card-text {
  margin: 0;
  padding: 0;
  color: #4b5563;
  font-size: 1rem;
  line-height: 1.5;
  text-wrap: balance;
}

@media (max-width: 768px) {
  .research-cards {
    grid-template-columns: 1fr;
  }
}
</style>
