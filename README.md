Guacamole API testing
=========

Some quick tests to interact with the Guacamole API from ansible.

Just a PoC/prototype to find out the available features in the API.

By now only RDP connections have been tested but adding support to create VNC connections should be trivial.


Requirements
------------

To use this playbook you need admin access to a guacamole instance. 

For testing and debugging you can use the provided [docker-compose.yml](docker-compose.yml) in this repo. Run `docker-compose up` to get a guacamole instance accessible in [http://localhost](http://localhost) with the default username and password `guacadmin/guacadmin` .


Testing the playbook
------------

Once you have a running guacamole instance just try:
```
ansible-playbook playbook_guacamole.yml -e guacamole_connection_name=test_connection_1 -e guacamole_username_to_create=test_user_1 -vv
```

Playbook Variables
--------------

Check the header of the [playbook](playbook_guacamole.yml) for a detailed list of variables

You should modify "guacamole access info" vars if you want to use this playbook with your guacamole instance.


License
-------

BSD

Author Information
------------------

Pablo Escobar Lopez

