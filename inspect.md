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
types:
  arr:
   - 0
   - 1
   - true
   - false
   - string
  obj:
   zero: 0
   one: 1
   boolt: true
   boolf: false
   str: string
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.9.0/styles/default.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.9.0/highlight.min.js"></script>

<!-- and it's easy to individually load additional languages -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.9.0/languages/json.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.9.0/languages/xml.min.js"></script>

<script>hljs.highlightAll();</script>

# Inspecting Jekyll variables

## `site`

<pre><code class="language-json">
{{ site | inspect }}
</code></pre>

<table>
 <tr>
  <th>node</th>
  <th>size</th>
  <th>first</th>
  <th>[0]</th>
  <th>first.size</th>
  <th>first.first</th>
  <th>first[0]</th>
 </tr>
{% include debug-var.html var=site.pages %}
</table>

{% raw %}
``````xml
{% include serialize.xml var=site %}
``````
{% endraw %}

## `page`

<pre><code class="language-json">
{{ page | jsonify }}
</code></pre>

<!-- {% raw %}
<pre><code class="language-xml">
{% include serialize.xml var=page %}
</code></pre>
{% endraw %}-->
``````xml
{% include serialize.xml var=page %}
``````


## foo

<pre><code class="language-json">
{{ page.foo | inspect }}
</code></pre>

<table>
 <tr>
  <th>node</th>
  <th>size</th>
  <th>first</th>
  <th>[0]</th>
  <th>first.size</th>
  <th>first.first</th>
  <th>first[0]</th>
 </tr>
{% include debug-var.html var=page.foo %}
</table>

``````xml
{% include serialize.xml var=page.foo %}
``````

## fu
<pre><code class="language-json">
{{ page.fu | inspect }}
</code></pre>

<table>
 <tr>
  <th>node</th>
  <th>size</th>
  <th>first</th>
  <th>[0]</th>
  <th>first.size</th>
  <th>first.first</th>
  <th>first[0]</th>
 </tr>
{% include debug-var.html var=page.fu %}
</table>

``````xml
{% include serialize.xml var=page.fu %}
``````

## fee
<pre><code class="language-json">
{{ page.fee | inspect }}
</code></pre>

<table>
 <tr>
  <th>node</th>
  <th>size</th>
  <th>first</th>
  <th>[0]</th>
  <th>first.size</th>
  <th>first.first</th>
  <th>first[0]</th>
 </tr>
{% include debug-var.html var=page.fee %}
</table>

``````xml
{% include serialize.xml var=page.fee %}
``````


## eeny
<pre><code class="language-json">
{{ page.eeny | inspect }}
</code></pre>

<table>
 <tr>
  <th>node</th>
  <th>size</th>
  <th>first</th>
  <th>[0]</th>
  <th>first.size</th>
  <th>first.first</th>
  <th>first[0]</th>
 </tr>
{% include debug-var.html var=page.eeny %}
</table>

``````xml
{% include serialize.xml var=page.eeny %}
``````

## types
<pre><code class="language-json">
{{ page.types | inspect }}
</code></pre>

<table>
 <tr>
  <th>node</th>
  <th>size</th>
  <th>first</th>
  <th>[0]</th>
  <th>first.size</th>
  <th>first.first</th>
  <th>first[0]</th>
 </tr>
{% include debug-var.html var=page.types %}
</table>

``````xml
{% include serialize.xml var=page.types %}
``````
