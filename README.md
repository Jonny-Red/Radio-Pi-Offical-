Pi Radio — an old-time radio station that runs itself

Pi Radio turns a Raspberry Pi (or any Linux PC) and a drive full of old-time radio shows into a real-sounding station. Shows start on the clock, the hour is rung, the news comes on, vintage commercials play between programs, and the day opens with a sign-on and closes with a sign-off — all on its own, around the clock.

Current version: v42 · Free and open source (MIT License) · Bring your own audio

What it does
Runs a broadcast day from your schedule — a daily lineup, or a different one for each day of the week
Keeps shows on the clock — an episode that has started always plays to its end, but the radio never starts one that would run into the next show; short gaps get music faded out right at the hour
Sounds like radio — hour chimes, news bulletins with a sting, 2–3 vintage ads between programs, station IDs, a daily sign-on and sign-off
Plays overnight — random shows or music after the last program, handing over to the morning show on time
Streams live to phones and PCs on your network (Icecast), tuned so phones don't cut out
Program Guide — a read-only "what's on now" page with a Listen button, which you can share online through a free Cloudflare link
Control from anywhere at home — a phone-friendly Control page, plus a desktop window on the Pi
Quick start
bash
# unzip the release, then from inside the folder (no sudo):
bash install.sh

Then:

Put your shows on a drive, one folder per show
Open the Control page (http://<your-pi>:8765/control) and point the radio at your shows folder
Set the day's start time and add shows to the schedule
Press Sign on

The full walkthrough is in SETUP_GUIDE.html (about 15 minutes). Every window and setting is covered in PI_RADIO_MANUAL.html.

Recommended drive layout

Any names and locations work — you point the radio at each folder once.

Your drive/
├── Shows/                 one folder per show (Dragnet, Gunsmoke, …)
├── Commercials/
├── News/
│   └── Intro/             optional news sting
├── Time Announcements/
├── Station IDs/
├── Station Sounds/        sign-on and sign-off
└── Gap Music/             optional short songs
Requirements
Raspberry Pi 4 or 5 (Raspberry Pi OS), or a PC with Linux Mint / Ubuntu
Python 3.9+, VLC, DarkIce and Icecast — the installer sets these up
Your own audio files (mp3, wav, ogg, flac, m4a, aac)
Documentation
File	What's in it
SETUP_GUIDE.html	Get on the air, add the station touches, listen and share
PI_RADIO_MANUAL.html	The full owner's manual, with screenshots
PI_RADIO_GUIDE.txt	The guide as plain text
CHANGES_v42.txt	What's new
Privacy

Your settings, backups and any Cloudflare token are kept in hidden files in your home folder (~/.pi_radio_*), never in the program folder. The included .gitignore keeps them out of the repository.

Personal use and license

Some features rely on third-party services that have their own terms and limits. Use them at your own risk and for personal use. You are solely responsible for the content you share and for following all applicable laws and service terms. Pi Radio ships with no audio.

Pi Radio is free software under the MIT License, provided "as is", without warranty of any kind. It uses other free programs (VLC, DarkIce, Icecast, cloudflared), which the installer gets from their usual sources under their own licenses.
