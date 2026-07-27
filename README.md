# 🏠 AI Weekly Instagram Post Generator for Rumah123

## Project Overview

This project automates the creation of weekly Instagram content for Rumah123 using AI and workflow automation.

Instead of manually searching for news, summarizing articles, writing captions, creating hashtags, and thinking about visual concepts, the workflow automates the entire process using n8n and GPT-4o-mini.

The generated output includes:

- Property news summary
- Instagram caption
- Relevant hashtags
- AI image generation prompt

The workflow is designed to reduce manual work for social media teams while maintaining consistent and engaging content.

---

## Workflow

Schedule Trigger
↓

Google News RSS (Property Indonesia)

↓

Filter Property News

↓

Remove Duplicate News

↓

Limit Latest Article

↓

AI News Summary

↓

AI Instagram Caption

↓

AI Hashtags

↓

AI Image Prompt

↓

Final Structured Output

---

## Technologies Used

- n8n
- OpenAI GPT-4o-mini
- Google News RSS
- JavaScript

---

## AI Usage

GPT-4o-mini is used to:

- Summarize property news
- Generate Instagram captions
- Generate hashtags
- Generate AI image prompts

The model was chosen because it provides a good balance between quality, speed, and cost.

---

## Challenges

### Duplicate News

Google News RSS often returns multiple articles discussing the same topic.

Solution:
A JavaScript node removes duplicate titles before sending data to the AI model.

---

### Irrelevant News

RSS may include general economic news.

Solution:
A keyword-based filtering node ensures only property-related news is processed.

---

### Structured AI Output

Instead of returning plain text, the workflow combines all AI-generated outputs into a structured JSON object, making it easier for future integrations.

---

## Future Improvements

- Auto-post to Instagram Graph API
- Canva API integration
- Generate Instagram Carousel content
- Generate Threads version
- Multi-language support
- AI ranking based on engagement prediction

---

## Repository Contents

workflow.json

Exported n8n workflow.

prompts.md

All prompts used in the AI nodes.

sample-output.md

Example generated output.

architecture.png

Workflow architecture diagram.

---

## Author

Created as part of the 99 Group AI Technical Assessment.
