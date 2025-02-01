# Realtime voice assitant using LiveKit

This work was inspired by [LiveKit tutorials](https://docs.livekit.io/agents/quickstarts/s2s/), and youtube tutorial by [Damiano Redemagni](https://www.youtube.com/watch?v=2jafwzDhJ2k) and [Underfitted](https://www.youtube.com/watch?v=nvmV0a2geaQ)

For more details, examples and agents available go to LiveKit github: https://github.com/livekit/agents/tree/main

1) First, you need to create a virtual environment, update pip and install the required packages:

   ```
   python3 -m venv .venv
   source .venv/bin/activate
   pip install -U pip
   pip install -r requirements.txt

   ```

2. You need to set up the following environment variables:

   ```
   LIVEKIT_URL="wss://...
   LIVEKIT_API_SECRET="...
   LIVEKIT_API_KEY="...
   OPEN_API_KEY="...
   ```
3. To run the code (choose agent_visual.py or agent_voice.py):

   ```
   python3 agent.py download-files
   python3 agent.py start
   ```

Open the playground to get on the interface of the voice assistant:

https://agents-playground.livekit.io/
