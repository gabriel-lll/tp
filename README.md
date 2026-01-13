<div align="center">

# AbsolutSin-ema

### The Ultimate Contact Manager for Party Planners

[![CI Status](https://github.com/AY2526S1-CS2103T-T12-4/tp/workflows/Java%20CI/badge.svg)](https://github.com/AY2526S1-CS2103T-T12-4/tp/actions)
[![codecov](https://codecov.io/gh/AY2526S1-CS2103T-T12-4/tp/branch/master/graph/badge.svg)](https://codecov.io/gh/AY2526S1-CS2103T-T12-4/tp)
[![Java](https://img.shields.io/badge/Java-17-orange.svg)](https://openjdk.java.net/projects/jdk/17/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

[**Download**](https://github.com/AY2526S1-CS2103T-T12-4/tp/releases) • [**Documentation**](https://ay2526s1-cs2103t-t12-4.github.io/tp/) • [**User Guide**](https://ay2526s1-cs2103t-t12-4.github.io/tp/UserGuide.html) • [**Developer Guide**](https://ay2526s1-cs2103t-t12-4.github.io/tp/DeveloperGuide.html)

</div>

---

![UI Screenshot](docs/images/Ui.png)

## ✨ What is AbsolutSin-ema?

**AbsolutSin-ema** is a powerful desktop application designed specifically for **party planners** and **event coordinators** who need to manage contacts and events efficiently. Combining the speed of a **Command Line Interface (CLI)** with the visual appeal of a modern **Graphical User Interface (GUI)**, AbsolutSin-ema helps you organize vendors, track budgets, and coordinate events faster than ever.

### 🎯 Perfect For

| User Type | Use Case |
|-----------|----------|
| **Student Organizers** | Managing dorm parties, graduation events (20-100 guests) |
| **Corporate Event Coordinators** | Company parties, team building events (50-500 attendees) |
| **Freelance Party Planners** | Weddings, birthdays, celebrations for clients |
| **Venue Managers** | Coordinating multiple events with vendors and suppliers |

## 🚀 Key Features

- **⚡ Lightning-Fast Contact Management** — Add, edit, find, and organize contacts with simple CLI commands
- **🎉 Party & Event Planning** — Create parties, set budgets, assign vendors, and track everything in one place
- **💰 Smart Budget Tracking** — Monitor spending per party and get alerts when you're approaching limits
- **🔍 Powerful Search** — Find contacts instantly by name or tag
- **↩️ Undo Support** — Made a mistake? One command to undo your last action
- **🏷️ Tag System** — Organize contacts with custom tags (DJ, catering, decorations, etc.)
- **💾 Auto-Save** — Your data is automatically saved after every change

## 📦 Installation

### Prerequisites

- **Java 17** or higher ([Download JDK 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html))

### Quick Start

1. Download the latest `absolutsinema.jar` from [Releases](https://github.com/AY2526S1-CS2103T-T12-4/tp/releases)
2. Move the file to your desired folder
3. Open a terminal and navigate to that folder
4. Run the application:

```bash
java -jar absolutsinema.jar
```

5. The application window should appear with sample data

## 🎮 Quick Tutorial

Plan your first party in under 2 minutes:

```bash
# Add some vendors
add n/DJ Mike p/91234567 e/mike@music.com b/800 t/dj
add n/Bella's Catering p/87654321 e/orders@bella.com b/1200 t/catering
add n/Party Supplies Plus p/76543210 e/info@partysupplies.com b/300 t/decorations

# Create a party and assign vendors
addp n/Sarah's Birthday d/25-12-2025 t/19:00 b/2500 c/1,2,3

# View your party details
view 1

# Find a specific vendor
find dj
```

## 📋 Command Reference

| Command | Description | Example |
|---------|-------------|---------|
| `add` | Add a new contact | `add n/John p/98765432 e/john@email.com b/500 t/vendor` |
| `edit` | Edit a contact | `edit 1 p/91234567 b/600` |
| `delete` | Delete a contact | `delete 3` |
| `find` | Find contacts by name or tag | `find catering` |
| `list` | List all contacts | `list` |
| `listtags` | List all tags | `listtags` |
| `addp` | Add a party | `addp n/Wedding d/15-06-2025 t/14:00 b/10000` |
| `editp` | Edit a party | `editp 1 b/12000` |
| `deletep` | Delete a party | `deletep 2` |
| `assign` | Assign contacts to party | `assign 1 c/1,2,3` |
| `unassign` | Remove contacts from party | `unassign 1 c/2` |
| `view` | View party details | `view 1` |
| `undo` | Undo last command | `undo` |
| `clear` | Clear data | `clear all` / `clear contacts` / `clear parties` |
| `help` | Show help | `help` |
| `exit` | Exit application | `exit` |

> 📖 For detailed command documentation, see the [User Guide](https://ay2526s1-cs2103t-t12-4.github.io/tp/UserGuide.html)

## 🏗️ Architecture

AbsolutSin-ema follows a clean, layered architecture:

```
┌─────────────────────────────────────────────────┐
│                      UI                         │
│            (JavaFX-based interface)             │
├─────────────────────────────────────────────────┤
│                    Logic                        │
│         (Command parsing & execution)           │
├─────────────────────────────────────────────────┤
│                    Model                        │
│      (Data structures & business logic)         │
├─────────────────────────────────────────────────┤
│                   Storage                       │
│           (JSON file persistence)               │
└─────────────────────────────────────────────────┘
```

## 🛠️ Development

### Building from Source

```bash
# Clone the repository
git clone https://github.com/AY2526S1-CS2103T-T12-4/tp.git
cd tp

# Build the project
./gradlew build

# Run tests
./gradlew test

# Run the application
./gradlew run
```

### Project Structure

```
src/
├── main/
│   ├── java/seedu/address/
│   │   ├── commons/     # Shared utilities
│   │   ├── logic/       # Command parsing & execution
│   │   ├── model/       # Data models (Person, Party, etc.)
│   │   ├── storage/     # JSON persistence
│   │   └── ui/          # JavaFX UI components
│   └── resources/
│       ├── images/      # Application icons
│       └── view/        # FXML layouts & CSS styles
└── test/                # JUnit test cases
```

## 📚 Documentation

| Document | Description |
|----------|-------------|
| [User Guide](https://ay2526s1-cs2103t-t12-4.github.io/tp/UserGuide.html) | Complete guide for end users |
| [Developer Guide](https://ay2526s1-cs2103t-t12-4.github.io/tp/DeveloperGuide.html) | Technical documentation for developers |
| [About Us](https://ay2526s1-cs2103t-t12-4.github.io/tp/AboutUs.html) | Meet the team |

## 🤝 Contributing

We welcome contributions! Please see our [Developer Guide](https://ay2526s1-cs2103t-t12-4.github.io/tp/DeveloperGuide.html) for:

- Setting up the development environment
- Code style guidelines
- Testing requirements
- Pull request process

## 👥 Team

- Gabriel Ponce Simundo
- Rahul Mallavarapu
- Josh Loh
- Yoson Teo
- Lin Tao

## 🙏 Acknowledgements

- Built upon [AddressBook Level 3](https://se-education.org/addressbook-level3/) by [SE-EDU](https://se-education.org)
- Libraries: [JavaFX](https://openjfx.io/), [Jackson](https://github.com/FasterXML/jackson), [JUnit5](https://github.com/junit-team/junit5)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**Made with ❤️ for party planners everywhere**

[⬆ Back to top](#absolutsin-ema)

</div>

