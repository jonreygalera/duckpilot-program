# DuckPilot: The Ultimate Developer Workflow Manager

## What is DuckPilot?

DuckPilot is a comprehensive Windows desktop application built with Flutter, specifically designed to streamline developer workflows. It serves as a unified dashboard for managing local software projects, directly interacting with Windows Subsystem for Linux (WSL), and simplifying project creation through dynamic scaffolding and automated templates.

---

## Why use DuckPilot? (The Problem it Solves)

**The Beginner Perspective:**
When you are learning to code or building software, you often have to juggle many different tools. You might have to open a black terminal screen to create a folder, type complicated commands to download code, and then open another window to run your app. DuckPilot takes all of this confusing work and puts it into one beautiful, simple window. It makes setting up new projects and organizing your code as easy as clicking a few buttons!

**The Advanced Perspective:**
Modern local development environments—particularly those leveraging WSL 2 on Windows—often suffer from heavily fragmented workflows. Developers frequently context-switch between CLI terminals, file explorers, and various IDEs just for routine scaffolding, Git operations, and environment management. DuckPilot mitigates this friction by acting as a centralized control plane. It seamlessly orchestrates underlying shell operations, abstracts away repetitive boilerplate through a powerful YAML-driven template engine, and provides real-time observability of underlying WSL processes via an intuitive graphical user interface.

---

## Key Benefits

* **Unified Dashboard:** Manage, monitor, and search through all your active projects from a single, clean interface.
* **Deep WSL Integration:** Execute Linux commands directly from Windows without the typical path-resolution headaches. 
* **Dynamic Template Scaffolding:** Generate complex, multi-tiered project structures instantly using pre-defined blueprints and Backstage-style variables.
* **Git Clone Manager:** Seamlessly clone remote repositories directly into your designated WSL environment with automated configuration.
* **Automated WSL Authentication:** Optionally configure secure password injection to bypass manual `sudo` prompts during automated administrative tasks.
* **Always Up-to-Date:** Built-in webhooks and update services ensure you are always running the latest version directly from GitHub releases.
* **Resource Efficient:** Single-instance locking ensures the application never spawns redundant processes, keeping your memory usage low.

---

## How to Use DuckPilot

### For Beginners

1. **Launch the App:** Open DuckPilot from your Windows start menu or desktop shortcut.
2. **Set Up a Project:** Click the "New Project" button. You can choose to start from scratch using a pre-made template (like a starter website layout) or import a folder you already have.
3. **Manage Your Work:** You will see a list of cards for each of your projects. You can click these cards to instantly open a terminal exactly where your code lives, saving you from typing long directory paths.
4. **Settings:** Explore the settings tab to fill out your developer profile or check for app updates.

### For Advanced Users

1. **Configuring Default Paths:** Upon initial launch, navigate to the **Settings > General** tab to establish your Default WSL Path (e.g., `\\wsl$\Ubuntu\home\user\projects`). This directory acts as the root output for all subsequent scaffolding and cloning pipelines.
2. **Utilizing the Template Engine:** DuckPilot features a Backstage-inspired Template Execution Engine. When creating a new project, the engine parses custom YAML configuration files, performs recursive variable interpolation (utilizing syntax like `${{ values.appName }}`), and executes staged shell scripts to bootstrap your specific microservice or application architecture.
3. **WSL Security Auth:** Navigate to the **Security** tab to enable automated WSL authentication. By securely storing your WSL credentials in memory during the session, DuckPilot can automatically inject passwords into standard input (stdin) for workflows that require elevated `sudo` privileges.
4. **Terminal Actions:** Utilize the embedded Action Icons on any Project Card to immediately spawn a new CLI instance bound directly to that project's specific WSL mount point, utilizing `Process.start` for instantaneous context switching.
