# ORION - Optimal Random Interactive Online Network

ORION is a web-based platform that facilitates safe and random anonymous chat connections. Users can connect with random individuals for conversations while maintaining their privacy and ensuring content is clean and appropriate. The platform employs features like message filtering and rate limiting for an optimal user experience.

---

## Features

- **Anonymous Random Chat:** Connect with random users for a completely anonymous conversation.
- **Message Filtering:** Employs a bad-words filter to sanitize inappropriate content.
- **Rate Limiting:** Limits requests to prevent abuse and ensure server stability.
- **Active Partner Matching:** Automatically matches users looking for a chat partner.
- **Responsive Design:** Simple, user-friendly interface optimized for various devices.

---

## Prerequisites

To run ORION locally, you need:

- [Node.js](https://nodejs.org/) (v14 or later)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/sayanth-t-m/orion.git
   cd orion
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Run the server:
   ```bash
   npm start
   ```

4. Open your browser and navigate to:
   ```
   http://localhost:3000
   ```

---

## Project Structure

```plaintext
ORION/
├── public/           # Static files (HTML, CSS, Client-side JS)
│   ├── index.html    # Main front-end page
│   ├── styles.css    # Styling for the UI
│   └── client.js     # Client-side JavaScript
├── server.js         # Main server logic (Express and Socket.IO)
├── package.json      # Node.js dependencies and scripts
└── README.md         # Project documentation
```

---

## How It Works

### 1. **Server-Side Logic:**
- The server uses **Express** to serve static files and **Socket.IO** to handle real-time communication.
- Users are added to a waiting pool if no partner is available, or paired with another waiting user.
- A profanity filter ensures clean communication.

### 2. **Client-Side Logic:**
- Users can start a chat, send messages, or disconnect from a chat session.
- The interface updates dynamically based on the server events (e.g., new chat partner, message received).

### 3. **Chat Partner Matching:**
- The system uses a `Set` to track waiting users and a `Map` to store active user pairs.

---

## Usage

1. Open the application in your browser.
2. Click **Start New Chat** to find a partner.
3. Once connected, type messages and send them to your partner.
4. If the partner disconnects, you can search for a new partner.

---

## Technical Highlights

- **Express:** For serving static files and handling HTTP requests.
- **Socket.IO:** Enables real-time communication between clients.
- **Bad-Words Filter:** Ensures messages remain clean and appropriate.
- **Rate Limiter:** Prevents spamming and maintains server stability.

---

## Contributions

Contributions are welcome! Follow these steps:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add feature-name"
   ```
4. Push to the branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

---

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

