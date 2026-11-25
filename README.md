# 🎮 KBC: General Knowledge Quiz Game
### A Java Swing Quiz Application Inspired by "Kaun Banega Crorepati"

> ⚠️ **DISCLAIMER:** This is a **personal learning and portfolio project**. It is a desktop quiz application built with Java Swing for educational and demonstration purposes. All questions, answers, and graphics are compiled from public sources. This is **NOT** an official application of "Kaun Banega Crorepati" (KBC), Sony Entertainment, or any affiliated organization.

A fully functional, GUI-based quiz game built with Java Swing. It features a complete flow from user registration/login to a progress loader, a five-question multiple-choice quiz with immediate feedback, and a "Congratulations" screen for successful candidates. Designed with a bold, colorful UI reminiscent of the classic KBC television show.

![Version](https://img.shields.io/badge/Version-1.0.0-ED8B00)
![Status](https://img.shields.io/badge/Status-Portfolio%20Project-F4B400)
![Platform](https://img.shields.io/badge/Platform-Desktop%20%28Java%20Swing%29-2D6A4F)

---

## 🔗 Links

- **Source Code:** [github.com/Ashish22Gupta/Basic_General_knowledge_question](https://github.com/Ashish22Gupta/Basic_General_knowledge_question)

> 💡 *No live demo — this is a desktop application. Clone the repo and run it locally with JDK + NetBeans.*

---

## ✨ Implemented Features

### 🔐 Authentication Flow
- **Start Screen** — Choose between "Already Registered" and "New User".
- **Login Form** — Basic credential validation (default: `admin` / `pass`).
- **Registration Form** — Username, Password, and Confirm Password fields with mismatch validation.

### ⏳ Progress Loader
- **Animated JProgressBar** — A "Best of Luck For Your Exam" screen with a progress bar that fills from 0% to 100%.
- **Threaded Animation** — Uses a background thread (`Thread.sleep(80)`) to update the progress bar without freezing the UI.
- **Automatic Transition** — Automatically navigates to the first question when the progress bar reaches 100%.

### 🧠 5-Question Quiz
- **Question Sequence** — Five general knowledge questions, each with four multiple-choice options.
- **Radio Button Input** — `ButtonGroup` ensures only one option can be selected per question.
- **Immediate Feedback** — Correct answers advance to the next question; incorrect answers display "You Are Fail, Please Try Next Time".
- **Fail-Safe Exit** — A wrong answer ends the quiz immediately.

### 🏆 Success Screen
- **Congratulations Message** — Displays "Thank you for giving the simple aptitude test", "You have Successfully cleared the aptitude test", and "Now you are eligible for the next round".
- **Dynamic Image Loading** — Loads a `cong.jpg` image and scales it using `Image.SCALE_SMOOTH`.

### 🎨 Bold Visual Design
- **Blue Theme** — Login/Register screens use a vibrant `#3366FF` background.
- **Purple Theme** — Quiz screens use a bold `#9933FF` background.
- **Custom Typography** — `SimSun` and `Segoe UI` fonts at various sizes.
- **Color-Coded Elements** — Cyan labels, magenta input fields, and red error text for strong contrast.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **Java (JDK 8+)** | Core language — event handling, `JFrame`, `ActionListener` |
| **Java Swing** | `JFrame`, `JPanel`, `JButton`, `JTextField`, `JRadioButton`, `JProgressBar` |
| **Java AWT** | `Image`, `ImageIcon`, `Font`, `Color` |
| **Apache Ant** | Build automation via `build.xml` |
| **NetBeans IDE** | GUI Builder for form layouts |

---

## 📁 Project Structure

```text
Basic_General_knowledge_question/
├── src/
│   └── kbc/
│       ├── START.java               # Landing: Already Registered / New User
│       ├── Already_register.java    # Login form
│       ├── Registeration_form.java  # Registration form
│       ├── process1.java            # "Start My Progress" trigger
│       ├── Process_frame.java       # Animated progress bar screen
│       ├── question1.java           # Question 1
│       ├── question2.java           # Question 2
│       ├── question3.java           # Question 3
│       ├── question4.java           # Question 4
│       ├── question5.java           # Question 5
│       └── Thanks.java              # Congratulations screen
│
├── build.xml                        # Ant build script
└── nbproject/                       # NetBeans project metadata
