
before
---

* need set up environment variable

~~~
http_proxy=***
https_proxy=***
~~~

ruby version 2.2.0
vagrant version 1.7.1

vagrant plugins
---

~~~
$ vagrant plugin install vagrant-proxyconf
$ vagrant plugin install vagrant-omnibus
$ vagrant plugin install vagrant-vbguest
~~~

gems
---

~~~
$ bundle install
~~~

add community cookbooks
---

~~~
$ bundle exec berks vendor cookbooks
~~~

how to run
---

~~~
$ vagrant up --provision
~~~


Serverspec
---

* setup ssh
  
  起動状態で以下

  ~~~
  vagrant ssh-config --host develop2015 >> ~/.ssh/config
  ~~~

* run serverspec 

  ~~~
  bundle exec rake spec
  ~~~
