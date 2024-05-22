---
cover: >-
  .gitbook/assets/DALL·E 2024-05-22 11.22.25 - Create a banner image for a
  GitBook titled 'RLU_ Rust Logseq Utility'. The design should be modern and
  clean, featuring the Rust programming language .webp
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# rlu - Rust Logseq Utility

`rlu` is a Rust-based command-line utility designed to interact with Logseq, a privacy-first, open-source knowledge base that works on top of local Markdown and Org-mode files. This utility provides various functionalities for managing content in Logseq.

### Table of Contents

* [Features](https://flowise.fluentcli.com/agentcanvas/d170e885-f0d6-42f1-b27f-8fe6c579ac64#features)
* [Installation](https://flowise.fluentcli.com/agentcanvas/d170e885-f0d6-42f1-b27f-8fe6c579ac64#installation)
* [Usage](https://flowise.fluentcli.com/agentcanvas/d170e885-f0d6-42f1-b27f-8fe6c579ac64#usage)
* [Dependencies](https://flowise.fluentcli.com/agentcanvas/d170e885-f0d6-42f1-b27f-8fe6c579ac64#dependencies)
* [Contributing](https://flowise.fluentcli.com/agentcanvas/d170e885-f0d6-42f1-b27f-8fe6c579ac64#contributing)
* [License](https://flowise.fluentcli.com/agentcanvas/d170e885-f0d6-42f1-b27f-8fe6c579ac64#license)

### Features

* **Add Journal Entries**: Add new entries to your Logseq journal.
* **Show Journal Entries**: Display entries for specific dates.
* **Get Journal Entry**: Retrieve a specific entry by ID.
* **Output Entry Content**: Display the full content of a specific entry.
* **Add Content**: Add content to existing entries.
* **Add Child Node**: Add a child node to an existing entry.
* **Delete Entry**: Delete a specific entry.

### Installation

1. Ensure you have Rust installed.
2.  Clone the rlu repository:

    ```bash
    bashgit clone https://github.com/yourusername/rlu.git
    ```
3.  Build the project using Cargo:

    ```bash
    bash
    cd rlu 
    cargo build --release // or cargo install --path .
    ```

### Usage

#### Commands

*   **Add a Journal Note**:

    ```bash
    bashrlu add --content "Your journal content" --date "2023-10-05"
    ```
*   **Show Journal Entries**:

    ```bash
    bashrlu show --date "2023-10-05"
    ```
*   **Get Journal Entry**:

    ```bash
    bashrlu get --entry_id "entry-uuid"
    ```
*   **Output Entry Content**:

    ```bash
    bashrlu output-content --entry_id "entry-uuid"
    ```
*   **Add Content to Start**:

    ```bash
    bashrlu add-to-start --entry_id "entry-uuid" --content "New start content"
    ```
*   **Append Content to End**:

    ```bash
    bashrlu append-to-end --entry_id "entry-uuid" --content "New end content"
    ```
*   **Add Child Node**:

    ```bash
    bashrlu add-child-node --entry_id "parent-id" --content "Child node content"
    ```
*   **Delete Entry**:

    ```bash
    bashrlu delete --entry_id "entry-uuid"
    ```

#### Environment Variables

Set the following environment variables:

* `LOGSEQ_API_URL`: URL for the Logseq API (default: `http://127.0.0.1:12315/api`).
* `LOGSEQ_API_KEY`: Your Logseq API key for authorization.

### Dependencies

* `reqwest`
* `serde` and `serde_json`
* `chrono`
* `clap`
* `log` and `env_logger`

### Contributing

Contributions are welcome! Fork the repository and submit a pull request for enhancements or bug fixes.

### License

This project is licensed under the MIT License. See the [LICENSE](https://flowise.fluentcli.com/agentcanvas/LICENSE) file for details.

***

This Gitbook provides an overview of the rlu application, its features, installation instructions, usage guide, dependencies, contribution guidelines, and licensing information.

Feel free to explore the rlu application further on the GitHub repository: [rlu GitHub Repository](https://github.com/njfio/rlu).
