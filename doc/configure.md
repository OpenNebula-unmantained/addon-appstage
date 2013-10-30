# Configuring AppStage

The AppStage command interacts directly with OpenNebula, it does not require to start other service. There are, however, some customization options.


## ACL Rule

You need to decide which OpenNebula users will be able to use AppStage, and create an ACL Rule to allow them to create Documents.

To enable AppStage for all users, add the rule:

~~~~
$ oneacl create "* DOCUMENT/* CREATE"
~~~~

If you only want a specific group to be able to use AppStage, execute:

~~~~
$ oneacl create "@1 DOCUMENT/* CREATE"
~~~~

Read more about the ACL Rules system in the [OpenNebula documentation](http://opennebula.org/documentation:documentation:manage_acl).


## Enable the Sunstone Tabs

The AppStage Sunstone plugins are enabled by default. They can be enabled for everyone, or only for a list of group or users. Read more about the configuration options in the [OpenNebula documentation](http://opennebula.org/documentation:documentation:sunstone_plugin_guide).

To disable or filter which users can use the plugins, edit `/etc/one/sunstone-plugins.yaml`, and look for the plugins `apptools.appstage*`.

~~~~ yaml
- user-plugins/apptools.appstage-dashboard.js: 
    :group: 
    :ALL: true
    :user: 
- user-plugins/apptools.appstage.js: 
    :group: 
    :ALL: true
    :user: 
~~~~

Be sure to restart Sunstone for the changes to take effect.
