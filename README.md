# Noita Together - Linux Tipsheet
Tips / Tricks / Workarounds to get Noita Together working on Linux

**How do I run the AppImage? App just opens and closes.**  
Make sure the AppImage is set permissions-wise to be executable. 
Also, it often needs to be run with a sandbox-disabling flag like --no-sandbox, --disable-gpu-sandbox, or --in-process-gpu.
I would use --no-sandbox before trying anything else
For example:
``` 
user@computer:~/Applications$ sudo ./Noita-Together-Setup-0.10.8.AppImage --no-sandbox
```

**NT doesn't download all the necessary files. It starts out fine but slows down, and often fails or stalls and sits at a particular file, for instance, files/entities/sampo/disabled_sampo.xml. The continue button is unclickable because not all files have downloaded yet**
Sometimes re-opening the app can help it along, but the only sure-fire way I've seen it finish successfully is to make sure the NT window is in focus, and then press CTRL+R. This "refreshes" the NT window and seems to help it download additional files. You can do this CTRL+R refresh as many times as necessary (each time it stalls) to ensure it gets through all the files. The continue button will become available to click once it is done.

**I've downloaded all the files, continued, and now when I click "Login to Twitch.tv" nothing happens but a spinning loading circle on the purple button**
For some reason the app sometimes has a problem launching a browser window. A workaround for this is to first, click the button if you haven't already (make sure the loading indicator is spinning), THEN, visit ```https://noitatogether.com/api/auth/login``` in your browser manually afterwards. Bookmark this URL to streamline this process if you want later.
