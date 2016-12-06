logrotate
=========

Log rotation for your application.

Rotation configuration:

    {{logrotate_logfile}} {
        daily
        missingok
        rotate {{logrotate_rotate}}
        compress
        delaycompress
        notifempty
        create 600 {{logroate_user}} {{logrotate_group}}
    }

Role Variables
--------------

    logrotate_name: web-app
    logrotate_logfile: /home/web-app/web-app/logs/debug.log
    logrotate_user: ubuntu
    logrotate_group: ubuntu
    logrotate_rotate: 14


Example Playbook
----------------

    - hosts: servers
      roles:
         - role: WebbyLab.logrotate
           logrotate_name: web-app
           logrotate_logfile: /home/web-app/web-app/logs/debug.log
           logrotate_user: ubuntu
           logrotate_group: ubuntu
           logrotate_rotate: 14

License
-------

MIT

Author Information
------------------

WebbyLab (http://webbylab.com)
