# vagrant-chef-server-bootstrap

Vagrant file &amp; cookbooks to install chef-server in VM

## NOTES

There seems to be a problem with the installation, which seems related to the gem:
The file `/etc/init.d/chef-server` has:

	DAEMON=/usr/bin/chef-server

but it should read:

	DAEMON=/usr/sbin/chef-server

After changing this issue `/etc/init.d/chef-server start` and it will start.

The web UI suffers from the same issue, the file `/etc/init.d/chef-server-webui` has:

  	DAEMON=/usr/bin/chef-server-webui

but is should read:

  	DAEMON=/user/sbin/chef-server-webui

After changing this issue `/etc/init.d/chef-server-webui start` and it will start.

## Using

Once the above is changed go to [http://localhost:4000](http://localhost:4000) to see REST API working.
The Web UI is on [http://localhost:4040](http://localhost:4040).

# License

vagrant-chef-server-bootstrap is licensed under MIT license.

	Copyright (C) 2011 Tom de Grunt <tom@degrunt.nl>

	Permission is hereby granted, free of charge, to any person obtaining a copy of
	this software and associated documentation files (the "Software"), to deal in
	the Software without restriction, including without limitation the rights to
	use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
	of the Software, and to permit persons to whom the Software is furnished to do
	so, subject to the following conditions:

	The above copyright notice and this permission notice shall be included in all
	copies or substantial portions of the Software.

	THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
	IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
	FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
	AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
	LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
	OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
	SOFTWARE.
