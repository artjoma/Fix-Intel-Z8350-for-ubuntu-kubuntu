# Fix Intel Z8350 for ubuntu/kubuntu 18

# Fix WI-FI:
* wget https://github.com/artjoma/Fix-Intel-Z8350-for-ubuntu-kubuntu/blob/master/nvram.txt <br/>
* sudo cp nvram.txt /lib/firmware/brcm/brcmfmac43455-sdio.txt

# Fix audio (no audio device)
* try find audio out using: speaker-test -c 2 -r 48000 -D hw:0,2
* or 
* speaker-test -c 2 -r 48000 -D hw:0,1

* after edit config for pulse audio
* sudo nano /etc/pulse/default.pa
* edit section: load-module module-alsa-sink device=hw:0,2
* save
* reboot
