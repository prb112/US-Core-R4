<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* US-Core-R4/input/includes/example-list-generator.md                                   *
*****************************************************************************************
{% endcomment %} -->
<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* US-Core-R4/input/includes/example-list-generator.md                                   *
*****************************************************************************************
{% endcomment %} -->
<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* US-Core-R4/input/includes/example-list-generator.md                                   *
*****************************************************************************************
{% endcomment %} -->
<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* Davinci-CDEX/input/includes/example-list-generator.md                                 *
*****************************************************************************************
{% endcomment %} -->
<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* Davinci-CDEX/input/includes/example-list-generator.md                                 *
*****************************************************************************************
{% endcomment %} -->
<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* Davinci-CDEX/input/includes/example-list-generator.md                                 *
*****************************************************************************************
{% endcomment %} -->
<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* Davinci-CDEX/input/includes/example-list-generator.md                                 *
*****************************************************************************************
{% endcomment %} -->
<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* Davinci-CDEX/input/includes/example-list-generator.md                                 *
*****************************************************************************************
{% endcomment %} -->
<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* Davinci-CDEX/input/includes/example-list-generator.md                                 *
*****************************************************************************************
{% endcomment %} -->
<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* Davinci-CDEX/input/includes/example-list-generator.md                                 *
*****************************************************************************************
{% endcomment %} -->
<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* Davinci-CDEX/input/includes/example-list-generator.md                                 *
*****************************************************************************************
{% endcomment %} -->
<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* Davinci-CDEX/input/includes/example-list-generator.md                                 *
*****************************************************************************************
{% endcomment %} -->
<!-- example-list-generator.md {% comment %}
*****************************************************************************************
*                            WARNING: DO NOT EDIT THIS FILE                             *
*                                                                                       *
* This file is generated by SUSHI. Any edits you make to this file will be overwritten. *
*                                                                                       *
* To change the contents of this file, edit the original source file at:                *
* Davinci-CDEX/input/includes/example-list-generator.md                                 *
*****************************************************************************************
{% endcomment %} -->

{% for p in site.data.ig.definition.resource %}
  {%- if p.exampleBoolean or p.exampleCanonical -%}
      {% if types %}
        {% assign types =  types | append: "," | append: p.reference.reference | split: '/' | first %}
      {% else %}
       {% assign types = p.reference.reference | split: '/' | first %}
      {% endif %}
  {% endif %}
{% endfor %}

{% assign my_array = types | split: "," %}
{% assign my_array = my_array | sort | uniq %}

{% for i in my_array %}
### {{ i }}
  {%- for p in site.data.ig.definition.resource -%}
      {%- if p.exampleBoolean or p.exampleCanonical -%}
        {%- assign type =  p.reference.reference | split: '/' | first -%}
            {%- if type == i %}
- [{{p.name}}]({{p.reference.reference | replace: '/','-'}}.html)
            {%- endif -%}
       {%- endif -%}
   {%- endfor %}
{% comment %} keep this line here for proper rendering {% endcomment %}
{% endfor %}