---
# A blank widget that renders the latest publications via a custom shortcode.
widget: blank
active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 3

title: Publications
subtitle: 'Journal Articles, Conference Papers, Datasets'

design:
  # Full-width list so it aligns with the other homepage sections.
  columns: '1'
---

{{< publications_list >}}

<p class="see-all"><a href="./publication/">View all publications &rarr;</a></p>
