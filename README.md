![Introduction banner](intro-banner.png)

# MacOS-Security
Harden macOS

![Banner](banner.png)

<img src="assets-scene.svg" alt="Animated themed scene" width="100%">

> CONDITION NOTE: `privacy-script.sh` is a generated privacy.sexy script (v0.13.7). It runs as root: if you start it as a normal user, it starts itself again with administrator privileges and then runs to the end with no prompt, no dry run, and no backup step.

> BEFORE YOU RUN: If you need any of the items in the list above, copy them somewhere else before you run this file, or do not run it.

## Warning: read this before you run privacy-script.sh

`privacy-script.sh` is a generated privacy.sexy script (v0.13.7). It runs as root: if you start it as a normal user, it starts itself again with administrator privileges and then runs to the end with no prompt, no dry run, and no backup step.

Running it deletes or resets the following, and none of it can be undone from anything in this repo:

- Firefox saved password files: `logins.json`, `signons.txt`, `signons2.txt`, `signons3.txt`, and `signons.sqlite` in every Firefox profile. Saved Firefox passwords are gone after this runs.
- All iOS device backups stored on this Mac, under `~/Library/Application Support/MobileSync/Backup/`.
- System logs, including everything under `/private/var/log/`.
- Shell histories for your account, the history files your terminal sessions are saved in.
- Browser histories and cookies, for the browsers the script covers, including Chrome, Safari, and Firefox history, cache, cookies, and download history.
- Every TCC permission grant on the machine. TCC is the system database that records which apps you allowed to use the camera, the microphone, accessibility, screen capture, and the other protected services the script resets, one by one. After this runs, every one of those allow decisions is wiped and apps have to ask again.

The script also clears caches, the Trash, printer job caches, and developer caches, turns several system services off, and turns Spotlight indexing off near the end.

If you need any of the items in the list above, copy them somewhere else before you run this file, or do not run it. I published the script as generated, with its sections labeled in the file itself. This warning is the part the file cannot give you before it starts: by the time a section name prints, that section is already running.
