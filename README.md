# Video Calling App

A real-time video calling web application using WebRTC, Node.js, and Socket.io. This project enables users to connect and communicate via video and audio directly in their browsers, leveraging peer-to-peer technology for low-latency communication.

## Features
- Real-time video and audio calling between users
- Peer-to-peer connection using WebRTC
- Signaling server implemented with Node.js and Socket.io
- Simple and intuitive user interface
- NAT traversal using ICE candidates
- **Works on Local WiFi:** Devices connected to the same WiFi network can easily discover and connect to each other for video calls.

## Technologies Used
- WebRTC
- Node.js
- Express.js
- Socket.io
- HTML, CSS, JavaScript

## Getting Started

### Prerequisites
- Node.js (v14 or higher recommended)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/videoCalling.git
   cd videoCalling
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the server:
   ```bash
   node server.js
   ```
4. Open your browser and navigate to [http://localhost:9000](http://localhost:9000)

## Usage
- Open the app in your browser.
- Share the room link or connect as instructed in the UI to start a video call.

## Project Structure
- `server.js` - Node.js server for signaling
- `app/index.html` - Main frontend HTML file
- `public/js/main.js` - Client-side JavaScript for WebRTC and signaling
- `public/css/style.css` - Stylesheet

## Additional Notes

**Media Stream Negotiation:**
WebRTC involves negotiating media streams between peers. The addTrack() method is used to add audio and video tracks from the local stream to the peer connection. These tracks are then negotiated between peers during the offer/answer exchange to establish a common media format for communication.

**Establishing Bi-Directional Communication:**
By adding local tracks to the peer connection, you enable bi-directional communication between peers. Your local audio and video tracks are sent to the remote peer, allowing them to see and hear you. Similarly, the remote peer's audio and video tracks are received and played back locally.

**Codec Negotiation:**
Adding tracks to the peer connection triggers codec negotiation between peers. WebRTC negotiates codecs based on the capabilities of each peer's device and network conditions to ensure optimal audio and video quality during communication.

**ICE Candidate Exchange:**
The addition of tracks to the peer connection triggers the gathering and exchange of ICE (Interactive Connectivity Establishment) candidates. ICE candidates facilitate NAT traversal and enable peers to establish direct peer-to-peer connections, even when behind firewalls or NAT devices.

**Signaling:**
Once local tracks are added to the peer connection, the peer connection's local description is updated. This local description includes information about the local media streams and ICE candidates, which is then sent to the remote peer through a signaling channel for negotiation.

---

Feel free to contribute or open issues for improvements! 
