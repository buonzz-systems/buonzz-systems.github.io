---
layout: no-sidebar
title:  "Installing LDAP in Ubuntu"
date:   2016-05-20 10:03:02
categories: tutorial devops
---

<article id="content">
	<header>
		<h2>Installing LDAP in Ubuntu</h2>
	</header>
	<p>Lets install slapd, utilities and few libraries</p>
{% highlight bash %}
sudo apt-get install libldap-2.4-2  slapd ldap-utils
{% endhighlight %}
	
	<p>The installation will set some default, but we would like to customize some of it, so lets execute</p>
{% highlight bash %}
sudo dpkg-reconfigure slapd
{% endhighlight %}	

	<p>We also would like to install PHPmyLDAPAdmin</p>
{% highlight bash %}
sudo apt-get update
sudo apt-get install phpldapadmin
{% endhighlight %}
	<p>Edit /etc/phpldapadmin/config.php with the appropriate values.</p>
</article>