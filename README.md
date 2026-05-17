# TIMP_1

# Отчёт по самой лабе:

```
reyne@reyne-VirtualBox:/run/media/reyne/VBox_GAs_7.2.6$ export GITHUB_USERNAME=reyne
reyne@reyne-VirtualBox:/run/media/reyne/VBox_GAs_7.2.6$ $ export GIST_TOKEN=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
$: command not found
reyne@reyne-VirtualBox:/run/media/reyne/VBox_GAs_7.2.6$ export GIST_TOKEN=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
reyne@reyne-VirtualBox:/run/media/reyne/VBox_GAs_7.2.6$ alias edit=<nano|vi|vim|subl>
bash: syntax error near unexpected token `newline'
reyne@reyne-VirtualBox:/run/media/reyne/VBox_GAs_7.2.6$ alias edit=nano
reyne@reyne-VirtualBox:/run/media/reyne/VBox_GAs_7.2.6$ mkdir -p ${GITHUB_USERNAME}/workspace
mkdir: Read-only file system
reyne@reyne-VirtualBox:/run/media/reyne/VBox_GAs_7.2.6$ cd ~
pwd
/home/reyne
reyne@reyne-VirtualBox:~$ mkdir -p ${GITHUB_USERNAME}/workspace
reyne@reyne-VirtualBox:~$ cd ${GITHUB_USERNAME}/workspace
reyne@reyne-VirtualBox:~/reyne/workspace$ pwd
/home/reyne/reyne/workspace
reyne@reyne-VirtualBox:~/reyne/workspace$ cd ..
reyne@reyne-VirtualBox:~/reyne$ pwd
/home/reyne/reyne
reyne@reyne-VirtualBox:~/reyne$ mkdir -p workspace/tasks/
reyne@reyne-VirtualBox:~/reyne$ mkdir -p workspace/projects/
reyne@reyne-VirtualBox:~/reyne$ mkdir -p workspace/reports/
reyne@reyne-VirtualBox:~/reyne$ cd workspace
reyne@reyne-VirtualBox:~/reyne/workspace$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
--2026-05-17 21:55:17--  https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
Resolving nodejs.org (nodejs.org)... 104.16.212.131, 104.16.213.131, 2606:4700::6810:d583, ...
Connecting to nodejs.org (nodejs.org)|104.16.212.131|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9356460 (8.9M) [application/x-xz]
Saving to: ‘node-v6.11.5-linux-x64.tar.xz’

node-v6.11.5-linux- 100%[===================>]   8.92M  11.7MB/s    in 0.8s    

2026-05-17 21:55:19 (11.7 MB/s) - ‘node-v6.11.5-linux-x64.tar.xz’ saved [9356460/9356460]

reyne@reyne-VirtualBox:~/reyne/workspace$ tar -xf node-v6.11.5-linux-x64.tar.xz
reyne@reyne-VirtualBox:~/reyne/workspace$ rm -rf node-v6.11.5-linux-x64.tar.xz
reyne@reyne-VirtualBox:~/reyne/workspace$ mv node-v6.11.5-linux-x64 node
reyne@reyne-VirtualBox:~/reyne/workspace$ ls node/bin
node  npm
reyne@reyne-VirtualBox:~/reyne/workspace$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin
reyne@reyne-VirtualBox:~/reyne/workspace$ export PATH=${PATH}:`pwd`/node/bin
reyne@reyne-VirtualBox:~/reyne/workspace$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin:/home/reyne/reyne/workspace/node/bin
reyne@reyne-VirtualBox:~/reyne/workspace$ mkdir scripts
reyne@reyne-VirtualBox:~/reyne/workspace$ cat > scripts/activate<<EOF
export PATH=\${PATH}:`pwd`/node/bin
EOF
reyne@reyne-VirtualBox:~/reyne/workspace$ source scripts/activate
reyne@reyne-VirtualBox:~/reyne/workspace$ gem install gist
Command 'gem' not found, but can be installed with:
sudo snap install ruby           # version 4.0.3, or
sudo apt  install ruby-rubygems  # version 3.6.7-2ubuntu2
See 'snap info ruby' for additional versions.
reyne@reyne-VirtualBox:~/reyne/workspace$ sudo apt  install ruby-rubygems
[sudo: authenticate] Password:             
The following packages were automatically installed and are no longer required:
  linux-headers-7.0.0-14                   linux-modules-7.0.0-14-generic
  linux-headers-7.0.0-14-generic           linux-tools-7.0.0-14
  linux-image-unsigned-7.0.0-14-generic    linux-tools-7.0.0-14-generic
  linux-main-modules-zfs-7.0.0-14-generic
Use 'sudo apt autoremove' to remove them.

Installing:
  ruby-rubygems

Installing dependencies:
  libruby     ruby-csv             ruby-sdbm     rubygems-integration
  libruby3.3  ruby-did-you-mean    ruby-webrick
  rake        ruby-net-telnet      ruby-xmlrpc
  ruby        ruby-ruby2-keywords  ruby3.3

Suggested packages:
  ri  ruby-dev  bundler

Summary:
  Upgrading: 0, Installing: 14, Removing: 0, Not Upgrading: 2
  Download size: 6,478 kB
  Space needed: 32.9 MB / 11.7 GB available

Continue? [Y/n] y
Get:1 http://archive.ubuntu.com/ubuntu resolute/main amd64 rubygems-integration all 1.19build1 [5,666 B]
Get:2 http://archive.ubuntu.com/ubuntu resolute/main amd64 ruby3.3 amd64 3.3.8-2ubuntu3 [49.1 kB]
Get:3 http://archive.ubuntu.com/ubuntu resolute/main amd64 ruby-rubygems all 3.6.7-2ubuntu2 [332 kB]
Get:4 http://archive.ubuntu.com/ubuntu resolute/main amd64 ruby amd64 1:3.3build1 [3,678 B]
Get:5 http://archive.ubuntu.com/ubuntu resolute/main amd64 rake all 13.3.1-1 [46.1 kB]
Get:6 http://archive.ubuntu.com/ubuntu resolute/main amd64 ruby-csv all 3.3.5-1 [43.1 kB]
Get:7 http://archive.ubuntu.com/ubuntu resolute/main amd64 ruby-did-you-mean all 2.0.0-1 [14.7 kB]
Get:8 http://archive.ubuntu.com/ubuntu resolute/main amd64 ruby-net-telnet all 0.2.0-1build1 [13.5 kB]
Get:9 http://archive.ubuntu.com/ubuntu resolute/main amd64 ruby-ruby2-keywords all 0.0.5-1build1 [4,398 B]
Get:10 http://archive.ubuntu.com/ubuntu resolute/main amd64 ruby-webrick all 1.9.2-1 [61.0 kB]
Get:11 http://archive.ubuntu.com/ubuntu resolute/main amd64 ruby-xmlrpc all 0.3.3-2build1 [24.9 kB]
Get:12 http://archive.ubuntu.com/ubuntu resolute/main amd64 libruby3.3 amd64 3.3.8-2ubuntu3 [5,858 kB]
Get:13 http://archive.ubuntu.com/ubuntu resolute/main amd64 libruby amd64 1:3.3build1 [5,272 B]
Get:14 http://archive.ubuntu.com/ubuntu resolute/main amd64 ruby-sdbm amd64 1.0.0-5build6 [16.1 kB]
Fetched 6,478 kB in 1s (7,845 kB/s)   
Selecting previously unselected package rubygems-integration.
(Reading database… 221120 files and directories currently installed.)
Preparing to unpack …/00-rubygems-integration_1.19build1_all.deb…
Unpacking rubygems-integration (1.19build1)…
Selecting previously unselected package ruby3.3.
Preparing to unpack …/01-ruby3.3_3.3.8-2ubuntu3_amd64.deb…
Unpacking ruby3.3 (3.3.8-2ubuntu3)…
Selecting previously unselected package ruby-rubygems.
Preparing to unpack …/02-ruby-rubygems_3.6.7-2ubuntu2_all.deb…
Unpacking ruby-rubygems (3.6.7-2ubuntu2)…
Selecting previously unselected package ruby.
Preparing to unpack …/03-ruby_1%3a3.3build1_amd64.deb…
Unpacking ruby (1:3.3build1)…
Selecting previously unselected package rake.
Preparing to unpack …/04-rake_13.3.1-1_all.deb…
Unpacking rake (13.3.1-1)…
Selecting previously unselected package ruby-csv.
Preparing to unpack …/05-ruby-csv_3.3.5-1_all.deb…
Unpacking ruby-csv (3.3.5-1)…
Selecting previously unselected package ruby-did-you-mean.
Preparing to unpack …/06-ruby-did-you-mean_2.0.0-1_all.deb…
Unpacking ruby-did-you-mean (2.0.0-1)…
Selecting previously unselected package ruby-net-telnet.
Preparing to unpack …/07-ruby-net-telnet_0.2.0-1build1_all.deb…
Unpacking ruby-net-telnet (0.2.0-1build1)…
Selecting previously unselected package ruby-ruby2-keywords.
Preparing to unpack …/08-ruby-ruby2-keywords_0.0.5-1build1_all.deb…
Unpacking ruby-ruby2-keywords (0.0.5-1build1)…
Selecting previously unselected package ruby-webrick.
Preparing to unpack …/09-ruby-webrick_1.9.2-1_all.deb…
Unpacking ruby-webrick (1.9.2-1)…
Selecting previously unselected package ruby-xmlrpc.
Preparing to unpack …/10-ruby-xmlrpc_0.3.3-2build1_all.deb…
Unpacking ruby-xmlrpc (0.3.3-2build1)…
Selecting previously unselected package libruby3.3:amd64.
Preparing to unpack …/11-libruby3.3_3.3.8-2ubuntu3_amd64.deb…
Unpacking libruby3.3:amd64 (3.3.8-2ubuntu3)…
Selecting previously unselected package libruby:amd64.
Preparing to unpack …/12-libruby_1%3a3.3build1_amd64.deb…
Unpacking libruby:amd64 (1:3.3build1)…
Selecting previously unselected package ruby-sdbm:amd64.
Preparing to unpack …/13-ruby-sdbm_1.0.0-5build6_amd64.deb…
Unpacking ruby-sdbm:amd64 (1.0.0-5build6)…
Setting up ruby-ruby2-keywords (0.0.5-1build1)…
Setting up rubygems-integration (1.19build1)…
Setting up ruby-net-telnet (0.2.0-1build1)…
Setting up ruby-csv (3.3.5-1)…
Setting up ruby-webrick (1.9.2-1)…
Setting up ruby-did-you-mean (2.0.0-1)…
Setting up ruby-xmlrpc (0.3.3-2build1)…
Setting up rake (13.3.1-1)…
Setting up ruby3.3 (3.3.8-2ubuntu3)…
Setting up libruby3.3:amd64 (3.3.8-2ubuntu3)…
Setting up ruby-rubygems (3.6.7-2ubuntu2)…
Setting up libruby:amd64 (1:3.3build1)…
Setting up ruby (1:3.3build1)…
Setting up ruby-sdbm:amd64 (1.0.0-5build6)…
Processing triggers for libc-bin (2.43-2ubuntu2)…
Processing triggers for man-db (2.13.1-1build1)…
reyne@reyne-VirtualBox:~/reyne/workspace$ gem install gist
Fetching gist-6.0.0.gem
Defaulting to user installation because default installation directory (/var/lib/gems/3.3.0) is not writable.
WARNING:  You don't have /home/reyne/.local/share/gem/ruby/3.3.0/bin in your PATH,
	  gem executables (gist) will not run.
Successfully installed gist-6.0.0
Parsing documentation for gist-6.0.0
Installing ri documentation for gist-6.0.0
Done installing documentation for gist after 0 seconds
1 gem installed
reyne@reyne-VirtualBox:~/reyne/workspace$ (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)
reyne@reyne-VirtualBox:~/reyne/workspace$ export LAB_NUMBER=01
reyne@reyne-VirtualBox:~/reyne/workspace$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Cloning into 'tasks/lab01'...
remote: Enumerating objects: 74, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 74 (delta 0), reused 1 (delta 0), pack-reused 71 (from 1)
Receiving objects: 100% (74/74), 945.07 KiB | 3.35 MiB/s, done.
Resolving deltas: 100% (20/20), done.
reyne@reyne-VirtualBox:~/reyne/workspace$ mkdir reports/lab${LAB_NUMBER}
reyne@reyne-VirtualBox:~/reyne/workspace$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
reyne@reyne-VirtualBox:~/reyne/workspace$ cd reports/lab${LAB_NUMBER}
reyne@reyne-VirtualBox:~/reyne/workspace/reports/lab01$ edit REPORT.md
reyne@reyne-VirtualBox:~/reyne/workspace/reports/lab01$ gist REPORT.md
Command 'gist' not found, but can be installed with:
sudo apt install yorick
reyne@reyne-VirtualBox:~/reyne/workspace/reports/lab01$ sudo apt install yorick
The following packages were automatically installed and are no longer required:
  linux-headers-7.0.0-14                   linux-modules-7.0.0-14-generic
  linux-headers-7.0.0-14-generic           linux-tools-7.0.0-14
  linux-image-unsigned-7.0.0-14-generic    linux-tools-7.0.0-14-generic
  linux-main-modules-zfs-7.0.0-14-generic
Use 'sudo apt autoremove' to remove them.

Installing:
  yorick

Installing dependencies:
  libptytty0  rlwrap  yorick-data  yorick-z

Suggested packages:
  yorick-full  emacsen

Summary:
  Upgrading: 0, Installing: 5, Removing: 0, Not Upgrading: 2
  Download size: 1,505 kB
  Space needed: 4,746 kB / 11.7 GB available

Continue? [Y/n] y
Get:1 http://archive.ubuntu.com/ubuntu resolute/universe amd64 libptytty0 amd64 2.0-1build1 [44.3 kB]
Get:2 http://archive.ubuntu.com/ubuntu resolute/universe amd64 rlwrap amd64 0.47.1-0.1 [107 kB]
Get:3 http://archive.ubuntu.com/ubuntu resolute/universe amd64 yorick-data all 2.2.04+dfsg1-14build1 [505 kB]
Get:4 http://archive.ubuntu.com/ubuntu resolute/universe amd64 yorick amd64 2.2.04+dfsg1-14build1 [812 kB]
Get:5 http://archive.ubuntu.com/ubuntu resolute/universe amd64 yorick-z amd64 1.2.0+cvs20080115-6build1 [36.7 kB]
Fetched 1,505 kB in 1s (1,775 kB/s) 
Selecting previously unselected package libptytty0:amd64.
(Reading database… 224566 files and directories currently installed.)
Preparing to unpack …/libptytty0_2.0-1build1_amd64.deb…
Unpacking libptytty0:amd64 (2.0-1build1)…
Selecting previously unselected package rlwrap.
Preparing to unpack …/rlwrap_0.47.1-0.1_amd64.deb…
Unpacking rlwrap (0.47.1-0.1)…
Selecting previously unselected package yorick-data.
Preparing to unpack …/yorick-data_2.2.04+dfsg1-14build1_all.deb…
Unpacking yorick-data (2.2.04+dfsg1-14build1)…
Selecting previously unselected package yorick.
Preparing to unpack …/yorick_2.2.04+dfsg1-14build1_amd64.deb…
Unpacking yorick (2.2.04+dfsg1-14build1)…
Selecting previously unselected package yorick-z.
Preparing to unpack …/yorick-z_1.2.0+cvs20080115-6build1_amd64.deb…
Unpacking yorick-z (1.2.0+cvs20080115-6build1)…
Setting up yorick-data (2.2.04+dfsg1-14build1)…
Setting up libptytty0:amd64 (2.0-1build1)…
Setting up yorick (2.2.04+dfsg1-14build1)…
Setting up yorick-z (1.2.0+cvs20080115-6build1)…
Setting up rlwrap (0.47.1-0.1)…
update-alternatives: using /usr/bin/rlwrap to provide /usr/bin/readline-editor (
readline-editor) in auto mode
Processing triggers for libc-bin (2.43-2ubuntu2)…
Processing triggers for man-db (2.13.1-1build1)…
Processing triggers for install-info (7.2-5ubuntu2)…
reyne@reyne-VirtualBox:~/reyne/workspace/reports/lab01$ 
```
# Отчёт по дз:

```

```
