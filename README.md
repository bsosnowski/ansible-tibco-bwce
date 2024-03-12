# Create TIBCO BWCE development machine
Ansible playbook for creation of [TIBCO BusinessWorks™ Container Edition](https://docs.tibco.com/products/tibco-businessworks-container-edition-2-8-3) development machine.

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

## Installed roles
- `sdkman` for installation of Java, Maven and Gradle (other tools can be added). More information: [sdkman.io](https://sdkman.io/)
- `libnsl` library required on RHEL OS family
- `bwce` TIBCO BWCE
- `plugins` TIBCO BWCE plugins

## How-to
### Configure list of target machines
Modify hosts file here: [hosts](./inventories/production/hosts)

### Configure TIBCO settings
In order to set BWCE, Java, Maven versions, installation directories and a list of plugins - modify settings here: [tibco.yml](./inventories/production/group_vars/tibco.yml)

## How to open Business Studio
This Playbook will install Business Studio shortcut:

![business-studio-icon](./imgs/business-studio-icon.png)