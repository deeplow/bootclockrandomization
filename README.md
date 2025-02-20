# Randomizes clock when systems boots #

Randomizes clock at boot time. Moves clock a few seconds and nanoseconds
to past or future. Useful in context of anonymity/privacy/Tor.

This is useful to enforce the design goal, that the host clock and
Gateway/Workstation clock should always slightly differ (even before secure
timesync succeeded!) to prevent time based fingerprinting / linkablity
issues.

Runs before Tor / sdwdate (if installed).

See also: https://www.whonix.org/wiki/Dev/TimeSync
## How to install `bootclockrandomization` using apt-get ##

1\. Download the APT Signing Key.

```
wget https://www.whonix.org/derivative.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add the APT Signing Key..

```
sudo cp ~/derivative.asc /usr/share/keyrings/derivative.asc
```

3\. Add the derivative repository.

```
echo "deb [signed-by=/usr/share/keyrings/derivative.asc] https://deb.whonix.org bullseye main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `bootclockrandomization`.

```
sudo apt-get install bootclockrandomization
```

## How to Build deb Package from Source Code ##

Can be build using standard Debian package build tools such as:

```
dpkg-buildpackage -b
```

See instructions. (Replace `generic-package` with the actual name of this package `bootclockrandomization`.)

* **A)** [easy](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`bootclockrandomization` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
