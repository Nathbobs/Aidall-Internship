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



error

---------------------------------------------------------------------------
LibsndfileError                           Traceback (most recent call last)
Cell In[56], line 6
      4 # Remove batch and channel dimensions
      5 cleaned_audio = cleaned_audio_tensor.squeeze().numpy()
----> 6 sf.write('cleaned_audio_tf.wav', cleaned_audio, sr)

File /opt/anaconda3/lib/python3.11/site-packages/soundfile.py:343, in write(file, data, samplerate, subtype, endian, format, closefd)
    341 else:
    342     channels = data.shape[1]
--> 343 with SoundFile(file, 'w', samplerate, channels,
    344                subtype, endian, format, closefd) as f:
    345     f.write(data)

File /opt/anaconda3/lib/python3.11/site-packages/soundfile.py:658, in SoundFile.__init__(self, file, mode, samplerate, channels, subtype, endian, format, closefd)
    655 self._mode = mode
    656 self._info = _create_info_struct(file, mode, samplerate, channels,
    657                                  format, subtype, endian)
--> 658 self._file = self._open(file, mode_int, closefd)
    659 if set(mode).issuperset('r+') and self.seekable():
    660     # Move write position to 0 (like in Python file objects)
    661     self.seek(0)

File /opt/anaconda3/lib/python3.11/site-packages/soundfile.py:1216, in SoundFile._open(self, file, mode_int, closefd)
   1213 if file_ptr == _ffi.NULL:
...
   1219     # when opening a named pipe in SFM_WRITE mode.
   1220     # See http://github.com/erikd/libsndfile/issues/77.
   1221     self._info.frames = 0

LibsndfileError: Error opening 'cleaned_audio_tf.wav': Format not recognised.
Output is truncated. View as a scrollable element or open in a text editor. Adjust cell output settings...







<!-- animals_basel: cow sounds are divided into; cough sounds,Estrus call, food anticipating call and normal call. (source: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7911430/ Deep Learning-Based Cattle Vocal Classification Model and Real-Time Livestock Monitoring System with Noise Filtering ).
BovineTalk: https://gitlab.com/is-annazam/bovinetalk
Youtube: Youtube poulty sounds with noise: https://www.youtube.com/watch?v=70IqKloH-mw  -->