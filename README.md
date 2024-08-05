# MP4_recovery
MP4 Recovery

Navigate to folder in command prompt (does not have to be admin)

Add good uncorrupted file shot on same camera to folder that contains the above files

run 
```
recover_mp4 uncorrupted_file --analyze
```
replace "uncorrupted_file" with filename

next run
```
recover_mp4.exe corrupted_file result.h264 result.wav --qt --pcmfix 3F9
```
replace "corrupted_file" with filename

lastly run to convert to .MOV
```
ffmpeg.exe -r 30000/1001 -i result.h264 -i result.wav -c:v copy -c:a adpcm_ima_wav result.mov
```
