# Chainlit Chatbot using Gemini API

Welcome to the **Chainlit Chatbot** project! This chatbot is built with the **Chainlit framework**, uses **Gemini API** for language processing, and runs via **uv**, a fast Python package manager and runner. The result is a lightweight, modern conversational AI experience.

## Project Overview

This project implements a chatbot using **Chainlit**, with backend intelligence powered by **Gemini's API**. The chatbot is capable of:

- Answering user queries  
- Providing information on various topics  
- Engaging in natural, context-aware conversation

## Features

- **Real-time interactions** powered by Gemini's advanced language model  
- **Chainlit UI** for a smooth and interactive chat interface  
- **Minimal setup** with `uv` for dependency management and running  
- **Lightweight and scalable**, perfect for quick prototyping or production use

## Technologies Used

- **Chainlit** – Framework for building chat interfaces  
- **Gemini API** – Natural language processing backend  
- **uv** – Fast, modern Python package manager and runner

## Installation

To run the chatbot locally:

1. **Clone the repository**:

    ```bash
    git clone https://github.com/azfarsuhail/ChainLitChatbot.git
    ```

2. **Navigate to the project folder**:

    ```bash
    cd ChainLitChatbot
    ```

3. **Install dependencies with `uv`**:

    ```bash
    uv install
    ```

4. **Set your Gemini API key**:  
   Get your API key from [Gemini](https://geminiapi.com) and configure it in your environment variables or `.env` file.

5. **Run the chatbot**:

    ```bash
    uv run chainlit run main.py -w
    ```

## Example Usage

After launching, you'll be able to chat via the Chainlit UI.

**User**: "Tell me a fun fact."  
**Bot**: "Did you know honey never spoils? Archaeologists found pots of it in ancient Egyptian tombs!"

## Deployment

For detailed instructions on deploying this chatbot in local or production environments (including optional Docker setup), please refer to the [deployment.md](deployment.md) file included in this repository.

## Developer

- **Name**: Azfar Suhail  
- **GitHub**: [azfarsuhail](https://github.com/azfarsuhail)  
- **Email**: azfarsuhail2011@gmail.com  
- **LinkedIn**: [azfarsuhail](https://www.linkedin.com/in/azfarsuhail/)

## License

Licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Chainlit](https://www.chainlit.io) for a powerful chat interface framework  
- [Gemini API](https://geminiapi.com) for cutting-edge NLP capabilities  
- The open-source community for inspiration and support

---

### Disclaimer

This project is independently developed and is not affiliated with Gemini or its parent organizations. It simply uses Gemini's API for backend processing.