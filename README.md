# comic book image-to-image translation jupiter book

This repository is my POC, building a pipeline to:

1. identify comic "bubbles" with text in page
2. crop them and OCR them
3. translate them 
4. inpaint them back into the page

As a set of jyupiter notebooks. I've used openai codex, chatgpt and [comic-translate](https://github.com/ogkalu2/comic-translate/) for references.

## By design this is built to run on a macbook

If you want to run it elsewhere you'll need:

1. Pytorch wheel might be different for your platform. I'm using `torchvision`, so you'll need to find out what to replace it with here at [pytorch.org](https://pytorch.org/get-started/locally/). 

2. I use apple vision OCR via [https://github.com/straussmaximilian/ocrmac] wrapper. For a platform-agnostic/"better" solutions - check what comic-translate is using.

## Mac Quick start

1. **Create a virtual environment**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   python -m pip install --upgrade pip
   pip install -r requirements.txt
   ```

4. **Launch Jupyter**
```
jupyter notebook
```
