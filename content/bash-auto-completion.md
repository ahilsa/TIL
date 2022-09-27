Title: Bash Auto-Completion Overriding
Tags: bash

Background: I was working with WSL (Windows Subsystem Linux) and used `alias java=java.exe` to use the already installed jdk in Windows. When using the alias `java` tab-completion was not working as expected whereas for `java.exe` it was. 

I discovered `/usr/share/bash-completion/` where bash stores convenient auto-completion rules for different commands. So it turns out that the command `java` had pre-defined rules `/usr/share/bash-completion/completions/java`.

I overrode the above by adding `complete -o default java` to my `.bashrc`. 

Bonus: Another learning I can take away is to not use common command names as alias names.
