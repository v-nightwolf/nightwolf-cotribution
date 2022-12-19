# Package Management (yum vs apt): 
---
Redhat and Ubuntu OS families have different package management tools like yum and apt. As an Administrator, we need to have the commands ready for any package mgmt related work for both the OS families. We have outlined few commands which comes handy in such scenarios. 


---

## General Packaging System Information

|                 |   Redhat Family(yum)              | Ubuntu(apt)                       |
|---------------------|-----------------------------------|-----------------------------------|
| Package file extension| *.rpm | *.deb|
|Repository location configuration| /etc/yum.conf OR /etc/yum.repos.d/| /etc/apt/sources.list|

---
<br>

## Adding, Removing and Upgrading Package

|Task                 |   Redhat Family(yum)              | Ubuntu(apt)                       |
|---------------------|-----------------------------------|-----------------------------------|
|Refresh list of available packages| Yum refreshes each time it's used| apt-get update        |
|Install a package from a repository | yum install package_name| apt-get install package_name |
|Install a package file | yum install package.rpm OR rpm -i package.rpm| dpkg --install package.deb|
|Remove a package| rpm -e package_name | apt-get remove package_name |
|Remove a package with configuration files| yum remove package_name | apt-get purge package_name |
|Check for package upgrades|yum check-update |apt-get -s upgrade OR apt-get -s dist-upgrade |
|Upgrade packages | yum update OR rpm -Uvh [args]| apt-get upgrade|
|Upgrade the entire system|yum upgrade| apt-get dist-upgrade|


---
<br>

## Package Information


|Task                 |   Redhat Family(yum)              | Ubuntu(apt)                       |
|---------------------|-----------------------------------|-----------------------------------|
| Get information about an available package| yum search package_name| apt-cache search package_name|
|Show available packages|yum list available|apt-cache dumpavail|
|List all installed packages|yum list installed OR rpm -qa|dpkg --list|
|Get information about a package|yum info package_name|apt-cache show package_name|
|Get information about an installed package|rpm -qi package_name|dpkg --status package_name|
|List files in an installed package|rpm -ql package_name|dpkg --listfiles package_name|
|List configuration files in an installed package|rpm -qc package_name|dpkg-query --show -f '${Conffiles}\n' package_name|
|Show the packages a given package depends on|rpm -qR package_name|apt-cache depends|
|Show other packages that depend on a given package (reverse dependency)|rpm -q --whatrequires [args]|apt-cache rdepends|


---
<br>

## Misc. Packaging System Tools 

|Task                 |   Redhat Family(yum)              | Ubuntu(apt)                       |
|---------------------|-----------------------------------|-----------------------------------| 
|Show stats about the package cache | -  | apt-cache stats |
|Verify all installed packages |rpm -Va | debsums|
|Remove packages from the local cache directory |yum clean package | apt-get clean |
|Remove only obsolete packages from the local cache directory | -  |apt-get autoclean |
|Remove header files from the local cache directory (forcing a new download of same on next use) |yum clean headers |apt-file purge |

---
<br>

## Package File Information

|Task                 |   Redhat Family(yum)              | Ubuntu(apt)                       |
|---------------------|-----------------------------------|-----------------------------------|
|Get information about a package file |rpm -qpi package.rpm |dpkg --info package.deb |
|List files in a package file |rpm -qpl package.rpm |dpkg --contents package.deb |
|List documentation files in a package file |rpm -qpd package.rpm | - |
|List configuration files in a package file |rpm -qpc package.rpm | - |
|Extract files in a package |rpm2cpio package.rpm | cpio -vid |dpkg-deb --extract package.deb dir-to-extract-to |
| Find package that installed a file|rpm -qf filename |dpkg --search filename |
|Find package that provides a particular file |yum provides filename |apt-file search filename |

