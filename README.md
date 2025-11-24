# UI/UX Reviewer | Azure Frontier Girls Challenge

## 📘 Overview
This project provides an AI-powered assistant capable of reviewing screenshots of websites, apps, dashboards, or other user interfaces.  
The agent analyzes layout, visual hierarchy, usability factors, and accessibility concerns, then suggests clear and concise improvements.

The evaluation is based on the following prompt:

```
You are a UI/UX design assistant. The user will upload screenshots of websites,
apps, dashboards, or interfaces. You must evaluate the image and then:

1. Analyze UI elements: buttons, text inputs, titles, images, icons thinking about user experience (i. e. element size, colors, clickable area, page design) - do not list them. you'll describe shortly your evaluation
2. Suggest improvements you consider necessary.

Always be concise and clear.
For topics, use sequential numbers
```

---

## 🖼️ How to Capture High-Quality Screenshots

To ensure accurate UI/UX evaluation, capture screenshots directly from your browser’s Developer Tools. This avoids browser chrome, improves resolution, and produces a clean image of the rendered UI.

### Steps

1. Open the website or web application you want to evaluate.
2. Right-click anywhere on the page and select **Inspect** (or press `F12`).
3. In the **Elements** panel, locate the root `<html>` element.
4. Right-click the `<html>` node and select:  
   - **Capture node screenshot** (Chrome), or  
   - **Screenshot Node** (Firefox)  
5. Your browser will save a clean, full-resolution screenshot of the rendered page.

This method ensures the screenshot:
- Contains no browser UI  
- Has no scrollbars  
- Reflects the exact DOM-rendered layout  
- Provides pixel-perfect detail for UI/UX review  

---

## 📤 How to Upload the Screenshot for Evaluation

Follow these steps to submit a screenshot to the AI agent:

1. Open the Agent interface in **Azure AI Foundry**.
2. Click the **Upload File** (attachment) icon in the input area.
3. Select your `.png` or `.jpg` screenshot file.
4. Add a message such as:
   - “Please evaluate this UI.”  
   - or “Provide UX improvement suggestions for this layout.”  
5. Submit your message.
6. The agent will:
   1. Analyze the UI using UX heuristics.  
   2. Provide a brief, non-exhaustive evaluation.  
   3. Suggest improvements using sequentially numbered points.  

---

## 🧠 How It Works

1. You upload a screenshot.  
2. The agent sends the image to **Azure AI Vision** for analysis.  
3. The LLM interprets the visual structure using the defined prompt.  
4. The agent returns a concise UI/UX evaluation and actionable suggestions.

---

## 📁 Project Structure

```
/ui-ux-review-agent
├── README.md        # Documentation
├── agent-config/    # System prompt, tools, and model settings
├── examples/        # Sample screenshots for testing
└── frontend/        # Optional UI for uploading and reviewing images
```

---

## 🚀 Getting Started

1. Clone or download this project.  
2. Open your Azure AI Foundry workspace.  
3. Create an Agent and paste the provided prompt.  
4. Add the Azure Vision HTTP tool for image analysis.  
5. Test by uploading a screenshot and reviewing the agent’s response.

---

- 🇧🇷 Versão em Português: [README.pt-BR.md](README.pt-BR.md)

