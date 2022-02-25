---
title: OpossumeRight
layout: post
permalink: /legit/
background: '#0a5'

slides:
   
 - title: Choose a theme!
   slide-data: Choose a theme using one of these in the Front Matter. <strong>black, white, league, sky, beige, simple, serif, blood(default), night, moon, solarized</strong>.<pre><code>
       
                -&nbsp;title:&nbsp;Some title
            
                &nbsp;&nbsp;slide-data:&nbsp;some data
                 
                &nbsp;&nbsp;theme:&nbsp;white
                 </code></pre>
   
 
 - title: Add background color!
   slide-data: Use <strong>background:</strong> attribute on a slide to change its backround color.<pre><code>
       
                -&nbsp;title:&nbsp;Some title
            
                &nbsp;&nbsp;slide-data:&nbsp;some data
                 
                &nbsp;&nbsp;background:&nbsp;'#0a5'
                 </code></pre>
   background: '#3498db'
   
 - title: Is Sparrow a Poser?
   slide-data: Mention <strong>image:</strong> attribute with complete path of the image in Front Matter for the particular slide. <pre><code>image:&nbsp;'/images/image-1.jpg'</code></pre>
   image: '/images/punk_show.jpg'

---

{% for slide in page.slides %}                 
<section data-background="{% if slide.image %}{{slide.image}}{% elsif slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}">
        <h1>{{slide.title}}</h1>{{ slide.slide-data }}
</section>               
{% endfor %}
    
