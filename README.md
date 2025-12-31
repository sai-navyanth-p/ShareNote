# ShareNote  
### Collaborative Real-Time Text Editing Platform

ShareNote is a **real-time collaborative document editing platform** that enables multiple users to simultaneously create, share, and edit documents with strong consistency guarantees. Built using **Java, multithreading, socket-based networking, and database integration**.

---

## 🚀 Features

### 🔐 User Authentication & Access Control
- Secure user registration and login with **hashed credentials**
- Role-based permissions:
  - **Owner** – full control
  - **Editor** – edit access
  - **Viewer** – read-only access
- Session-based authentication

### 📄 Document Management
- Create, open, edit, save, and delete documents
- Persistent storage with metadata (creator, timestamp, collaborators)
- Auto-save to prevent data loss

### 🤝 Real-Time Collaboration
- Multiple users can edit the same document concurrently
- **Instant propagation** of changes across all connected clients
- Live collaborator presence and cursor tracking
- Low-latency updates using socket-based communication

### 🔄 Version Control
- Automatic version snapshots on every save
- View complete document history
- Restore documents to previous versions

### 🖥️ Interactive UI
- Clean, responsive, and intuitive interface
- Real-time updates without page refresh
- Visual indicators for collaborators and document state

---

## 🧠 System Architecture

ShareNote follows a **client–server architecture**:

- **Backend**
  - Java-based server
  - Multithreaded handling of concurrent clients
  - Socket-based real-time communication
  - Database-backed persistence layer
- **Frontend**
  - Web-based UI
  - Communicates with backend for real-time updates and document operations

---

## 🛠️ Tech Stack

### Backend
- Java
- Multithreading
- Java Sockets (Client–Server communication)
- REST APIs for document operations
- Database integration (users, documents, versions, permissions)

### Frontend
- JavaScript
- Modern frontend tooling (Vite-based setup)
- Real-time UI updates

### Concepts Demonstrated
- Distributed systems
- Concurrency & synchronization
- Conflict resolution
- Client-server networking
- Persistent storage & versioning

---

## ⚙️ How to Run the Application

### Prerequisites
- Java (JDK 11+ recommended)
- Node.js & npm
- Gradle

### 🔧 Backend Setup

```bash
cd ShareNote/backend
bash gradlew build
bash gradlew bootRun
```

### 🎨 Frontend Setup

```bash
cd ShareNote/frontend
npm install
npm run dev
```

## 🌐 Access the Application

Open your browser and navigate to:

```text
http://localhost:5173/
```

## 📌 Example Workflow

1. **User Registration** – Alice and Bob register and log in.
2. **Document Creation** – Alice creates a document named *Team Notes*.
3. **Sharing** – Alice shares the document with Bob (edit access).
4. **Collaborative Editing** – Both users edit simultaneously and see updates in real time.
5. **Version Control** – Bob restores a previous version after an accidental edit.
6. **Persistence** – The final document is stored and accessible anytime.


## ⚠️ Engineering Challenges Addressed

- Maintaining **consistency** across concurrent edits
- Handling **network delays and failures**
- Conflict detection and resolution
- Concurrent database access
- Scalability with multiple active users

---

## 📚 Learning Outcomes

This project demonstrates:
- Practical implementation of **distributed systems**
- Real-world use of **multithreading and synchronization**
- End-to-end system design (backend + frontend)
- Challenges behind real-time collaborative platforms
