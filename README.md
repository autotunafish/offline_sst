# offline_sst
repo of files pertaining to realtime, offline translations using whisper realtime and argos translate. This repo is marked Creative Commons CC0. https://creativecommons.org/share-your-work/public-domain/cc0/

How it works: Whisper realtime produces text output which is piped into a watched file. A script watches this file and its triggering writes the output text into an executable command for Argos Translate. This executable is run and its output (translation) is echoed onto the terminal.

https://www.youtube.com/watch?v=gLVprfZREkI

Whisper real-time and Argos translate also work on Win and Mac but the tool 'inotifywait' is used for communication from one program to the other and is Linux specific. There are equivalent tools in those other operating systems but are not covered here. This is a work in progress.

# Install dependencies
Anaconda3
portaudio19-dev
ffmpeg
setuptools-rust
inotify-tools

# clone
github.com/autotunafish/offline_sst

# conda env
conda create -n name-me python=3.9
conda activate name-me

# build
cd offline_sst
pip install -r requirements.txt

# check run
python transcribe_demo.py --model tiny 

- ctrl-C to stop

# In a new terminal, Home, base env
pip install argostranslate
argospm update
argospm install translate

# Add executable permissions to the scripts and receivingexec4.txt
# Adjust the filepaths (Sorry!)

# in Home, base, run the script
./espres_o

# in name-me, run
python transcribe_demo.py --model tiny 2>&1 | tee -a testing.txt

# Check out
https://github.com/davabase/whisper_real_time
https://github.com/argosopentech/argos-translate

Update: added line to print the translation with line breaks, much nicer.
