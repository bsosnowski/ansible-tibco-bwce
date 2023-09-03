# Crete TIBCO BWCE development machine
Ansible playbook for creation of TIBCO BWCE development machine

## Constrains
Supported operating systems:
- RHEL family (Rocky, Alma, Fedora, etc)

Supported processor architectures:
- x64

Artifact repository structure should follow below convention:
```.
├── bwce
│   └── ${version}
│       └── linux
│           ├── TIB_bwce_${version}_linux26gl23_x86_64.zip
│           ├── product_tibco_eclipse_lgpl_${lgpl-version}_linux26gl25_x86_64.zip
├── bwplugin-${plugin-name}
│   └── ${plugin-version}
│       └── linux
│           ├── TIB_bwplugin-${plugin-name}_${plugin-version}_linux_x86_64.zip
```


## Environment setup
Playbook will create user and group dedicated for TIBCO.

## Installed components
- `sdkman` for installation of Java, Maven and Gradle (other tools can be added)
- `libnsl` library required on RHEL OS family
- `lgpl` Oracle Elliptic Curve Cryptography (ECC) - LGPL Assemblies
- `bwce` TIBCO BWCE
