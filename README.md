#### Mame: Global Leaderboard patch

This is a patch for mame to transmit hiscores to a global leaderboard. The hiscores will be transmitted as soon as you leave mame or switch between games. This basically happens directly after the hi file for the game has been written.

##### Installation
1. Obtain the main sources from the [mamedev website](http://www.mamedev.org/release.html) use the most current version. I started this patch with mame version 0151. I am planning on updating this patch as soon as a new version of mame (and hiscore patch) is available. However, I have no intend to backport this patch to previous versions. If you need it for a previous version, feel free to request it with a good reason why you need that version.
2. Obtain and apply the [hiscore patch](http://forum.arcadecontrols.com/index.php?topic=64298.0). Download the apropriate patch for your mame version.
3. Apply Global Leaderboard patch from this repository. Make sure you choose the appropriate patch for your mame version. Copy the patch to your mame directory and apply the patch.

   ```patch -p1 -E --binary < global_leaderboard.diff```

4. Compile mame as you normaly would.

##### Settings
The global Leaderboard patch comes with three settings. But the only one you **need** to set the API Key. This settings need to be done in your mame.ini

* **global_leaderboard_api_key** This is your API Key for the global Leaderboard (default=default).
* **global_leaderboard_url** This is the URL to the global Leaderboard. You most likely do not want to change this, except you want to run your own leaderboard (default=localhost).
* **disable_global_leaderboard_patch** You can set this option to 1 if you want to stop transmitting your scores to the global leaderboard (default=1).
