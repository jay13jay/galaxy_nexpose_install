Nexpose Install
=========

Install Nexpose

## Notes
___
- Module incomplete
- the download takes a while (around 10 mins@3-4MB/s)
  

## Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

## Role Variables
--------------

Role Variables are the following:
```
nexpose_product_key: XXXX-XXXX-XXXX-XXXX
nexpose_download_url: https://download2.rapid7.com/download/InsightVM/
nexpose_filename: Rapid7Setup-Linux64.bin
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

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

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
