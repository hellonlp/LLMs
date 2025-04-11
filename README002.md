### DATABASE SCHEMA ### 
{% for document in documents %}
    {{ document }}
{% endfor %}

{% if instructions %}
### INSTRUCTIONS ###
{{ instructions }}
{% endif %}

{% if sql_functions %}
### SQL FUNCTIONS ###
{% for function in sql_functions %}
{{ function }}
{% endfor %}
{% endif %}

{% if sql_samples %}
### SQL SAMPLES ###
{% for sample in sql_samples %}
Question:
{{sample.question}}
SQL:
{{sample.sql}}
{% endfor %}
{% endif %}

### QUESTION ###
User's Question: {{ query }}
Current Time: {{ current_time }}

{% if sql_generation_reasoning %}
### REASONING PLAN ###
{{ sql_generation_reasoning }}
{% endif %}

Let's think step by step.
