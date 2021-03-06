========================================
Bootstrap carousel plugin for Django-CMS
========================================

.. image:: https://travis-ci.org/nimbis/cmsplugin-bootstrap-carousel.svg?branch=master
   :target: https://travis-ci.org/nimbis/cmsplugin-bootstrap-carousel

.. image:: https://coveralls.io/repos/nimbis/cmsplugin-bootstrap-carousel/badge.png?branch=master
   :target: https://coveralls.io/r/nimbis/cmsplugin-bootstrap-carousel?branch=master

A Django-CMS plugin to easily create carousel components using Bootstrap, from Twitter.
Forked from: https://bitbucket.org/tonioo/cmsplugin-bootstrap-carousel

This plugin supports filer and will use it if it is found in your INSTALLED_APPS.

Requirements
============

* `Django-CMS >= 2.4 <http://django-cms.org>`_
* `Bootstrap <http://twitter.github.com/bootstrap/>`_
* `easy-thumbnails <https://github.com/SmileyChris/easy-thumbnails>`_
* `Pillow`
* `filer` is optional.


Installation
============

To use it into your project, just follow this procedure:

#. Install the the plugin in your virtualenv, using::

    pip install cmsplugin-bootstrap-carousel

and remember to add it to your requirements.txt file, if you use one.

#. Open the *settings.py* file and add ``cmsplugin_bootstrap_carousel`` to the
   ``INSTALLED_APPS`` variable

#. This plugin will use filer if it is in your INSTALLED_APPS

#. add::

    THUMBNAIL_HIGH_RESOLUTION = True
    
to settings.py, if you want to support retina displays in the admin. (Otherwise 
you may encounter missing image placeholders in image file listings.)

#. Run the following command::

    $ ./manage.py syncdb


.. note::

    Bootstrap is not included with this plugin.

History
=======

0.2.1:

    * Changed plugin name from CarouselPlugin to BootstrapCarouselPlugin to avoid name collision
    with djangocms-cascade.

0.2.0:

    * Added fields for toggling visibility of carousel controls and slide indicator. Improved the included template.