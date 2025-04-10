# Hyperbolic-Ai
Hyperbolic Node Setup Guide

Easily run the Hyperbolic Node on your VPS.

Official Site: https://app.hyperbolic.xyz/


Step-by-Step Instructions

1. Update & Upgrade Your System

###sudo apt update && sudo apt upgrade -y

2. Install Required Packages

sudo apt install git python3 python3-pip python3-venv -y

3. Clone the Repo

git clone https://github.com/0xmoei/chatbot-app.git
cd chatbot-app



VPS-Only (Skip for Local Setup)

4. Install Screen

apt install screen -y

5. Create a Screen Session

screen -S hyperbolic



6. Create Python Virtual Environment

python3 -m venv venv
source venv/bin/activate
pip install requests



7. Add Your API Key

nano chatbot.py

Find the line:

headers = {"Authorization": "Bearer YOUR_API_KEY_HERE"}

Replace 'YOUR_API_KEY_HERE' with your actual API key.

Save and exit:
Press CTRL+X, then Y, then Enter



8. Run the Bot

python3 chatbot.py

Detach screen:
Press CTRL+A then D


Restart / Resume Instructions

If the bot stops (after 100 questions) or you disconnect:

Reconnect to the screen session:

cd chatbot-app
screen -r hyperbolic

Detach again if needed:
Press CTRL+A then D

Re-run the bot:

python3 chatbot.py

Detach again:
Press CTRL+A then D
