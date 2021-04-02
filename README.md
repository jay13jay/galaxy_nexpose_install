Nexpose Install
=========

Install Nexpose

## Notes
___
- Module in development
- The download takes a while (around 10 mins@3-4MB/s)
- The install takes even longer (didn't even time it, just walked away and came back later)
- vars/main.yml needs to be modified with your information for this to run
  - I have gone back and forth on whether to put default values for the required vars or not, if you have an opinion feel free to create an issue on github and I will take it into account
  

## Requirements
------------

- *unix install
  - tested on Arch and Centos 7

## Role Variables
--------------

Role Variables are the following:
```
nexpose_product_key: XXXX-XXXX-XXXX-XXXX
nexpose_download_url: https://download2.rapid7.com/download/InsightVM/
nexpose_filename: Rapid7Setup-Linux64.bin

# Nexpose SSL cert info:
first_name: [FIRST NAME]
last_name: [LAST NAME]
company: [COMPANY NAME]

# Nexpose auth info
user: [USERNAME]
password: [PASSWORD]
require_reset: "n"
```
- nexpose_product_key
  - First things first, you need a non-free email account, so you need to use an email from a domain you own. Gmail, yahoo, etc emails will not work
  - If you do not own a domain name you can use for this, you can use the following service:
  https://temp-mail.org
  - you get the install from downloading nexpose from their website:
    ```
    https://www.rapid7.com/try/nexpose/
    ```
    - This should already be configured in the role, however, you just need to double check the configured variables and input your product key emailed to you when signing up
  

## Dependencies
___

None (so far)

## Example Playbook
----------------

    - hosts: servers
      roles:
         - nexpose

## License
-------

BSD

### Author Information
------------------

Name: Josh Hackney

Email: jhaxllc@gmail.com

github: https://github.com/jay13yaj
