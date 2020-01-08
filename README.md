Hi!!

-StreamingKit (formally Audjustable) is an audio playback and streaming library for iOS and Mac OSX. 
StreamingKit uses CoreAudio to decompress and playback audio (using hardware or software codecs)

whilst providing a clean and simple object-oriented API.
The primary motivation of this project was to decouple the input data sources from the actual player logic 
in order to allow advanced customizable input handling such as HTTP progressive download based streaming, 
encryption/decryption, auto-recovery, dynamic-buffering. StreamingKit is the only streaming and playback library 
that supports dead-easy gapless playback between audio files of differing formats.

-Installation
StreamingKit is available as a Cocoapod. You can also simply copy all the source files located inside StreamingKit/StreamingKit/* into your Xcode project.

Main Features
Free OSS.
Simple API.
Easy to read source.
Carefully multi-threaded to provide a responsive API that won't block your UI thread nor starve the audio buffers.
Buffered and gapless playback between all format types.
Easy to implement audio data sources (Local, HTTP, AutoRecoveringHTTP DataSources are provided).
Easy to extend DataSource to support adaptive buffering, encryption, etc.
Optimised for low CPU/battery usage (0% - 1% CPU usage when streaming).
Optimised for linear data sources. Random access sources are required only for seeking.
StreamingKit 0.2.0 uses the AudioUnit API rather than the slower AudioQueues API which allows real-time interception of the raw PCM data for features such as level metering, EQ, etc.
Power metering
Inbuilt equalizer/EQ (iOS 5.0 and above, OSX 10.9 Mavericks and above) with support for dynamically changing/enabling/disabling EQ while playing.
Example apps for iOS and Mac OSX provided.
-Usage
There are two main classes. The STKDataSource class which is the abstract base class for the various compressed audio data sources. The STKAudioPlayer class manages and renders audio from a queue DataSources. By default STKAudioPlayer will automatically parse URLs and create the appropriate data source internally.

-[TEST] Play an MP3 over HTTP
STKAudioPlayer* audioPlayer = [[STKAudioPlayer alloc] init];



private network info(connection info)
[audioPlayer play:@"host:"xhttp://82.221.139.233/main/", port: 8080"];
[audioPlayer play:@"host:"xhttp://82.221.139.233/main/", port: 8080"];
[audioPlayer play:@"host:"xhttp://82.221.139.233/main/", port: 8080"];
Gapless playback
STKAudioPlayer* audioPlayer = [[STKAudioPlayer alloc] init];

[audioPlayer queue:@"http://www.com2commn.com/files/sample.mp3"];
[audioPlayer queue:@"http://www.com2commn.com/files/sample2.aac"];



-More
More documentation is available on the project Wiki

-Authors and Contributors
Copyright (c) 2012-2019.12, Thong Nguyen
