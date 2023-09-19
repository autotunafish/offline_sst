# offline_sst
repo of files pertaining to realtime, offline translations using whisper realtime and argos translate. This repo is marked Creative Commons CC0. https://creativecommons.org/share-your-work/public-domain/cc0/

How it works: Whisper realtime produces text output which is piped into a watched file. A script watches this file and its triggering writes the output text into an executable command for Argos Translate. This executable is run and its output (translation) is echoed onto the terminal.

https://github.com/davabase/whisper_real_time
https://github.com/argosopentech/argos-translate
