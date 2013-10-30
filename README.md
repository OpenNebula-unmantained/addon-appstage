# AppStage

## Description

AppStage performs the automatic installation and configuration of the software stack that constitutes an application environment. With AppStage you can easily define software configurations for your virtual machines and share them with other users.

Installing and configuring applications is a laborious task. Nowadays, there are several Configuration Management tools like [chef](http://www.opscode.com/chef/), [puppet](http://puppetlabs.com/puppet/what-is-puppet/) or [cfengine](http://cfengine.com/) that allow to script the installation and configuration of applications and services.

AppStage helps you to integrate these tools and automation processes with an OpenNebula IaaS cloud, by:

* Managing software stacks configurations (environment). So cloud users can instantiate an environment rather than just a VM.
* Providing the required scripting glue to seamlessly integrate chef with the powerful OpenNebula's contextualization process.

AppStage uses [chef-solo](http://wiki.opscode.com/display/chef/Chef+Solo) to power the automatic installation and configuration of the app software stack.

## Development

To contribute bug patches or new features, you can use the github Pull Request model. It is assumed that code and documentation are contributed under the Apache License 2.0. 

More info:
* [How to Contribute](http://opennebula.org/software:add-ons#how_to_contribute_to_an_existing_add-on)
* Support: [OpenNebula user mailing list](http://opennebula.org/community:mailinglists)
* Development: [OpenNebula developers mailing list](http://opennebula.org/community:mailinglists)
* Issues Tracking: [Github issues](https://github.com/OpenNebula/addon-appstage/issues)

## Authors

* Leader: Javier Fontán (jfontan@opennebula.org)

## Compatibility

This add-on is compatible with OpenNebula 3.8.

## Features

* Automatic installation and configuration of software stacks
* Simplify the process of building new applications
* Provide configurable application environments from a catalog and self-service portal
* Enable tight, efficient administrative control
* Fine-grained access control for the secure sharing of application environments with other users

## Limitations

This version only supports Chef.

## Requirements

* OpenNebula 3.8
* Chef solo in the VMs
* Contextualization packages in the VMs

## Installation

## Configuration

## Usage

## References

* [chef-solo](http://wiki.opscode.com/display/chef/Chef+Solo)

## License

Apache v2.0 license.
