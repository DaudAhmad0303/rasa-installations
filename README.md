# Installation Guide for RASA-x (and RASA as well) in Windows OS in Anaconda
Create a new Python **Virtual Environment**:
```
conda create -n rasa281 python=3.8
```

**Activate** the environment
```
conda activate rasa281
```

Install the Specified `pip` version
```
pip install pip==20.2
```

> Needs **Microsoft Build Tool** already installed as a dependency in RASA

Install the **RASA** Specified version
```
pip install rasa==2.8.1
```

Install the **rasa-sdk** specified version
```
pip install rasa-sdk==2.8.1
```

So far, We you have installed the followings:
```
Rasa Version      :         2.8.1
Minimum Compatible Version: 2.8.0 
Rasa SDK Version  :         2.8.6 
Rasa X Version    :         None
Python Version    :         3.8.13
Operating System  :         Windows-10-10.0.19044-SP0
Python Path       :         C:\Users\username\.conda\envs\rasa281\python.exe
```

You can get above with this command:
```
rasa --version
```

Now, You can create an **initial project** of RASA and then further provide directory path
```
rasa init
```

For Installation of RASA-X first install some dependencey libraries. (press y when prompt for options)
```
pip install SQLAlchemy==1.3.22
```

```
conda install ujson
```

```
conda install tensorflow
```

```
pip install rasa-x==0.39.3 --extra-index-url https://pypi.rasa.com/simple
```

Now, Check for whether RASA-X has been installed
```
rasa --version
```

```
Rasa Version      :         2.8.1
Minimum Compatible Version: 2.8.0 
Rasa SDK Version  :         2.8.6 
Rasa X Version    :         0.39.3
Python Version    :         3.8.13
Operating System  :         Windows-10-10.0.19044-SP0
Python Path       :         C:\Users\username\.conda\envs\rasa281\python.exe
```

> **rasa 2.8.1 with Python virtual environment 3.8 has been installed**

---------------------------------------------------------------------------------------------
[For Running on WhatsApp relevent commands]
$ rasa run -m models --enable-api --cors "*"
$ ngrok http 5005


$ rasa run --log-file out.log --cors * --enable-api

--------------------------------------------------------------------------------------------
For voice chatbot Libraries

For Automatic Speech Recognition (ASR) | Speech To Text (STT)
$ pip install SpeechRecognition PyAudio

For Text to Speech (TTS)
$ pip install gtts
[For Windows]
$ pip install mpyg321
[For Ubuntu]
$ sudo apt-get install mpg321


For Running Endpoint:
$ rasa run -m models --endpoints endpoints.yml --port 5002 --credentials credentials.yml 

----
