---
layout: post
title:  "A Simple Post"
date:   2022-04-05 07:50:38 -0600
categories: jekyll update
---
 {% comment %} The next few paragraphs illustrate some  {% endcomment %}
{% capture my_table %}
| foo | bar |
| :---: | ---: |
| baz | bim |
| {: .ipa } doesn't gentium this   |   |
| centred   | right-j  |
| <span>gentium stuff</span>{: .ipa }  | etc  |
{% endcapture %}
{% assign my_string = 'ɩ́nɩ' %}
{% assign my_string =  " bɔ́fʋn" | prepend: my_string %}
<span>{{ my_string }}</span>{: .ipa }
My favorite food is {{ my_string }}.

This is a simple post to illustrate a bit of ~~Jekyll~~{: .ipa }.

The next two lines should be in different fonts
1. This bullet point is in the default minima font. The next point should be in Google <span>Gentium</span>{: .ipa } Basic *web*{: .ipa } font
2. {: .ipa } Nɔ́pʋ Gugɛl Gyɛntiam Besɩk wɛbfɔnt wanlɩn ɩ́nɩ.
3. third <span>point</span>{: .ipa }

{{ my_table }}

```
{{ my_table }}
```
{% capture my_checkbox_test %}
- {: .ipa }[x] Before the checkbox applies to entire line -- puts the class attribute on the li element
- [x] {: .ipa }ipa on the checkbox doesn't gentium because the ipa class is applied to only the checkbox
- [x] The liquid attribute is just concatenated into the code
- [ ] <span>Does gentium because it uses span marker</span>{: .ipa }
- [ ]  explicit span marker <span>always</span>{: .ipa } works

{% endcapture %}

{{ my_checkbox_test }}

Original Code:
```
{{ my_checkbox_test }}
```

The generated HTML:
```
<ul class="task-list">
  <li class="task-list-item ipa"><input type="checkbox" class="task-list-item-checkbox" disabled="disabled" checked="checked" />Before the checkbox applies to entire line – puts the class attribute on the li element</li>
  <li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox ipa" disabled="disabled" checked="checked" />ipa on the checkbox doesn’t gentium because the ipa class is applied to only the checkbox</li>
  <li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled="disabled" checked="checked" />The liquid attribute is just concatenated into the code</li>
  <li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled="disabled" /><span class="ipa">Does gentium because it uses span marker</span></li>
  <li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled="disabled" />explicit span marker <span class="ipa">always</span> works</li>
</ul>
```

That's all for this post.
