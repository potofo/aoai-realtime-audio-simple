# Microsoft aoai-realtime-audio-sdk rtclient-0.5.1 Sample Programs

This repository contains sample programs using Microsoft's aoai-realtime-audio-sdk rtclient-0.5.1.  It includes several sample programs that allow you to experience speech recognition and AI responses, along with scripts and configuration files to run them.


## Sample Program Descriptions

This collection includes three Python sample programs:

- **`low_level_sample.py`**: A sample program to verify the basic functions of the SDK. You can verify the basic flow of loading, sending, and receiving audio data.
- **`client_sample.py`**: A sample program that generates a text response using an Azure OpenAI model for input audio and outputs it as speech. You can verify the integration of speech recognition, text generation, and speech synthesis.
- **`client_sample_no_vad.py`**: A sample program that responds to input audio with a system prompt. Because it does not use Voice Activity Detection (VAD), it supports continuous audio input.


## File Descriptions

This repository contains the files necessary to run the sample programs:

- **`.env.example`**: A sample file for setting the Azure OpenAI endpoint, API key, and the deployment name of the model to be used. Copy this file as `.env` and enter the necessary information.
- **`createvenv.bat`**: A batch file to create a Python virtual environment in the `venv` folder. (For Windows Command Prompt)
- **`activate.bat`**: A batch file to activate the `venv` environment created by `createvenv.bat`. (For Windows Command Prompt) In PowerShell, activate the virtual environment using the `activate` command.
- **`deactivate.bat`**: A batch file to deactivate the Python virtual environment `venv`. (For Windows Command Prompt) In PowerShell, deactivate by exiting PowerShell.
- **`do_low_level_sample.bat`**: A batch file to run `low_level_sample.py`.
- **`do_client_sample.bat`**: A batch file to run `client_sample.py`.
- **`do_client_sample_no_vad.bat`**: A batch file to run `client_sample_no_vad.py`.
- **`download-wheel.ps1`**: A PowerShell script to download `rtclient-0.5.1-py3-none-any.whl`, which is not registered in the pypi.org repository.
- **`download-wheel.sh`**: A Unix shell script to download `rtclient-0.5.1-py3-none-any.whl`, which is not registered in the pypi.org repository.
- **`requirements.txt`**: A file listing the required Python packages for the sample programs. Install with `pip install -r requirements.txt`.
- **`test_instructions_for_LMM.txt`**: Sample instructions used by `client_sample_no_vad.py`. (Speaking excitedly)
- **`test_instructions_for_LMM_soccer.txt`**: Sample instructions used by `client_sample_no_vad.py`. (Speaking like a soccer broadcast)
- **`test_instructions_for_LMM_soccer_ja.txt`**: Sample instructions used by `client_sample_no_vad.py`. (Speaking like a soccer broadcast in Japanese)
- **`output/`**: A folder where the results of running the sample programs are output.


## Installation Instructions

1. **Create a Python Virtual Environment**: Run `createvenv.bat` to create a Python virtual environment in the `venv` folder.
2. **Activate the Python Virtual Environment**: Activate the virtual environment by running the `activate` command in PowerShell or `activate.bat` in the command prompt.
3. **Download rtclient-0.5.1**: Run `download-wheel.ps1` to download `rtclient-0.5.1-py3-none-any.whl`.
4. **Install rtclient-0.5.1**: Install the downloaded `rtclient` into the virtual environment using `pip install rtclient-0.5.1-py3-none-any.whl`.
5. **Install Dependent Packages**: Install the necessary Python packages into the virtual environment using `pip install -r requirements.txt`.
6. **Configure the .env file**: Copy `.env.example` to `.env` and enter the Azure OpenAI endpoint, API key, and model deployment name.


## How to Run

1. **Run `low_level_sample.py`**: Run `do_low_level_sample.bat`. The results will be output to the `output` folder.
2. **Run `client_sample.py`**: Run `do_client_sample.bat`. The results will be output to the `output` folder.
3. **Run `client_sample_no_vad.py`**: Run `do_client_sample_no_vad.bat`. This sample uses the `test_instructions_for_LMM_soccer_ja.txt` file. The results will be output to the `output` folder.