# Korean Streaming Automatic Speech Recognition
**Real-time streaming Korean speech-to-text model that can run on a CPU**

ASR (Automatic Speech Recognition) is a process that involves two distinct stages:

1. Speech Enhancement: In this stage, the incoming audio or speech signal is processed to reduce noise, improve clarity, and enhance the quality of the speech. Various techniques such as filtering, spectral subtraction, and deep learning-based methods may be employed to achieve speech enhancement. There are two main approaches for processing using deep learning techniques: waveform domain processing and spectrogram domain processing. We process waveform domain.

2. Speech Recognition: Once the speech signal has been enhanced, it is passed through the speech recognition system. In this stage, the system converts the processed audio into text by identifying and transcribing the spoken words. Modern ASR systems typically rely on advanced machine learning algorithms, such as deep neural networks, to accurately recognize and transcribe the speech.

Together, these two stages enable ASR systems to convert spoken language into text, making them valuable tools in various applications such as voice assistants, transcription services, and more.

We used denoiser from @[facebook](https://github.com/facebookresearch/denoiser) and @[Nemo framework](https://github.com/NVIDIA/NeMo) for conformer CTC.

<div align="center">
  <img src="https://github.com/SUNGBEOMCHOI/Korean-Streaming-ASR/assets/92682815/f140e147-74cb-43ee-8daa-c3356492b28a" height=75% width=80% alt="model_overview"/>
</div>



## Requirements
Please refer to **[pip.txt](https://github.com/SUNGBEOMCHOI/Korean-Streaming-ASR/blob/main/pip.txt)** for the list of required dependencies

**Clone**
```bash
git clone https://github.com/SUNGBEOMCHOI/Korean-Streaming-ASR.git
cd Korean-Streaming-ASR
```


## Run
**File mode**
```bash
python  audio_stream.py --audio_path "./audio_example/0001.wav" --device cpu
```

**Microphone mode**
```bash
python audio_stream.py --mode microphone --device cpu
```

**Web**
```
flask run
```

---
### Example
**Raw Wave(Input)**

<div align="center">
  
  https://github.com/SUNGBEOMCHOI/Korean-Streaming-ASR/assets/92682815/7f4b98f4-bda7-49ba-b191-c2a49f1399dd

</div>

**Clean Wave (enhanced by denoiser)**

<div align="center">

  https://github.com/SUNGBEOMCHOI/Korean-Streaming-ASR/assets/92682815/ac41e19e-8323-436b-914d-958b25d68de2

</div>


**Text**
<div align="center">
  
![스트리밍 gif](https://github.com/SUNGBEOMCHOI/Korean-Streaming-ASR/assets/92682815/97175803-72ed-41dd-8baf-443200bc9022)

</div>


---
### Datasets

We collect data from [AI Hub](https://aihub.or.kr/)

---
### References

```bibtex
@inproceedings{defossez2020real,
  title={Real Time Speech Enhancement in the Waveform Domain},
  author={Defossez, Alexandre and Synnaeve, Gabriel and Adi, Yossi},
  booktitle={Interspeech},
  year={2020}
}
```


