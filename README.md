***Data***
## Backyard Chicken Audio Dataset

### Preprocessing/youtube
Long audio of chickens in the backyard with noise such as cars and birds.
*Source*: Youtube poulty sounds with noise: https://www.youtube.com/watch?v=70IqKloH-mw

## Preprocessing Methods
The following libraries were used;
Noise Reduce and Bandpass Filter

--> First, install the following packages:
____________________
pip install librosa
pip install ffmpeg to enable audio read.
pip install noisereduce
import noisereduce as nr to reduce noise from the audio file.

**Next:** : first convert from mp3 to .wav

## Denoised Audio

Noisy Chicken audio: backyard_chickens_cut1.wav
Denoised Chicken audio using Band Filtering: bandpass-filter_backyard_chickens_cut1.wav 
Denoised Chicken audio using Noise Reduce: denoised_backyard_chickens_cut1.wav













<!-- animals_basel: cow sounds are divided into; cough sounds,Estrus call, food anticipating call and normal call. (source: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7911430/ Deep Learning-Based Cattle Vocal Classification Model and Real-Time Livestock Monitoring System with Noise Filtering ).
BovineTalk: https://gitlab.com/is-annazam/bovinetalk
Youtube: Youtube poulty sounds with noise: https://www.youtube.com/watch?v=70IqKloH-mw  -->