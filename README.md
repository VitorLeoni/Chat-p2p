# Chat-p2p


A fully decentralized Peer-to-Peer (P2P) chat application featuring voice calls, video, and screen sharing, built with a strong focus on privacy, efficiency, and ease of use.

The application runs directly in the browser as a single HTML file, requiring no installations, account registration, or central backend database.
 Features

End-to-End Encryption (E2EE): Key exchange using ECDH (P-256) and AES-GCM encryption directly between participants via the Web Crypto API.

Self-Destructing Messages: Messages automatically disappear from the screen and memory after 5 minutes.

Voice and Video Calls: Real-time audio and video streaming powered by WebRTC.

Screen Sharing: Share your screen along with system audio transmission (when supported by the OS/browser).

Rooms for up to 5 People: Supports 1 Host and up to 4 interconnected Guests.

Real-Time Network Monitor: Displays round-trip time (RTT), jitter, and packet loss for the P2P connection.

Typing Indicators: Visual notification when other participants are typing.

# Built With


HTML5 / CSS3 (using CSS Variables for themes and responsive layout with Grid & Flexbox)

Vanilla JavaScript

WebRTC API (RTCPeerConnection, RTCDataChannel) for real-time media and data streaming.

Web Crypto API for ECDH key generation and AES-GCM encryption.

Web Audio API for local microphone and system audio mixing.

# Getting Started


Since the entire application is self-contained in a single HTML file, running it is simple:

1. Requirements

A modern web browser supporting WebRTC and Web Crypto APIs (Chrome, Edge, Firefox, Safari, Brave, Opera, etc.).

To ensure media and crypto APIs function properly, open the file using:

A secure server (https://)

Local host (http://localhost or http://127.0.0.1)

Direct file opening in your browser (file://).

2. How to Start a Session

Creating a Room (Host):

1- Open the file in your web browser.

2- Enter your display name and click "Criar sala (sou o host)" (Create Room).

3- Copy the generated Invite Code (Step 1) and send it to your guest.

4- Wait for the guest to send you back their response code.

5- Paste their response code into "Código de resposta" (Step 2) and click "Conectar" (Connect).

Joining a Room (Guest):

1- Open the file in your web browser.

2- Enter your display name and click "Tenho um código" (I have a code).

3- Paste the invite code received from the Host into Step 1 and click "Gerar resposta" (Generate response).

4- Copy the response code generated in Step 2 and send it back to the Host.


# Connection Architecture


The Host acts as the central hub, maintaining individual direct P2P connections with each guest.
The Host relays audio, video, and text messages between all connected participants.
Signaling (initial handshake) is performed manually by exchanging tokens, removing the need for an external signaling server.
#
Vibe Coder Edition is maintained by Keven Toledo and may be out of date
