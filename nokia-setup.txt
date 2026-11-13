echo MOOSSETUP-BEGIN
getprop ro.product.model; getprop ro.product.device; getprop ro.build.fingerprint
getprop ro.build.version.sdk; getprop ro.vndk.version; getprop ro.vendor.build.version.sdk; getprop ro.treble.enabled; getprop ro.boot.slot_suffix; getprop ro.build.ab_update; uname -r
ls /dev/block/by-name; su -c 'ls /dev/block/by-name'
mkdir -p ~/.ssh && echo 'ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIBQKOl7uN4K8fIP66Kmz9h3JTy8hAAwQpIf/lOxKmx59 hatch' > ~/.ssh/authorized_keys && chmod 700 ~/.ssh && chmod 600 ~/.ssh/authorized_keys && echo KEY-OK
pkill sshd; sleep 1; sshd; sleep 1; ps -ef | grep sshd | grep -v grep; echo SSHD-DONE
whoami; ip addr show wlan0 | grep inet
echo MOOSSETUP-END
