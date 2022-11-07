
## System requirements:

Ubuntu 20.04

## Will it work on Windows?

No. 


## How to execute:


```
git clone https://github.com/elaa0505/Tamilvoice.git

cd Tamilvoice

```

Edit the file, install.sh

Fill the following details.

DOWNLOAD_PATH=/home/yourpath~/packages  #to download the required packages

COMPILE_PATH=/home/yourpath~/compiled   # to place the compiled files and folders


Register here http://htk.eng.cam.ac.uk/download.shtml and get a username and password

HTKUSER=username

HTKPASSWORD=password


Then, execute the file as

```
bash install.sh

```


## How to convert a text to audio?

```
export FESTDIR=/usr


cd COMPILE_PATH
ssn_hts_demo/scripts/complete “தமிழ் வாழ்க” linux

```


This will convert the text and store as wav in

```
ssn_hts_demo/wav/1.wav

```

you can play it with any audio player.



## How to convert a full text file to audio?

Prepare the tamil text content as a text file. Save it as ".txt" extension.

open the file convert-file-to-audio.py, with any text editor and replace the following two parapeters with suitable folders.

ssn_demo_path = "/home/~yourpath~/ssn_hts_demo"

mp3_out_path = "/home/~yourpath~/test"


Then execute the below command

```
python text2audio.py <filename.txt>
```

This will make mp3 file and store in the folder mp3_out_path/filename-timestamp
