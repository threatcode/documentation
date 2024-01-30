---
Title: watobo
Homepage: https://sourceforge.net/projects/watobo/
Repository: https://gitlab.com/kalilinux/packages/watobo
Architectures: any
Version: 1.0.1-0kali2
Metapackages: kali-linux-everything kali-tools-web 
Icon: images/watobo-logo.svg
PackagesInfo: |
 ### watobo
 
  WATOBO is intended to enable security professionals to perform highly efficient
  (semi-automated) web application security audits. It works like a local web
  proxy.
 
 **Installed size:** `3.28 MB`  
 **How to install:** `sudo apt install watobo`  
 
 {{< spoiler "Dependencies:" >}}
 * bundler
 * pry
 * ruby
 * ruby-fxruby
 * ruby-jwt
 * ruby-mechanize 
 * ruby-net-http-pipeline
 * ruby-selenium-webdriver 
 {{< /spoiler >}}
 
 ##### watobo
 
 
 ```
 root@kali:~# watobo -h
 #############################################################
 
      W A T O B O - THE Web Application Toolbox
      brought to you by siberas http://www.siberas.de
 
 #############################################################
 + looking for DEV_ENV environment variable ...[N/A]
 /usr/share/watobo/config/datastore.yml
 /usr/share/watobo/config/forwarding_proxy.yml
 /usr/share/watobo/config/general.yml
 /usr/share/watobo/config/gui.yml
 /usr/share/watobo/config/interceptor.yml
 /usr/share/watobo/config/ott_cache.yml
 /usr/share/watobo/config/scan_policy.yml
 /usr/share/watobo/config/scanner.yml
 /usr/share/watobo/config/scope.yml
 /usr/share/watobo/config/sid_cache.yml
 ---
 uninitialized constant Watobo::Modules::Active::Ror
 
             class_constant = Watobo::Modules::Active.const_get(group_class).const_get(module_class)
                                                     ^^^^^^^^^^
 when loading module file /usr/share/watobo/modules/active/RoR/cve_2013_015x.rb
 ---
 ---
 uninitialized constant Watobo::Modules::Active::Sap
 
             class_constant = Watobo::Modules::Active.const_get(group_class).const_get(module_class)
                                                     ^^^^^^^^^^
 when loading module file /usr/share/watobo/modules/active/sap/business_objects.rb
 ---
 
 Loading FXRuby ... this may take some time ... [OK]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
