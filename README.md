# BitStreams - P2P Livestreaming

![BitStreams Screenshot](https://github.com/user-attachments/assets/2800e8ed-5055-4cd5-9a0b-d9bbc2952b2b)


BitStreams is a peer-to-peer (P2P) livestreaming application built using WebRTC. It allows users to broadcast and watch livestreams directly between peers without the need for a centralized server, ensuring a decentralized and privacy-focused streaming experience. This project is designed for simplicity and ease of use, with features like live comments, stream sharing, and 1v1 video chat capabilities.

## Features

- **P2P Livestreaming**: Stream video directly to peers using WebRTC.
- **Live Comments**: Engage with viewers through a real-time comment section.
- **Stream Sharing**: Viewers can relay streams to other peers, creating a scalable network.
- **1v1 Chat**: Enable video sharing with upstream peers for a more interactive experience.
- **Customizable UI**: Adjust colors and device settings through the in-app settings menu.
- **Responsive Design**: Optimized for both desktop and mobile browsers, with a side-by-side video/comments layout on desktop and a stacked layout on mobile.

## Prerequisites

Before running BitStreams, ensure you have the following:

- A modern web browser (e.g., Chrome, Firefox, Edge) that supports WebRTC.
- Access to a camera and microphone for broadcasting.
- A local development server or hosting solution that supports HTTPS (required for WebRTC).

**Note**: WebRTC requires HTTPS for secure connections. If testing locally, you can use Chrome with the `--allow-file-access-from-files` flag, but this is not recommended for production.

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/BitcoinJake09/BitStream.git
   cd BitStream

Serve the Application:
Since WebRTC requires HTTPS, you’ll need to serve the index.html file over a secure connection. You can use one of the following methods:
Local Development Server:
Use a simple HTTP server with HTTPS support. For example, with Python 3:
bash

python -m http.server 8000

Then, access the app at http://localhost:8000. For HTTPS, you may need a tool like mkcert to generate local certificates.

Deploy to a Hosting Service:
Deploy the app to a service like Netlify, Vercel, or GitHub Pages with HTTPS enabled.

Access the App:
Open your browser and navigate to the hosted URL (e.g., https://your-deployment-url or http://localhost:8000 if using the local server with Chrome's flag).

Usage
Broadcasting a Stream
Enter your BitStream Name in the input field.

Click Start Stream to begin broadcasting your video.

(Optional) Set a stream title to let viewers know what your stream is about.

Click Generate Signaling Data to create a JSON payload.

Share the JSON data with a viewer (e.g., via messaging platforms like X DMs).

Watching a Stream
Enter your BitStream Name.

Paste the signaling data you received from the broadcaster into the "Connect to Peer" section.

Click Connect to join the stream.

(Optional) Click Share Stream to relay the stream to another peer by generating new signaling data.

(Optional) Enable 1v1 Chat to share your video with the upstream peer.

Additional Features
Live Comments: Type and send comments visible to all connected peers.

Settings: Customize the background, button, and text colors, and select your camera and microphone.

Fullscreen Mode: Double-click the video to toggle fullscreen.

Responsive Layout: On desktop, the video and comments are side by side; on mobile, they stack vertically.

Privacy Note
BitStreams uses WebRTC for peer-to-peer communication, which may expose your IP address to other peers. To protect your privacy, we strongly recommend using a VPN while streaming or viewing. A VPN will help mask your IP address and enhance your security.
Known Limitations
WebRTC requires HTTPS for secure connections. Local testing without HTTPS may require browser flags (not recommended for production).

The application relies on STUN servers for NAT traversal. If peers are behind strict firewalls, connectivity may be limited.

Mobile browser support may vary depending on WebRTC compatibility.

Contributing
Contributions are welcome! If you'd like to contribute to BitStreams, please follow these steps:
Fork the repository.

Create a new branch (git checkout -b feature/your-feature-name).

Make your changes and commit them (git commit -m "Add your feature").

Push to your branch (git push origin feature/your-feature-name).

Open a Pull Request with a detailed description of your changes.

Please ensure your code follows the existing style and includes appropriate comments.
License
This project is licensed under the MIT License. See the LICENSE file for details.
Developer
Developed by BitcoinJake09. For more details, visit the GitHub Repository.
Acknowledgements
Built with WebRTC for P2P communication.

Uses Google's public STUN servers for NAT traversal.

