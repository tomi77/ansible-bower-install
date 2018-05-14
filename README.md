# ansible-bower
A Ansible role to install Bower packages

## Parameters

| Name             | Default                   | Description |
| ---------------- | ------------------------- | ----------- |
| bower_executable | ./node_modules/.bin/bower | Location of a `bower` command |
| pkg              |                           | Package(s) to install. If omit, install from `bower.json` |
| chdir            | .                         | Location of a project |

## Examples

~~~yaml
# Install all from bower.json
- tomi77.bower-install

# Install using global bower
- role: tomi77.bower-install
  executable: bower

# Install lodash package
- role: tomi77.bower-install
  pkg: lodash

# Specify project location
- role: tomi77.bower-install
  chdir: /location/of/a/project
~~~
