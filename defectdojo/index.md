---
Title: defectdojo
Homepage: https://github.com/DefectDojo/django-DefectDojo
Repository: https://gitlab.com/kalilinux/packages/defectdojo
Architectures: amd64 arm64 armhf
Version: 2.12.0-0kali2
Metapackages: kali-linux-everything kali-tools-identify 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### defectdojo
 
  This package contains a security orchestration and vulnerability management
  platform. DefectDojo allows you to manage your application security program,
  maintain product and application information, triage vulnerabilities and push
  findings to systems like JIRA and Slack. DefectDojo enriches and refines
  vulnerability data using a number of heuristic algorithms that improve with
  the more you use the platform.
 
 **Installed size:** `165.38 MB`  
 **How to install:** `sudo apt install defectdojo`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * celery
 * nginx
 * postgresql
 * python3-argon2
 * python3-asteval
 * python3-bleach
 * python3-celery
 * python3-cpe
 * python3-cvss
 * python3-django-appconf
 * python3-django-auditlog
 * python3-django-celery-results
 * python3-django-crispy-forms
 * python3-django-crum
 * python3-django-dbbackup
 * python3-django-environ
 * python3-django-extensions
 * python3-django-fieldsignals
 * python3-django-filters
 * python3-django-imagekit
 * python3-django-multiselectfield
 * python3-django-polymorphic
 * python3-django-ratelimit
 * python3-django-restframework-guardian
 * python3-django-split-settings
 * python3-django-tagging
 * python3-django-tagulous
 * python3-django-watson
 * python3-djangorestframework-spectacular
 * python3-drf-yasg-nonfree
 * python3-git
 * python3-github
 * python3-googleapi
 * python3-gunicorn
 * python3-html2text
 * python3-hyperlink
 * python3-jira
 * python3-jose
 * python3-json-log-formatter
 * python3-lxml
 * python3-markdown
 * python3-numpy
 * python3-openpyxl
 * python3-packageurl
 * python3-psycopg2
 * python3-social-django
 * python3-titlecase
 * python3-vobject
 * redis-server
 * sudo
 * uuid-runtime
 * uwsgi-plugin-python3
 {{< /spoiler >}}
 
 ##### defectdojo
 
 
 ```
 root@kali:~# defectdojo -h
 User _defectdojo already exists in PostgreSQL
 Database defectdojo already exists in PostgreSQL
 ALTER ROLE
 Waiting for database to be reachable 
 Making migrations
 No changes detected in app 'dojo'
 Migrating
 ```
 
 - - -
 
 ##### defectdojo-stop
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
