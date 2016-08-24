MLS-Workbook
============

Red Hat Government hands-on workshop to explore MLS System Operation under RHEL6


Developer Notes
============
The MLS workbook has been designed around the Publican documentation system:
https://fedorahosted.org/publican/

Make sure rhel-7-server-optional-rpms is enabled on your system. Once enabled, to install Publican on Fedora or RHEL:

$ sudo yum install publican publican-redhat


Additionally, Publican utilizes ~/.publican.cfg to set default build parameters. The following
defaults are recommended:

$ echo 'firstname: "FirstName"' >> ~/.publican.cfg

$ echo 'surname: "LastName"' >> ~/.publican.cfg

$ echo 'email: "Your@EMail.com"' >> ~/.publican.cfg

$ echo 'formats: "html,html-single,pdf,txt,epub"' >> ~/.publican.cfg

$ echo 'langs: "en-US"' >> ~/.publican.cfg


To run a build:

$ make content

Output will be placed into the tmp/ directory, e.g.:
tmp/en-US/html-single/
