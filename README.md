# .babun-shell
Best shell for windows ever (zsh)

## IntelliJ IDEA

1. [install babun shel from home site]()
2. fix fons in idea console by setting propper env variable in your zsh
   ```
   echo "TERM=cygwin" >> ~/.zshrc
   ```
3. add idea integration:
   ```
   "C:/Users/maksim.kostromin/.babun/cygwin/bin/zsh.exe" -c '/bin/env CHERE_INVOKING=1 /bin/zsh.exe'
   ```
![idea -> settings -> Terminal](./idea.png)
<!--
Format: ![Alt Text](./idea.png)
Format: ![Alt Text](https://github.com/daggerok/.babun-shell/edit/master/idea.png)
-->

4. And lastly, maybe reboot the system... :)

## ConEmu

__setup__

Open ConEmu -> Settings -> Startup -> Tasks
Create a new task with

- parameters: `/icon "%userprofile%\.babun\cygwin\bin\mintty.exe" /dir "%userprofile%"`
- commands: `%userprofile%\.babun\cygwin\bin\mintty.exe /bin/env CHERE_INVOKING=1 /bin/zsh.exe`

in my case it was like so:

![ConEmu -> Settings -> Startup -> Tasks](./ConEmu-1.png)

and finnaly, __set babun as default one on ConEmu start__:

![ConEmu -> Settings -> Startup](./ConEmu-2.png)

read [official babun guide: 12) How do I integrate Babun with ConEmu / cmder](http://babun.github.io/faq.html)
