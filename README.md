---
title: "thesandi99"
emoji: 🎤🎸🥁🎹
colorFrom: yellow
colorTo: purple
sdk: docker
app_port: 7860
tags: ["audio", "music", "vocal-removal", "karaoke", "music-separation", "music-source-separation"]
pinned: true
---

<h2 align="center">Moseca - Music Source Separation & Karaoke</h1>
<p align="center">
    <a href="https://colab.research.google.com/drive/1ODoK3VXajprNbskqy7G8P1h-Zom92TMA?usp=sharing">
        <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">
    </a>
    <a href="https://huggingface.co/spaces/fabiogra/moseca">
        <img src="https://img.shields.io/badge/🤗%20Hugging%20Face-Spaces-blue" alt="Hugging Face Spaces">
    </a>
    <a href="https://huggingface.co/spaces/fabiogra/moseca/discussions?docker=true">
        <img src="https://img.shields.io/badge/-Docker%20Image-blue?logo=docker&labelColor=white" alt="Docker">
    </a>
</p>

---

- [Setup](#setup)
  - [Local environment](#local-environment)
  - [Docker](#docker)
  - [(Optional) Preprocess samples](#optional-preprocess-samples)
- [About](#about)
  - [High-Quality Stem Separation](#high-quality-stem-separation)
  - [Advanced AI Algorithms](#advanced-ai-algorithms)
  - [Karaoke Fun](#karaoke-fun)
  - [Easy Deployment](#easy-deployment)
  - [Open-Source and Free](#open-source-and-free)
  - [Support](#support)
- [FAQs](#faqs)
  - [What is Moseca?](#what-is-moseca)
  - [Are there any limitations?](#are-there-any-limitations)
  - [How does Moseca work?](#how-does-moseca-work)
  - [How do I use Moseca?](#how-do-i-use-moseca)
  - [Where can I find the code for Moseca?](#where-can-i-find-the-code-for-moseca)
  - [How can I get in touch with you?](#how-can-i-get-in-touch-with-you)
- [Disclaimer](#disclaimer)

---


## Setup
### Local environment
Create a new environment with Python 3.10 and install the requirements:
```bash
pip install -r requirements.txt
```
set the `PYTHONPATH` to the root folder:
```bash
export PYTHONPATH=path/to/moseca
```
download the vocal remover model:
```bash
wget --progress=bar:force:noscroll https://huggingface.co/fabiogra/baseline_vocal_remover/resolve/main/baseline.pth
```
then run the app with:
```bash
streamlit run app/header.py
```
### Docker
You can also run the app with Docker:
```bash
docker build -t moseca .
docker run -it --rm -p 7860:7860 $(DOCKER_IMAGE_NAME)
```
or pull the image from Hugging Face Spaces:
```bash
docker run -it -p 7860:7860 --platform=linux/amd64 \
	registry.hf.space/fabiogra-moseca:latest
```

You can set the following environment variables to limit the resources used by the app:
- ENV_LIMITATION=true
- LIMIT_CPU=true

### (Optional) Preprocess samples
If you want to preprocess the samples used in the demo, you need to set the env variable `PREPARE_SAMPLES=true` as a secret (create the file `run/secrets/PREPARE_SAMPLES` with `true` value inside).

If you run locally you also need to move the files inside `scripts` to the root folder and run `prepare_samples.sh`.
```
cp scripts/ .
chmod +x prepare_samples.sh
python prepare_samples.sh
```

---
## About

 musician looking to remix your favorite songs, a karaoke
enthusiast, or a music lover wanting to dive deeper into your favorite tracks,
Moseca is for you.

<br>

### High-Quality Stem Separation

<img title="High-Quality Stem Separation" src="https://i.imgur.com/l7H8YWL.png" width="250" ></img>


<br>

Separate up to 6 stems including 🗣voice, 🥁drums, 🔉bass, 🎸guitar,
🎹piano (beta), and 🎶 others.

<br>

### Advanced AI Algorithms

<img title="Advanced AI Algorithms" src="https://i.imgur.com/I8Pvdav.png" width="250" ></img>

<br>

Moseca utilizes state-of-the-art AI technology to extract voice or music from
your original songs accurately.

<br>

### Karaoke Fun

<img title="Karaoke Fun" src="https://i.imgur.com/nsn3JGV.png" width="250" ></img>

<br>

Engage with your favorite tunes in a whole new way!

Moseca offers an immersive online karaoke experience, allowing you to search
for any song on YouTube and remove the vocals online.

Enjoy singing along with high-quality instrumentals at the comfort of your home.


<br>

### Easy Deployment


With Moseca, you can deploy your personal Moseca app in the
<a href="https://huggingface.co/spaces/fabiogra/moseca?duplicate=true">
<img src="https://img.shields.io/badge/🤗%20Hugging%20Face-Spaces-blue"
alt="Hugging Face Spaces"></a> or locally with
[![Docker Call](https://img.shields.io/badge/-Docker%20Image-blue?logo=docker&labelColor=white)](https://huggingface.co/spaces/fabiogra/moseca/discussions?docker=true)
in just one click.

You can also speed up the music separation process by [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ODoK3VXajprNbskqy7G8P1h-Zom92TMA?usp=sharing) with GPU support.

<br>

### Open-Source and Free

Moseca is the free and open-source alternative to lalal.ai, splitter.ai or media.io vocal remover.

You can modify, distribute, and use it free of charge. I believe in the power of community
collaboration and encourage users to contribute to our source code, making Moseca better with
each update.


<br>

### Support

- Show your support by giving a star to the GitHub repository [![GitHub stars](https://img.shields.io/github/stars/fabiogra/moseca.svg?style=social&label=Star)](https://github.com/fabiogra/moseca).
- If you have found an issue or have a suggestion to improve Moseca, you can open an [![GitHub issues](https://img.shields.io/github/issues/fabiogra/moseca.svg)](https://github.com/fabiogra/moseca/issues/new)
- Enjoy Moseca? [![Buymeacoffee](https://img.shields.io/badge/Buy%20me%20a%20coffee--yellow.svg?logo=buy-me-a-coffee&logoColor=orange&style=social)](https://www.buymeacoffee.com/fabiogra)

------
