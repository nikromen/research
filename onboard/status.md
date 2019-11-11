## Onboarded:
* ansible-bender
* blivet-gui
* conu
* dnf
* fmf
* libdnf
* osbuild
* packit
* pycharm-community-edition
* python-avocado
* python-deprecated
* python-dockerfile-parse
* python-ogr
* rear
* rebase-helper
* tmt
* tmux-top

## In review(packit):
* chkconfig - https://github.com/fedora-sysv/chkconfig/pull/25
* conman - https://github.com/dun/conman/pull/33
* cronie - https://github.com/cronie-crond/cronie/pull/47
* Cython - https://github.com/cython/cython/pull/3229
* initscripts - https://github.com/fedora-sysv/initscripts/pull/292
* initial-setup - https://github.com/rhinstaller/initial-setup/pull/79
* jansi-native - https://github.com/fusesource/jansi-native/pull/22
* libica - https://github.com/opencryptoki/libica/pull/33
* jose - https://github.com/latchset/jose/pull/71
* mod_security_crs - https://github.com/SpiderLabs/owasp-modsecurity-crs/pull/1621
* numactl - https://github.com/numactl/numactl/pull/83
* openssl-ibmca - https://github.com/opencryptoki/openssl-ibmca/pull/60
* python-meh - https://github.com/rhinstaller/python-meh/pull/21
* python-paramiko - https://github.com/paramiko/paramiko/pull/1549
* python-pillow - https://github.com/python-pillow/Pillow/pull/4206
* python-simpleline - https://github.com/rhinstaller/python-simpleline/pull/62
* python-urlgrabber - https://github.com/rpm-software-management/urlgrabber/pull/22
* rpmdeplint - https://github.com/default-to-open/rpmdeplint/pull/1
* scap-security-guide - https://github.com/ComplianceAsCode/content/pull/5000
* scap-workbench - https://github.com/OpenSCAP/scap-workbench/pull/236
* sos - https://github.com/sosreport/sos/pull/1853
* tang - https://github.com/latchset/tang/pull/39
* tuned - https://github.com/redhat-performance/tuned/pull/205

## In review(copr):
* cockpit-ostree - https://github.com/cockpit-project/cockpit-ostree/pull/31
* cockpit-podman - https://github.com/cockpit-project/cockpit-podman/pull/235
* sen - https://github.com/TomasTomecek/sen/pull/150

## Onboarded without copr builds
* nss-pem

## Blocked:
### Package not found
* cockpit-container
* redminecli

### Upstream not found
* anaconda-user-help

### Source in pagure
* standard-test-roles

### multiple sources or patches in spec
* avahi
* jzlib
* ksh
* libvncserver
* openscap
* pykickstart - has invalid packit.yml right now (spec.in in specfile path)
* python-requests
* rust-pretty-git-prompt - has packit config
* system-config-printer
* yp-tools

## Needs action for spec generate:
* anaconda - how is it built?
* abrt
* libreport
* cockpit - spec parse fails
* cockpit-composer - npm fails
* rpminspect - instructions for creating .spec?
* satyr

## Other error
* expat - unclosed macro or bad line continuation
* javapackages-tools - unclosed macro or bad line continuation
* gperftools - Failed to parse SPEC file
* abrt-java-connector - The target archive doesn't use a common extension
* libevent - The target archive doesn't use a common extension

## Rejected
* python-requests-file
  * increased maintanance cost by having .packit.yml file in repo
  * More info: https://github.com/dashea/requests-file/pull/14
* pyparted
  * increased maintanance cost by having .packit.yml file in repo
  * https://github.com/packit-service/packit-service/issues/46
  * https://github.com/packit-service/packit/issues/540
  * More info: https://github.com/dcantrell/pyparted/pull/66
* lorax
  * automation for Fedora and COPR should not depend on upstream changes
   or carrying your config file in our repositories.
  * More info: https://github.com/weldr/lorax/pull/878
* checkpolicy - https://github.com/SELinuxProject/selinux/pull/186
  * related also to **libsepol, libselinux, libsemanage, policycoreutils, secilc, mcstrans**
  * multiple components and multiple tarballs from one repository
  * the packages from the repo depend on each other (have to be taken care of/built in a specific order)
  * changes have potential to be accepted only on fedora fork
  https://github.com/fedora-selinux/selinux, changes on
  upstream need to be approved via mailing list
  * lack of trust caused by failed cooperation with other always ready project