---
foo:
 - bar: foobar
 - baz: foobaz
fu:
  bar: fubar
  baz: fubaz
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

## fu
<pre><code class="language-json">
{{ page.fu | inspect }}
</code></pre>
`page.fu | size` : {{ page.fu | size }}  
`page.fu.first` : {{ page.fu.first }}  
`page.fu.first | size` : {{ page.fu.first | size }}   
`page.fu.first.first` : {{ page.fu.first.first }}  


