foreman\_tasks\_cleanup
=========

Simple role which runs the Foreman cleanup tasks, so it is possible to schedule them from Ansible Tower.

It is not the best implementation since it uses the shell module.

Requirements
------------

Foreman/Satellite installed on the host where the cleanup process is going to be executed.

Role Variables
--------------

**days**: Number of days of tasks to keep. (Default: **30**)

Example: days=30 means that just the latest 30 days of tasks are going to stay stored.

**verbose**: Prints debug info after running the role. (Default: **true**)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: satellite
      roles:
         - { role: satellite_tasks_cleanup , x: 42 }

License
-------

GPL v3.0

Author Information
------------------

Sergio Pérez Fernández
