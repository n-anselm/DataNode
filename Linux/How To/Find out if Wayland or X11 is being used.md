### Wayland or X11
Obtain the session ID to pass in by issuing:

	loginctl

Then run:

	loginctl show-session <SESSION_ID> -p Type

If you want it all in one command:

	loginctl show-session $(awk '/tty/ {print $1}' <(loginctl)) -p Type | awk -F= '{print $2}'

Another way (doesn't always work)

	echo $XDG_SESSION_TYPE
