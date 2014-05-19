The OpenShift `diy` cartridge documentation can be found at:

https://github.com/openshift/origin-server/tree/master/cartridges/openshift-origin-cartridge-diy/README.md

    git clone https://github.com/mignev/ruby21.git

```sh    
app create myruby21 diy-0.1
cd myruby21
mv ../ruby21/* .
mv ../ruby21/.openshift/action_hooks/* .openshift/action_hooks/
git add .
git commit -m "Initial Commit"
git push -f
```

If everything is okay the result should be something like this:

```sh
@mignev in ~/tmp/myruby21 (master)
→ git push -f
Counting objects: 70, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (54/54), done.
Writing objects: 100% (65/65), 15.68 KiB | 0 bytes/s, done.
Total 65 (delta 3), reused 0 (delta 0)
remote: Stopping DIY cartridge
remote: Building git ref 'master', commit c86f7ca
remote: /var/lib/openshift/5379db520fe7e61ce4000059/app-root/data /var/lib/openshift/5379db520fe7e61ce4000059
remote:   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
remote:                                  Dload  Upload   Total   Spent    Left  Speed
remote: 107  1184  107  1184    0     0   1445      0 --:--:-- --:--:-- --:--:--  8165
remote: Initialized empty Git repository in /var/lib/openshift/5379db520fe7e61ce4000059/app-root/data/.rbenv/.git/
remote: Initialized empty Git repository in /var/lib/openshift/5379db520fe7e61ce4000059/app-root/data/.rbenv/plugins/rbenv-vars/.git/
remote: Initialized empty Git repository in /var/lib/openshift/5379db520fe7e61ce4000059/app-root/data/.rbenv/plugins/ruby-build/.git/
remote: Initialized empty Git repository in /var/lib/openshift/5379db520fe7e61ce4000059/app-root/data/.rbenv/plugins/openshift-rbenv-installer/.git/
remote: /var/lib/openshift/5379db520fe7e61ce4000059
remote: Downloading yaml-0.1.6.tar.gz...
remote: -> http://dqw8nmjcqpjn7.cloudfront.net/5fe00cda18ca5daeb43762b80c38e06e
remote: Installing yaml-0.1.6...
remote: Installed yaml-0.1.6 to /var/lib/openshift/5379db520fe7e61ce4000059/app-root/data//.rbenv/versions/2.1.0
remote:
remote: Downloading ruby-2.1.0.tar.gz...
remote: -> http://dqw8nmjcqpjn7.cloudfront.net/9e6386d53f5200a3e7069107405b93f7
remote: Installing ruby-2.1.0...
...
...
and so on and so on ....
```

It will take several minutes.
