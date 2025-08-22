Open whisper.android folder in Android Stuido.
	Must open this folder or else the proper gradle files and environment variables won't be found.

Point Android project to Android SDK path (if required)
	- 1.) Set the sdk_dir parameter in the local.properties file
	- 2.) Export the ANDROID_HOME environment variable to your .bashrc

Downlolad whisper models from: https://huggingface.co/ggerganov/whisper.cpp/tree/main

Transfer to device via Android Studio
	NOTE: Do not use Studio's Device Explorer tool for this.
	In Studio, click the "Android" button at the top left window and change to "Project" mode.
	Navigate to: ~./whisper.android/app/src/main
	Create a new directory called: /assets
	Then create two sub-directories called: /models and /samples
	Then open a terminal to copy the whisper model (.bin) and audio sample (.wav, .mp3, etc.) into their associated directory.
		
		sudo cp /Users/.../Documents/models/ggml-small.bin 
		/Users/.../whisper.cpp/examples/whisper.android/app/src/main/assets/models
		
		sudo cp /Users/.../Downloads/samples_wav_blizzard_biased_sample-0.wav 
		/Users/.../whisper.cpp/examples/whisper.android/app/src/main/assets/samples
		
	

