rpm-python27
============

RPM spec file build and alternative Python 2.7.x install for CentOS


Build steps...

(1) sudo yum -y install rpmdevtools && rpmdev-setuptree

(2) sudo yum -y install tk-devel tcl-devel expat-devel db4-devel gdbm-devel sqlite-devel bzip2-devel openssl-devel ncurses-devel readline-devel

(3) wget https://raw.github.com/bmacauley/rpm-python27/master/python27.spec -O ~/rpmbuild/SPECS/python27.spec

(4) wget http://www.python.org/ftp/python/2.7.6/Python-2.7.6.tgz -O ~/rpmbuild/SOURCES/Python-2.7.6.tgz

(5) QA_RPATHS=$[ 0x0001|0x0010 ] rpmbuild -bb ~/rpmbuild/SPECS/python27.spec