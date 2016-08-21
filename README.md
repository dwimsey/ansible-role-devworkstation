ansible-role-devworkstation
===========================

Adds various tools and configuration to produce a workstation ready for software development.

Requirements
------------

This rule does not require any prerequisites at this time.

Role Variables
--------------

install_desktop: Set this value to false to skip the installation of the a desktop environment on the target host.  This does not apply to Windows or Mac OS X targets which come with a desktop environment out of the box.

Dependencies
------------

1. dwimsey.devenv - This role requires the dwimsey.devenv role to be applied first.  Some aspects of this role will be controlled by the dwimsey.devenv role, such as skipping IntelliJ if Java has been skipped by devenv and is not available on the target system.
2. jdauphant.intellij - This role requires the jdauphant.intellij in order to install the JetBrains IntelliJ IDE.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: dwimsey.devworkstation, install_desktop: false }

License
-------

Copyright (c) 2016 David Wimsey

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Author Information
------------------

David Wimsey <david@wimsey.us>
