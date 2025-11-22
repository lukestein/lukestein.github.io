---
permalink: /
#title: "Luke Stein's homepage"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Accomplished scholar and award-winning teacher at Babson College, with expertise in financial economics. Stanford Ph.D. in Economics; Harvard A.B. in Applied Mathematics and Citation in Japanese Language. Expert witness. Non-profit organization board member.

Research published/accepted in top peer-reviewed journals including _Journal of Financial Economics_, _Review of Financial Studies_, _Journal of Corporate Finance_, _Financial Review_, and _Economic Journal_.

2022 recipient of Babson Deans’ Award for Excellence in Graduate Teaching (annual award to one faculty member for “excellence and innovative practices in teaching”) and Thomas Kennedy Award for Teaching Excellence (“Graduate Faculty of the Year” awarded annually by graduating class to one faculty member “who personifies teaching excellence at the graduate level and whose personal standards of quality and caring extend beyond the classroom”).

Former finance faculty at Arizona State University’s W. P. Carey School of Business (winner of 2019 Huizingh Outstanding Undergraduate Teacher Award, given to an instructor “dedicated to inspiring students through excellence in teaching and mentoring”) and economics instructor at Stanford University (winner of 2012 Gores Award, “the University's highest award for excellence in teaching”). In an earlier life: strategy consultant for Bain & Company in New York and Tokyo.


## Research

([Full list with abstracts](/publications) or [pdf cv](/files/steincv.pdf))

{% include base_path %}

{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      
      {% unless title_shown %}
### {{ category[1].title }}
<ol>
        {% assign title_shown = true %}
      {% endunless %}
      
      {% include archive-single-compact.html %}
    
    {% endfor %}
    
    {% if title_shown %}
</ol>
    {% endif %}
    
  {% endfor %}

{% else %}

<ol>
    {% for post in site.publications reversed %}
      {% include archive-single-compact.html %}
    {% endfor %}
</ol>

{% endif %}

---

Luke Stein     
Finance Division, Babson College  
320 Tomasso Hall  
231 Forest Street  
Babson Park, MA 02457

[lcdstein@babson.edu](mailto:lcdstein@babson.edu)