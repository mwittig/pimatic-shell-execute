pimatic shell execute plugin
=======================
This plugin let you define devices that execute shell commands. Additonal it allowes you
to execute shell commands in rule actions. So you can define rules of the form:

    if ... then execute "some command"

Configuration
-------------
You can load the plugin by editing your `config.json` to include:

    { 
       "plugin": "shell-execute"
    }


Devices can be defined by adding them to the `devices` section in the config file.
Set the `class` attribute to `ShellSwitch`. For example:

    { 
      "id": "light",
      "name": "Lamp",
      "class": "ShellSwitch", 
      "onCommand": "echo on",
      "offCommand": "echo off"
    }

For device configuration options see the [device-config-schema](device-config-schema.html) file.