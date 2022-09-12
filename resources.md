---
layout: default
title: Project Resources
nav_order: 5
---

# Project Resources
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Git Resources
![Git Cheat Sheet](/assets/images/git-cheat-sheet.png?raw=true "Git Cheat Sheet")

* [Git tutorial](https://kbroman.org/github_tutorial/)

## Web Design Resources

* Web Content Accessibility Guidelines (WCAG) 2021 Quick Reference: [https://www.w3.org/WAI/WCAG21/quickref/](https://www.w3.org/WAI/WCAG21/quickref/)
* Four basic principles: Perceivable, Operable, Understandable, Robust
* Semantic & Accessible HTML on MDN: [https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML)
* Accessible Rich Internet Applications (ARIA) Reference on MDN: [https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
Use ARIA only in cases that aren't covered by HTML 5 semantic tags. In particular, check out the tutorials section, where they demonstrate how a screen reader parses web pages.
* ANDI Free Accessibility Testing Tool: [https://www.ssa.gov/accessibility/andi/help/install.html](https://www.ssa.gov/accessibility/andi/help/install.html)
Do NOT use this as a one-stop shop to test for accessibility. In the end, you are responsible for ensuring compliance with accessibility standards. This tool only tests compliance with Section 508, a set of standards developed for federally-funded site accessibility. It does not necessarily imply compliance with WCAG or accessibility as a general concept.
* WebAIM Contrast Checker Tool: [https://webaim.org/resources/contrastchecker/](https://webaim.org/resources/contrastchecker/)
This tool is great because it tells you whether you are passing WCAG contrast guidelines!
* Great Slideshow on Usability by UVA's own Professor Praphamontripong: [http://www.cs.virginia.edu/~up3f/cs4640/slides/4640meet03A-UsabilityPrinciples.pdf](http://www.cs.virginia.edu/~up3f/cs4640/slides/4640meet03A-UsabilityPrinciples.pdf)
* Here's a helpful infographic! For larger version, visit [https://webaim.org/resources/designers/](https://webaim.org/resources/designers/)

## Django Resources

* [Creating python virtual env](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/)
* [Tutorial on the basics of Django (YouTube Series)](https://www.youtube.com/watch?v=UmljXZIypDc)
* [Django generic editing views](https://docs.djangoproject.com/en/3.1/ref/class-based-views/generic-editing/)

## Heroku Resources
* [Deploying Django project to Heroku](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Deployment)
* [Deploying Python / Django apps on Heroku](https://devcenter.heroku.com/articles/python-gunicorn)
* [Making Heroku automatically always do migrations whenever a new build is made](https://help.heroku.com/GDQ74SU2/django-migrations) - This fixes the "missing relation" problem on Heroku.

### Avoiding the macOS / psycopg2 error

Use this code at the bottom of your `settings.py` file to try/catch the import of django-heroku so it only has to work when deployed to heroku and not locally:

```
# Activate Django-Heroku.
# Use this code to avoid the psycopg2 / django-heroku error!  
# Do NOT import django-heroku above!
try:
    if 'HEROKU' in os.environ:
        import django_heroku
        django_heroku.settings(locals())
except ImportError:
    found = False
```
