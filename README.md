# AI Voice and Video Agents with Livekit

This repository contains code for implementing AI-powered voice and video agents using the [Livekit](https://livekit.io/) platform. We have created two agent versions:

  * **Voice-Only Agent (agent\_voice.py):**  Provides voice assistance based on the official Livekit documentation examples.
  * **Voice and Visual Agent (agent\_vision.py):**  Extends the voice agent to include visual capabilities, following the tutorial by Damiano Redemagni and Underfitted.

This implementation is straightforward to set up and run, thanks to the excellent documentation and tutorials provided by Livekit.

## Inspiration

This work is inspired by:

  * [LiveKit tutorials](https://www.google.com/url?sa=E&source=gmail&q=https://livekit.io/docs) and examples.
  * YouTube tutorial by [Damiano Redemagni](https://www.youtube.com/watch?v=2jafwzDhJ2k) and [Underfitted](https://www.google.com/url?sa=E&source=gmail&q=https://www.youtube.com/@Underfitted).

## Agents

This repository includes two agent implementations:

  * **`agent_voice.py`**: An AI agent that provides voice-only assistance. This agent interacts with users solely through voice, leveraging Speech-to-Text (STT) to understand voice input and Text-to-Speech (TTS) to respond. It is based on examples found in the official Livekit documentation.

  * **`agent_vision.py`**: An enhanced AI agent that combines voice and visual capabilities. In addition to voice interaction, this agent can process visual information, such as images from a video feed. This allows for more complex interactions where the agent can understand and respond to visual cues. This agent is based on the tutorial by Damiano Redemagni and Underfitted.

## Setup

Follow these steps to set up and run the agents:

1.  **Create a virtual environment:**

    ```bash
    python3 -m venv .venv
    ```

2.  **Activate the virtual environment:**

    ```bash
    source .venv/bin/activate
    ```

3.  **Update pip:**

    ```bash
    pip install -U pip
    ```

4.  **Install requirements:**

    ```bash
    pip install -r requirements.txt
    ```

5.  **Set environment variables:**
    Create a `.env` file in the repository root and add the following environment variables with your actual credentials:

    ```
    LIVEKIT_URL="wss://YOUR_LIVEKIT_URL"
    LIVEKIT_API_SECRET="YOUR_LIVEKIT_API_SECRET"
    LIVEKIT_API_KEY="YOUR_LIVEKIT_API_KEY"
    OPENAI_API_KEY="YOUR_OPENAI_API_KEY"
    ```

    Replace the placeholder values with your actual Livekit and OpenAI API keys and URL. You can obtain Livekit credentials from your [Livekit account](https://www.google.com/url?sa=E&source=gmail&q=https://cloud.livekit.io/) and OpenAI API key from [OpenAI's website](https://www.google.com/url?sa=E&source=gmail&q=https://platform.openai.com/).

6.  **Run the agent:**

    First, download necessary files:

    ```bash
    python3 agent.py download-files
    ```

    Then, to start the voice-only agent, run:

    ```bash
    python3 agent.py start agent_voice
    ```

    Or, to start the voice and visual agent, run:

    ```bash
    python3 agent.py start agent_vision
    ```

    *(Replace `agent.py` with `agent_voice.py` or `agent_vision.py` if you renamed the files)*

7.  **Open Livekit Playground:**

    Access the [Livekit Agents Playground](https://agents-playground.livekit.io/) in your browser to connect to the agent and interact with it through a user-friendly interface.

## Key Libraries

  * **asyncio:**  This Python library is used for asynchronous programming. It enables the agent to handle multiple operations concurrently, such as processing audio and video streams, and interacting with APIs, without blocking the main execution thread. This is crucial for building responsive and efficient real-time applications like voice and video agents.

  * **dotenv:** The `python-dotenv` library facilitates the management of environment variables. It loads environment variables from a `.env` file into the application's environment. This is important for security and configuration, as it allows you to keep sensitive information like API keys separate from your code and easily configure different environments without modifying the code directly.

## Explore More

For more advanced examples, additional agents, and detailed information, visit the [LiveKit Agents GitHub repository](https://github.com/livekit/agents/tree/main).


```
```
