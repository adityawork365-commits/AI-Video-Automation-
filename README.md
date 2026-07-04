# 🎬 AI Video Generation Workflow using n8n

> An end-to-end AI-powered automation workflow built with **n8n** that transforms structured job data into AI-generated images and videos through automated scripting, media generation, and API orchestration.

---

## 📌 Overview

This project demonstrates an advanced **n8n automation workflow** designed to automate the complete AI content generation pipeline.

Instead of manually writing prompts, generating images, creating videos, and managing outputs, this workflow automates the entire process from a single execution.

The workflow accepts structured input, processes job information, generates AI-ready scripts, prepares media metadata, creates images, triggers AI video generation, monitors the rendering process, and finally returns the completed output.

The project showcases practical usage of:

- AI Automation
- API Integration
- Data Transformation
- Workflow Orchestration
- Image Generation
- Video Generation
- Process Automation

---

# 🚀 Features

- ✅ Fully automated workflow
- ✅ Modular node architecture
- ✅ Structured input processing
- ✅ Dynamic script generation
- ✅ AI image generation
- ✅ AI video generation
- ✅ Automatic API integration
- ✅ Video rendering status tracking
- ✅ Local image storage
- ✅ Scalable workflow design
- ✅ Easy to customize
- ✅ Production-ready architecture

---

# 📸 Workflow Preview

> Overall workflow architecture

<img width="1605" height="491" alt="Screenshot 2026-07-04 231315" src="https://github.com/user-attachments/assets/9b26e09b-4ada-4b68-9740-80dbf2d4ec60" />


---

# 🏗 Workflow Architecture

The workflow is divided into multiple processing stages.

```
Start
      │
      ▼
Input Parameters
      │
      ▼
Get Job Data
      │
      ▼
Convert Jobs
      │
      ▼
Generate AI Script
      │
      ▼
Prepare Video Data
      │
      ├──────────────► Generate Image
      │                     │
      │                     ▼
      │              Save Image
      │                     │
      │                     ▼
      │              Final Output
      │
      ▼
Combine Jobs
      │
      ▼
Generate Video
      │
      ▼
Check Video Status
```

---

# ⚙️ Workflow Execution

## 1. Start Button

The workflow begins with a manual trigger.

This allows the user to execute the automation whenever required.

---

## 2. Input Parameters

This node collects all required parameters for the workflow.

Typical inputs may include:

- Prompt
- Job Details
- Scene Information
- Configuration Values
- Output Settings

These values are used throughout the workflow.

---

## 3. Get Job Data

The workflow retrieves the complete job information that will be processed.

This acts as the primary data source for the automation.

---

## 4. Convert Jobs

The incoming job data is transformed into a structured format.

Responsibilities include:

- Data formatting
- Cleaning
- Normalization
- Preparing items for iteration

---

## 5. Script Generator

This is one of the core components.

Using the processed job information, the workflow creates AI-ready scripts that will later be used for media generation.

Typical responsibilities:

- Generate prompts
- Build scene descriptions
- Organize content
- Prepare AI instructions

---

## 6. Prepare Video Data

Once the scripts are generated, the workflow prepares all required data before media generation.

Examples:

- Image prompts
- Video prompts
- Scene metadata
- Timing
- Processing payloads

---

## 7. Generate Image

The prepared prompt is sent to an AI image generation service.

The service generates images based on the provided prompt.

These images can later be used inside the generated video.

---

## 8. Save Image

Generated images are automatically stored locally using the Write File node.

This allows the workflow to preserve outputs for future usage.

---

## 9. Combine Jobs

Before video generation, all prepared data is merged into a single payload.

This ensures that every required asset is included before sending the final request.

---

## 10. Generate Real Video

The combined payload is sent to an external AI Video API.

The API starts rendering the final video.

Responsibilities:

- Build API payload
- Send HTTP Request
- Receive Job ID
- Start rendering process

---

## 11. Check Video Status

Video generation usually takes time.

Instead of finishing immediately, the workflow periodically checks the rendering status until the final video becomes available.

---

## 12. Final Video Output

The workflow returns the final processed output.

Depending on configuration this may include:

- Generated Images
- Video Information
- Render Status
- File URLs
- Metadata

---

# 🔄 End-to-End Workflow

```
User Starts Workflow
        │
        ▼
Input Parameters
        │
        ▼
Load Job Data
        │
        ▼
Convert Data
        │
        ▼
Generate AI Script
        │
        ▼
Prepare Video Payload
        │
        ├────────► AI Image Generation
        │               │
        │               ▼
        │          Save Images
        │
        ▼
Combine Data
        │
        ▼
Generate AI Video
        │
        ▼
Check Render Status
        │
        ▼
Return Final Output
```

---

# 📦 Technologies Used

- n8n
- JavaScript
- HTTP Request Nodes
- Data Transformation
- REST APIs
- AI Image Generation
- AI Video Generation
- Workflow Automation

---

# 📁 Project Structure

```
AI-Video-Generation/

│
├── README.md
│
├── workflow/
│     workflow.json
│
├── images/
│     workflow.png
│
├── .env.example
│
├── LICENSE
│
└── docs/
```

---

# 📥 Installation

Clone the repository

```bash
git clone https://github.com/yourusername/AI-Video-Generation.git
```

Open n8n.

Import the workflow JSON file.

Configure all required credentials.

Run the workflow.

---

# 📤 Import into n8n

1. Open n8n
2. Click **Import Workflow**
3. Select `workflow.json`
4. Configure credentials
5. Save
6. Execute

---

# 🔐 Configuration

Before running the workflow, configure:

- AI API Credentials
- HTTP Request Authentication
- Output Directory
- Required Environment Variables

---

# 📄 Example Folder

```
workflow/

    workflow.json
```

```
images/

    workflow.png
```

---

# 💡 Benefits

This workflow helps automate repetitive content creation tasks by reducing manual effort and connecting multiple AI services into one seamless pipeline.

Key advantages include:

- Faster content generation
- Reduced manual work
- Consistent output
- Easy integration with external APIs
- Scalable architecture
- Modular and reusable design
- Suitable for real-world AI automation projects

---

# 🚀 Future Improvements

- Multiple AI provider support
- Retry mechanism
- Error notifications
- Cloud storage integration
- Database logging
- Queue management
- Batch processing
- Multi-language support
- Dashboard integration

---

# 👨‍💻 Author

**Aditya Gour**

GitHub: https://github.com/yourusername

LinkedIn: https://linkedin.com/in/yourprofile

---

# 📜 License

This project is licensed under the MIT License.

---

⭐ If you found this project useful, consider giving it a star on GitHub.
