---
title: 'Components - Fonts'
meta:
  robots: 'noindex, nofollow'
  description: 'Discover the fonts that are available for use.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Fonts'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Fonts'
sort_order: 2
---
{% set fonts = {
  'Proxima Nova': {
    'family' : "'proxima-nova', sans-serif",
    'weights' : ['400', '600', '700','800'],
    'italics' : ['400', '600', '700']
  },
  'Serifa': {
    'family' : "'serifa', serif",
    'weights' : ['400','500','700']
  },
} %}
<ul>
  {% for name, style in fonts %}
    {% for weight in style.weights %}
      <li style="font-family: {{ style.family }}; font-weight: {{ weight }}">
        {{ style.family }} - {{ weight}} - The quick brown fox jumps over the lazy dog
      </li>
      {% if weight in style.italics %}
        <li style="font-family: {{ style.family }}; font-weight: {{ weight }}; font-style: italic">
          {{ style.family }} - {{ weight }} - italic - The quick brown fox jumps over the lazy dog
        </li>
      {% endif %}
    {% endfor %}
  {% endfor %}
</ul>