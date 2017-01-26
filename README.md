Role Name
=========

This simple role allow you to install [Gandyn](https://github.com/Chralu/gandyn). Gandyn is a simple python script to connect to [Gandi](https://www.gandi.net/) domain name  API and automatically refresh zone entries. Allowing you to setup a dynamic DNS. This extremly useful when you don't have a fix public IP address.

Requirements
------------

A Gandi API key. Follow this [link](https://wiki.gandi.net/en/xml-api/activate) if you don't have one.

Role Variables
--------------

This all the variables you can tweak and theire default values.

```
gandyn_api_key: '' #your Gandi API key to connect to the API
gandyn_domain_name: '' #the domain name you want to update entries of.
gandyn_record_TTL: 300 
gandyn_record_type: 'A'
gandyn_record_name: '@'
gandyn_log_level: logging.INFO
gandyn_log_file: '/var/log/gandyn.log'
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
    - hosts: servers
      vars:
	   - gandyn_api_key: "xxxxxxxxxxxx"
	   - gandyn_domain_name: "domain.tld"
	   - gandyn_record_name: "subdomain"
      roles:
         - loikg.gandyn
```

License
-------

The Unlicensed
