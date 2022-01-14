# mini-backup
A small command line tool that uses ssh and scp to be able to backup files with remote storage.

# mini-backup
A mini application for creating home backups.


## Background
I backup a lot of my own data, including photos, music, and films. For this, I have a couple harddrives. I always make sure to have atleast 2 backups of each file and 3 backups if the file is important. I have to do this manually by individually plugging external drives into my laptop and copying the files over. This is pretty annoying, and so this project is meant to address this.

The idea is to have a Raspberry Pi with my external drives plugged into it. Running on the Pi will be mini server that listens for data pushes and will copy pushed data onto multiple drives automatically. This should be accessible from any computer on my network. On my computers, I'll run a client application that interfaces with the Pi. With that application I can push files to the Pi, specify how many backups I want, and receive information like drive capacities, when drives go down, or anything else I might need to know. 

To make this more user friendly, the server will recognize a few categories of file and know where to put those categories and onto how many drives to put them. This makes it simple to keep of track of where files are. The category is specified through the client's command line.

## Usage
