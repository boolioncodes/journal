---
foo:
 - bar: foobar
 - baz: foobaz
fu:
  bar: fubar
  baz: fubaz
fee:
 - fie
 - fo
eeny:
 meeny:
  miney:
   - mo
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.9.0/styles/default.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.9.0/highlight.min.js"></script>

<!-- and it's easy to individually load additional languages -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.9.0/languages/json.min.js"></script>

<script>hljs.highlightAll();</script>

# Inspecting Jekyll variables

## `site`

<pre><code class="language-json">
{{ site | inspect }}
</code></pre>

## `page`

<pre><code class="language-json">
{{ page | jsonify }}
</code></pre>

## foo

<pre><code class="language-json">
{{ page.foo | inspect }}
</code></pre>
`page.foo | size` : {{ page.foo | size }}   
`page.foo.first` : {{ page.foo.first }}  
`page.foo.first | size` : {{ page.foo.first | size }}   
`page.foo.first.first` : {{ page.foo.first.first }}  
`page.foo.first.bar | size` : {{ page.foo.first.bar | size }}   
`page.foo.first.bar.first` : {{ page.foo.first.bar.first }}  
`page.foo.first.bar.first | size` : {{ page.foo.first.bar.first | size }}   
`page.foo.first.bar.first.first` : {{ page.foo.first.bar.first.first }}  
```xml
{% include serialize.xml var=page.foo %}
```

## fu
<pre><code class="language-json">
{{ page.fu | inspect }}
</code></pre>
`page.fu | size` : {{ page.fu | size }}  
`page.fu.first` : {{ page.fu.first }}  
`page.fu.first | size` : {{ page.fu.first | size }}   
`page.fu.first.first` : {{ page.fu.first.first }}  
`page.fu.bar | size` : {{ page.fu.bar | size }}  
`page.fu.bar.first` : {{ page.fu.bar.first }}  
`page.fu.bar.first | size` : {{ page.fu.bar.first | size }}   
`page.fu.bar.first.first` : {{ page.fu.bar.first.first }}  
```xml
{% include serialize.xml var=page.fu %}
```

## fee
<pre><code class="language-json">
{{ page.fee | inspect }}
</code></pre>
`page.fee | size` : {{ page.fee | size }}  
`page.fee.first` : {{ page.fee.first }}  
`page.fee.first | size` : {{ page.fee.first | size }}   
`page.fee.first.first` : {{ page.fee.first.first }}  
```xml
{% include serialize.xml var=page.fee %}
```


## eeny
<pre><code class="language-json">
{{ page.eeny | inspect }}
</code></pre>
`page.eeny | size` : {{ page.eeny | size }}  
`page.eeny.first` : {{ page.eeny.first }}  
`page.eeny.first | size` : {{ page.eeny.first | size }}   
`page.eeny.first.first` : {{ page.eeny.first.first }}  
`page.eeny.meeny | size` : {{ page.eeny.meeny | size }}  
`page.eeny.meeny.first` : {{ page.eeny.meeny.first }}  
`page.eeny.meeny.first | size` : {{ page.eeny.meeny.first | size }}   
`page.eeny.meeny.first.first` : {{ page.eeny.meeny.first.first }}  
`page.eeny.meeny.miney | size` : {{ page.eeny.meeny.miney | size }}  
`page.eeny.meeny.miney.first` : {{ page.eeny.meeny.miney.first }}  
`page.eeny.meeny.miney.first | size` : {{ page.eeny.meeny.miney.first | size }}   
`page.eeny.meeny.miney.first.first` : {{ page.eeny.meeny.miney.first.first }}  
```xml
{% include serialize.xml var=page.eeny %}
```
