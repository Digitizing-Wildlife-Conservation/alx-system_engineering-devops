   0x17. Web stack debugging #3 DevOps SysAdmin Scripting Debugging Cohort

Web Stack Debugging #3
Description
This project focuses on debugging a  website running on a LAMP stack that is encountering a 500 Internal Server Error. The task involves using strace to identify the issue causing the error, fixing it, and then automating the fix using Puppet.

Tasks
0. Strace is your friend
Using strace, identify the reason behind Apache returning a 500 error.
Fix the issue and automate the fix using Puppet.
Puppet code should be contained in 0-strace_is_your_friend.pp file.
Utilize any Puppet resource type for the fix.
Requirements
All files should be interpreted on Ubuntu 14.04 LTS.
Files should end with a new line.
Puppet manifests must pass puppet-lint version 2.1.1 without any errors.
Puppet manifests must run without error.
Puppet manifests' first line must be a comment explaining the manifest's purpose.
Puppet manifests files must end with the extension .pp.
Puppet v3.4 will be used for checking.
Setup
Install puppet-lint:
bash
Copy code
$ apt-get install -y ruby
$ gem install puppet-lint -v 2.1.1
Execution Example
bash
Copy code
$ curl -sI 127.0.0.1
HTTP/1.0 500 Internal Server Error
Date: Fri, 24 Mar 2017 07:32:16 GMT
Server: Apache/2.4.7 (Ubuntu)
X-Powered-By: PHP/5.5.9-1ubuntu4.21
Connection: close
Content-Type: text/html

$ puppet apply 0-strace_is_your_friend.pp
Notice: Compiled catalog for e514b399d69d.ec2.internal in environment production in 0.02 seconds
Notice: /Stage[main]/Main/Exec[fix-wordpress]/returns: executed successfully
Notice: Finished catalog run in 0.08 seconds

$ curl -sI 127.0.0.1:80
HTTP/1.1 200 OK
Date: Fri, 24 Mar 2017 07:11:52 GMT
Server: Apache/2.4.7 (Ubuntu)
X-Powered-By: PHP/5.5.9-1ubuntu4.21
Link: <http://127.0.0.1/?rest_route=/>; rel="https://api.w.org/"
Content-Type: text/html; charset=UTF-8
Repository Information
GitHub repository: alx-system_engineering-devops
Directory: 0x17-web_stack_debugging_3
File: 0-strace_is_your_friend.pp
Concepts
Web Server
Web stack debugging
Background Context
Logs may not always provide enough information when debugging.
Websites that  runs on a LAMP stack (Linux, Apache, MySQL, and PHP).
Debugging may require going down the stack.
