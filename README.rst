armstrong.templates.paywayll
============================
Provides a basic example of how to create a paywall inside Armstrong

This template shows a working version of paywall code. The paywall is declared
in ``urls/defaults.py``.

Usage
-----
You can use this to initial a demo Armstrong project with a paywall.  The paywall
is defined in ``urls/defaults.py``.   By default, the ``SubscriptionPaywall``
returns a 304 when access is denied, but it has been overriden to render the
``permission_denied.html`` template instead. The only view that needs to be
protected is the ``ArticleDetailView``.

The third article on the front page, 'Help Wanted' is protected. When not
logged in, the ``permission_denied.html`` will be rendered, but when logged in as a
staff member or as the user with the username ``user`` and password of ``user`` you
will see the normal ``article.html`` template.


You can install this demo project template via the ``armstrong`` binary that
ships with `armstrong.cli`_ like this:

::

    $ armstrong init --template=paywall

You must install this package in order to be able to use ``armstrong init``.
You can also use it via Django's ``django-admin.py`` as of Django 1.4.  Create
a clone of the ``armstrong.templates.paywall`` repository and run this command
(adjusting the paths for your machine):

::

    $ django-admin.py startproject --template=/path/to/armstrong.templates.paywall/project_template

.. _armstrong.cli: https://github.com/armstrong/armstrong.cli


Installation & Configuration
----------------------------
You can install the latest release of ``armstrong.templates.paywall`` using `pip`_:

::

    pip install armstrong.templates.paywall

No configuration is required for this component.

.. _pip: http://www.pip-installer.org/


Contributing
------------

* Create something awesome -- make the code better, add some functionality,
  whatever (this is the hardest part).
* `Fork it`_
* Create a topic branch to house your changes
* Get all of your commits in the new topic branch
* Submit a `pull request`_

.. _pull request: http://help.github.com/pull-requests/
.. _Fork it: http://help.github.com/forking/


State of Project
----------------
Armstrong is an open-source news platform that is freely available to any
organization.  It is the result of a collaboration between the `Texas Tribune`_
and `Bay Citizen`_, and a grant from the `John S. and James L. Knight
Foundation`_.

To follow development, be sure to join the `Google Group`_.

``armstrong.templates.paywall`` is part of the `Armstrong`_ project.  You're
probably looking for that.

.. _Texas Tribune: http://www.texastribune.org/
.. _Bay Citizen: http://www.baycitizen.org/
.. _John S. and James L. Knight Foundation: http://www.knightfoundation.org/
.. _Google Group: http://groups.google.com/group/armstrongcms
.. _Armstrong: http://www.armstrongcms.org/


License
-------
Copyright 2011-2012 Bay Citizen and Texas Tribune

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
