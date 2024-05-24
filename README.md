# Chatbot Application

This application allows you to upload an image and ask questions about it. The chatbot uses Visual Question Answering VQA models to provide relevant answers.

## Features

- **Model Selection**: Choose between different VQA models (currently supports BLIP).
- **Image Upload**: Upload an image in JPG, PNG, or JPEG format.
- **Interactive Chat**: Ask questions about the uploaded image and receive responses.

## How It Works

1. **Upload an Image**: Use the sidebar to upload an image. The image will be displayed in the sidebar.
2. **Ask Questions**: Type your question in the chat input box at the bottom of the page.
3. **Get Responses**: The selected VQA model processes the question and image to generate an answer, which is displayed in the chat.

## Steps to Run the Chatbot Application

### Step 1: Create a New Python Virtual Environment

Follow these instructions to create a virtual environment for a specified version of Python.

#### Prerequisites

- Ensure Python is installed on your system. You can download it from [python.org](https://www.python.org/downloads/).
- Verify that `pip` is installed by running `pip --version` in your terminal or command prompt.

#### Step 1.1: Install `virtualenv`

If not already installed, you need to install `virtualenv` using pip:

```bash
pip install virtualenv
```

#### Step 1.2: Create the Virtual Environment

Create a virtual environment specifying the path to the Python interpreter for the version you wish to use. Replace `path/to/python` with the actual path and `myenv` with your desired environment name:

```bash
virtualenv -p /path/to/python myenv
```

- **Example for Windows**: If Python 3.8 is installed at `C:\Python38\python.exe`:

  ```bash
  virtualenv -p C:\Python38\python.exe myenv
  ```

- **Example for macOS/Linux**: If Python 3.8 is installed and the executable is named `python3.8`:

  ```bash
  virtualenv -p python3.8 myenv
  ```

#### Step 1.3: Activate the Virtual Environment

Activate the newly created virtual environment:

- **On Windows**:

  ```bash
  myenv\Scripts\activate
  ```

- **On macOS/Linux**:

  ```bash
  source myenv/bin/activate
  ```

#### Step 1.4: Verify Python Version

Check the Python version to ensure the correct version is activated:

```bash
python --version
```

#### Step 1.5: Deactivate the Environment

To stop using the virtual environment and revert to the default Python settings:

```bash
deactivate
```

This completes the setup of a Python virtual environment with your specified version.

### Step 2: Install Necessary Packages

Activate the virtual environment and install the required packages using the following command:

```bash
pip install -r requirements.txt
```

### Step 3: Run the Streamlit Application

Run the application with the following commands:

```bash
cd chatbot
streamlit run app.py
```

### Step 4: Interact with the Application

1. **Open the Application**: Once the Streamlit app is running, open your browser and navigate to the local server URL provided.
2. **Upload an Image**: Use the sidebar to upload an image file. The uploaded image will be displayed in the sidebar.
3. **Ask a Question**: Type your question in the chat input box at the bottom of the page.
4. **Receive an Answer**: The chatbot will process your question and the uploaded image, and provide an answer in the chat interface.

## Notes

- The application downloads the Hugging Face models and caches them inside the `models` folder when you run the application for the first time. Therefore, the first run will be slower. In subsequent runs, it will load the downloaded models stored locally.
- If you encounter errors related to the Hugging Face transformers library, you can install the latest version directly using the following command:

  ```bash
  pip install git+https://github.com/huggingface/transformers
  ```

## File Structure

- `app.py`: The main application script.
- `requirements.txt`: A list of Python packages required to run the app.
- `models/`: Directory for caching model files.

## Example

Here's a simple example to get you started:

1. **Upload an Image**:
   ![Upload Image](screenshot1.png)
2. **Ask a Question**:
   ![Ask Question](screenshot2.png)
3. **Receive an Answer**:
   ![Receive Answer](screenshot3.png)
