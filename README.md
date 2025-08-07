# 🚬 Chain Smoker Synchronization Problem — Console Simulation in C++

### 📌 Description
This project is a console-based C++ simulation of the classic **Chain Smoker Synchronization Problem**, which I developed as part of an Operating Systems course. It uses **POSIX threads and semaphores** to simulate a scenario involving **one agent and three smokers**, each needing specific ingredients to make a cigarette. The simulation demonstrates how synchronization and mutual exclusion can be achieved using semaphores.

### 🎯 Objectives
- To demonstrate multithreading and synchronization using semaphores in C++.
- To simulate real-world concurrency using the Chain Smoker problem.
- To learn deadlock prevention and inter-thread communication.

---

### 🧠 The Problem — In Short

- There are **3 smokers**, each with an **infinite supply** of one item:
  - Smoker 1 → Tobacco
  - Smoker 2 → Matches
  - Smoker 3 → Paper
- The **agent** randomly places 2 of the 3 items on the table.
- The smoker who has the **third item** picks up the other two, **makes a cigarette**, and **smokes**.
- This process continues until all smokers have smoked **7 times each**.

---

### 🛠 Technologies & Concepts Used

| Component        | Description |
|------------------|-------------|
| **C++**           | Main language used |
| **POSIX Threads** (`pthread`) | To create concurrent smoker and agent threads |
| **Semaphores** (`sem_t`) | To synchronize access between agent and smokers |
| **Linux Terminal** | Console-based colored output using ANSI escape codes |
| **Random Delays** | Introduces realistic interleaving of threads using `usleep` and `sleep` |

---

### 📁 File Structure

├── console_version_chainsmoker.cpp        # Main program file<br>
├── Project Report.pdf                     # Detailed explanation of logic and implementation<br>
├── Screenshot.png                         # Console output snapshot<br>
└── README.md                              # You're reading it!

---

### 🖥️ Screenshot

<img width="1366" height="672" alt="Screenshot" src="https://github.com/user-attachments/assets/694eff71-c8bc-42e6-9e0d-408b0e203ac3" />

> This screenshot shows the real-time interaction of smokers and the agent with colorful terminal outputs.

---

### 📦 How to Compile and Run

> ✅ I tested it on **Linux (Ubuntu)** and it will also work on other POSIX-compliant systems like **macOS**, **WSL**, etc.

#### 🔧 Dependencies
Make sure you have the following installed:
- `g++` compiler
- POSIX thread and semaphore support

#### 🚀 Compile
g++ console_version_chainsmoker.cpp -o console_version_chainsmoker -lpthread

▶️ Run<br>./console_version_chainsmoker

---

📊 Output Explanation

During execution, you will see:

- Which smoker is waiting for which items.
- What ingredients the agent throws.
- Which smoker is currently making and smoking a cigarette.
- Color-coded output for visual clarity.

Example log:

Smoker 1 waiting for paper & matches<br>==> Smoker1 is making a cigarette<br>Now Smoking

---

📚 Project Report<br>For a complete breakdown of:

- Libraries and their usage
- Threading model
- Synchronization logic

Limitations and improvements<br>📄 Read the full Project Report (PDF)

---

💡 Key Learnings

- Implementing inter-thread communication using semaphores.
- Handling race conditions and synchronization in concurrent systems.
- Modeling real-world OS problems in a simplified console simulation.

---

🧪 Tested On<br>
| OS        | Status |
|------------------|-------------|
| ✅ Linux           | ✔️ Fully Functional |
| ✅ WSL (Windows Subsystem for Linux) | ✔️ Functional |
| ❌ Native Windows | ❌ Not supported (POSIX threads not available natively) |

---

🙋‍♂️ Author<br>Muhammad Ashir<br>Student of FAST-NUCES, Karachi<br>For contributions or queries, feel free to connect on LinkedIn [linkedin.com/in/ashir-qayyum]

---

📜 License<br>This project is licensed for educational and academic use. Attribution appreciated.
