JDK install
=========

A role that maintance oracle jdk and openjdk, include break jce limit

Requirements
------------

Current only support EL

Role Variables
--------------

vendor could be oracle or openjdk
 
 jdk_vendor: 'oracle'

version should be 1.6 1.7 1.8

 jdk_version: 1.7

due to US's export policy , there is a limit to the  Java Cryptography Extension (JCE),
so when you choose oracle jdk , you should replace the default jce to Unlimited Strength one

 is_unlimited_jce: 'true'
 jce_1_7_oracle_url: "http://somehttpshare/jce/UnlimitedJCEPolicyJDK7.zip"
 jce_1_8_oracle_url: "http://somehttpshare/jce/jce_policy-8.zip"


Dependencies
------------
none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars:
       jdk_vendor: 'oracle'
       jdk_version: 1.7
       is_unlimited_jce: 'true'
       jce_1_7_oracle_url: "http://somehttpshare/jce/UnlimitedJCEPolicyJDK7.zip"
      roles:
         - role: jjmomark.jdk

License
-------

BSD

Author Information
------------------

https://github.com/jagjag

