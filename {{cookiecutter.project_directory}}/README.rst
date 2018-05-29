{% set is_open_source = cookiecutter.open_source_license != 'Not open source' -%}
{% for _ in cookiecutter.project_name %}={% endfor %}
{{ cookiecutter.project_name }}
{% for _ in cookiecutter.project_name %}={% endfor %}

{% if is_open_source %}
.. image:: https://img.shields.io/pypi/v/{{ cookiecutter.project_directory }}.svg
        :target: https://pypi.python.org/pypi/{{ cookiecutter.project_directory }}

.. image:: https://img.shields.io/travis/{{ cookiecutter.github_username_or_organization }}/{{ cookiecutter.project_directory }}.svg
        :target: https://travis-ci.org/{{ cookiecutter.github_username_or_organization }}/{{ cookiecutter.project_directory }}

.. image:: https://readthedocs.org/projects/{{ cookiecutter.project_directory | replace("_", "-") }}/badge/?version=latest
        :target: https://{{ cookiecutter.project_directory | replace("_", "-") }}.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status
{%- endif %}

{% if cookiecutter.add_pyup_badge == 'y' %}
.. image:: https://pyup.io/repos/github/{{ cookiecutter.github_username_or_organization }}/{{ cookiecutter.project_directory }}/shield.svg
     :target: https://pyup.io/repos/github/{{ cookiecutter.github_username_or_organization }}/{{ cookiecutter.project_directory }}/
     :alt: Updates
{% endif %}


{{ cookiecutter.project_short_description }}

{% if is_open_source %}
* Free software: {{ cookiecutter.open_source_license }}
* Documentation: https://{{ cookiecutter.project_directory | replace("_", "-") }}.readthedocs.io.
{% endif %}

Features
--------

* TODO

Credits
-------

This package was created with Cookiecutter_ and the `elgertam/cookiecutter-pipenv`_ project template, based on `audreyr/cookiecutter-pypackage`_.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`elgertam/cookiecutter-pipenv`: https://github.com/elgertam/cookiecutter-pipenv
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
