# ☕ Java Lab Repository (`java-lab`)

A curated collection of Java laboratory assignments, socket programming, enterprise web applications, distributed computing (RMI), and database-driven software projects.

---

## 📂 Repository Structure

```
java-lab/
├── Calculator/            # MVC-based GUI Calculator using Java Swing
├── StudentRegistration/  # Student Registration System with JDBC & MySQL
├── Server-Client/          # Client-Server Socket Communication (TCP Networking)
├── RMI/                   # Distributed Computing with Remote Method Invocation (RMI)
├── Servlet/               # Jakarta / Java EE Servlet & JSP Web Application
└── Shopsphere/            # Full-Stack E-Commerce System (Swing, Web, RMI, Sockets)
```

---

## 🚀 Projects Overview

### 1. 🧮 Calculator (`Calculator/`)
- **Description:** A desktop calculator built using the **Model-View-Controller (MVC)** architectural pattern in Java Swing.
- **Key Components:**
  - `modelscalculator.java` — Core mathematical logic and state handling.
  - `viewcalculator.java` — Swing user interface with buttons and display.
  - `controllercalculator.java` — Action listener and event dispatcher binding View to Model.
  - `runcalculator.java` — Application bootstrap entry point.
- **How to Run:**
  ```bash
  cd calculator
  javac *.java
  java runcalculator
  ```

---

### 2. 📝 Student Registration System (`StudentRegistration/`)
- **Description:** A database-backed CRUD application that allows registering students, validating input fields, and storing records into a MySQL database.
- **Technologies:** Java Swing/AWT, JDBC (Java Database Connectivity), MySQL (`mysql-connector-j-9.7.0.jar`).
- **How to Run:**
  ```bash
  cd student-registration
  javac -cp ".;mysql-connector-j-9.7.0.jar" StudentRegistration.java
  java -cp ".;mysql-connector-j-9.7.0.jar" StudentRegistration
  ```

---

### 3. 🌐 Server-Client Networking (`Server-Client/`)
- **Description:** Real-time bidirectional socket communication between a TCP server and client using Java Networking (`java.net.Socket`, `java.net.ServerSocket`).
- **Key Components:**
  - `server.java` — TCP Server listening on a specified port.
  - `client.java` — TCP Client connecting to the server for data exchange.
- **How to Run:**
  - *Terminal 1 (Start Server):*
    ```bash
    cd serverclient
    javac server.java
    java server
    ```
  - *Terminal 2 (Start Client):*
    ```bash
    cd serverclient
    javac client.java
    java client
    ```

---

### 4. 📡 Remote Method Invocation (`RMI/`)
- **Description:** A distributed computing application demonstrating Java RMI (Remote Method Invocation) to execute methods across different JVM instances via `LocateRegistry`.
- **Key Components:**
  - `MyInterface.java` — Remote interface extending `java.rmi.Remote` that defines the callable remote method (`add(int, int)`).
  - `MyRemote.java` — Remote object implementation extending `UnicastRemoteObject` and implementing `MyInterface`.
  - `Server.java` — RMI server creating an RMI registry on port `1099` and binding the remote instance as `rmi://localhost/Add`.
  - `Client.java` — RMI client looking up the remote reference from the registry and invoking the remote addition method.
- **How to Run:**
  - *Terminal 1 (Start Server):*
    ```bash
    cd rmi
    javac *.java
    java Server
    ```
  - *Terminal 2 (Start Client):*
    ```bash
    cd rmi
    java Client
    ```

---

### 5. ⚡ Java Servlet Application (`servlet/`)
- **Description:** Dynamic server-side web application leveraging Java Servlets, JSP, and Apache Maven for build lifecycle management.
- **Technologies:** Java Servlets, Jakarta EE / Java EE, Maven, Apache Tomcat.
- **How to Run:**
  ```bash
  cd servlet
  mvn clean package
  ```
  Deploy the generated `.war` file to your Apache Tomcat `webapps/` directory.

---

### 6. 🛒 ShopSphere (`ShopSphere/`)
- **Description:** A comprehensive enterprise-grade e-commerce application integrating multiple Java architectures:
  - **Swing Admin Panel:** Desktop backoffice for inventory and order management.
  - **Web Storefront:** Servlet/JSP web interface for customer browsing and checkout.
  - **RMI (Remote Method Invocation):** Distributed business logic.
  - **Network Sockets:** Live notification/chat service.
  - **Database:** Full MySQL schema with relational constraints.
- **How to Run:**
  Refer to [`shopsphere/README.md`](shopsphere/README.md) for full setup instructions and database migration script (`database/shopsphere.sql`).

---

## 🛠️ Prerequisites

- **Java Development Kit (JDK):** JDK 17 or higher recommended.
- **Apache Maven:** 3.8+ (for `servlet` and `shopsphere` modules).
- **MySQL Server:** 8.0+ (for `student-registration` and `shopsphere`).
- **Apache Tomcat:** 9.x or 10.x (for servlet web deployment).
- **Git:** For version control.

---

## 📤 How to Add More Folders / Experiments

To add and push new lab folders or experiments to this repository:

1. **Create / Paste your folder** into the workspace root (e.g. `c:\Users\shubh\Desktop\java-lab1\new-experiment`).
2. **Add code files** into that folder (Git does not track completely empty folders).
3. **Stage, commit, and push** using PowerShell or Git Bash:
   ```bash
   git status
   git add .
   git commit -m "Add <folder-name> experiment"
   git push origin main
   ```
4. **Update `README.md`** to keep the structure and run instructions in sync!

---

## 👨‍💻 Author

- **Name:** Nishit Chugh
- **Email:** nishitchugh20@gmail.com
- **Repository:** [github.com/Nishit1956/Advanced-Java](https://github.com/Nishit1956/Advanced-Java)
