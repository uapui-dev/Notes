
1. 预安装

sudo yum install python-devel
CentOS6 编译与安装HUE3.6

0. Download HUE 3.6

 wget https://github.com/cloudera/hue/archive/cdh5.1.0-release.tar.gz


1. 预安装

* sudo yum install python-devel

* maven

* sudo yum install gcc

* sudo yum install gcc-c++

* sudo yum install krb5-devel

>>
Dependencies Resolved

==================================================================================================================
 Package                          Arch                Version                          Repository            Size
==================================================================================================================
Installing:
 krb5-devel                       x86_64              1.10.3-15.el6_5.1                updates              495 k
Installing for dependencies:
 keyutils-libs-devel              x86_64              1.4-4.el6                        base                  28 k
 libcom_err-devel                 x86_64              1.41.12-18.el6                   base                  32 k
 libselinux-devel                 x86_64              2.0.94-5.3.el6_4.1               base                 136 k
 libsepol-devel                   x86_64              2.0.41-4.el6                     base                  64 k


* sudo yum install libxml2-devel

* sudo yum install libxslt-devel

* sudo yum install mysql-devel



* sudo yum install sqlite-devel

* sudo yum install  openldap-devel

==================================================================================================================
 Package                        Arch                 Version                          Repository             Size
==================================================================================================================
Installing:
 openldap-devel                 x86_64               2.4.23-34.el6_5.1                updates               1.1 M
Installing for dependencies:
 cyrus-sasl-devel               x86_64               2.1.23-13.el6_3.1                base                  302 k






http://mvnrepository.com/artifact/org.apache.hadoop/hadoop-common/2.4.0



sudo yum install asciidoc  （否则doc编译不同过，a2x）

=========================================================================================================================================================================
 Package                                        Arch                                Version                                      Repository                         Size
 =========================================================================================================================================================================
 Installing:
  asciidoc                                       noarch                              8.4.5-4.1.el6                                base                              183 k
  Installing for dependencies:
   docbook-dtds                                   noarch                              1.0-51.el6                                   base                              274 k
    docbook-style-xsl                              noarch                              1.75.2-6.el6                                 base                              2.6 M
     sgml-common                                    noarch                              0.6.3-32.el6                                 base                               43 k



2. 删除文件(remove files which need hadoop mr1)

rm /home/azureuser/workspace/hue/hue-release-3.6.0/desktop/libs/hadoop/java/src/main/java/org/apache/hadoop/mapred/ThriftJobTrackerPlugin.java

rm desktop/libs/hadoop/java/src/main/java/org/apache/hadoop/thriftfs/ThriftJobTrackerPlugin.java



 /home/azureuser/workspace/hue/hue-release-3.6.0/build/env/bin/python2.6 /home/azureuser/workspace/hue/hue-release-3.6.0/build/env/bin/easy_install -f http://archive.cloudera.com/desktop-sdk-python-packages/    -H archive.cloudera.com -qq ipdb
