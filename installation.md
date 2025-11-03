# Installation

## Requirements

* Velocity 3.2 or newer
* Java 17 or newer
* Optional: LuckPerms for queue priority integration

## Installation Steps

{% stepper %}
{% step %}
### Download the plugin

Download the latest `QueuePlus.jar`.
{% endstep %}

{% step %}
### Install the plugin

Place it in your Velocity `plugins/` directory.
{% endstep %}

{% step %}
### Start the proxy once

Start the proxy once — this generates the configuration folder:

```
/plugins/Queue/
├─ config.toml
├─ devmodes.toml
```
{% endstep %}

{% step %}
### Configure

Edit `config.toml` to fit your setup (see the Configuration section).
{% endstep %}

{% step %}
### Reload configuration

Run the following in-game or in-console to reload the configuration at runtime:

```
/queuereload
```
{% endstep %}
{% endstepper %}

## Updating

When updating, always:

{% stepper %}
{% step %}
Stop the proxy.
{% endstep %}

{% step %}
Replace the old `.jar` with the new one.
{% endstep %}

{% step %}
Start Velocity again — your configuration and devmodes are preserved.
{% endstep %}
{% endstepper %}
