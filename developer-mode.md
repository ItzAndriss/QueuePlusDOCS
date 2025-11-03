# Developer mode

Developer Mode is designed for testing or maintenance periods.\
When active, only players with the correct permission can join a target server.

## Usage

```bash
/queuedev <server> on
```

Only players with:

```
queue.dev.<server>
```

may connect.

Use:

```bash
/queuedev <server> off
```

to disable it again.

## Persistence

Developer mode states are saved to `plugins/Queue/devmodes.toml`.\
These persist across proxy restarts.

## Example Workflow

{% stepper %}
{% step %}
### Enable developer mode before updating

```bash
/queuedev survival on
```
{% endstep %}

{% step %}
### Restart the backend server
{% endstep %}

{% step %}
### Test your changes safely — only devs can join
{% endstep %}

{% step %}
### Disable developer mode afterward

```bash
/queuedev survival off
```
{% endstep %}
{% endstepper %}
