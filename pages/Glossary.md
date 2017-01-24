---
title: Glossary
layout: tutorial
keywords:
permalink: /Glossary.html
---

See also:

- [Full API Connect glossary](http://www.ibm.com/support/knowledgecenter/SSMNED_5.0.0/com.ibm.apic.overview.doc/overview_apimgmt_glossary.html)
- [LoopBack glossary](http://loopback.io/doc/en/lb2/Glossary.html)

{% assign gloss = site.data.glossary %}

<dl>
{% for item in gloss %}
  {% capture id %}{{item[0]}}{% endcapture %}
  {% assign gloss_item = gloss[{{id}}] %}
  <dt>{{gloss_item.term }}</dt>
  <dd>{{gloss_item.definition }}</dd>
{% endfor %}
</dl>
