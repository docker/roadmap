---
name: Feature request
about: Read /etc/sysctl.conf when starting Docker-Desktop in WSL
title: '[Feature request] Read /etc/sysctl.conf when starting Docker-Desktop in WSL'
labels: community_new, Docker-Desktop
assignees: ''

---

**Tell us about your request**
WSL does not automatically read sysctl.conf on startup.
A service in a docker container might depend on a parameter set in sysctl.conf.
Please have Docker-Desktop read and accordingly process sysctl.conf on startup.

**Which service(s) is this request for?**
Docker-Desktop for windows

**Tell us about the problem you're trying to solve. What are you trying to do, and why is it hard?**
https://stackoverflow.com/q/69214301/10071239

**Are you currently working around the issue?**
https://stackoverflow.com/a/69294687/10071239
Adding an according line, e. g. below, to .bashrc makes a workaround:

wsl.exe -d docker-desktop sh -c "sysctl -w vm.max_map_count=262144"

**Additional context**
