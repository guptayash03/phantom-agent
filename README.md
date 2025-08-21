🤖 AI Automation Agent for Social Media ie., Instagram, Linkedin, Reddit, Twitter
An intelligent agent that automates the creation and publication of engaging content for various social media platforms like Instagram, LinkedIn, Twitter, and Reddit.

📜 Overview
The AI Co-Creator is a powerful Agent designed to streamline your social media content strategy. By simply providing a title or a topic, the application leverages a sophisticated multi-agent system to generate high-quality, platform-specific posts complete with relevant hashtags and compelling images. It then automates the entire process, from content creation to direct publishing on your selected social media channels, saving you time and effort while boosting your online presence.

🛠️ Tech Stack
This project is built with a modern, robust technology stack to ensure a seamless and powerful user experience.

Frontend:

Next.js: A React framework for building fast, server-rendered applications.

Tailwind CSS: A utility-first CSS framework for rapid UI development.

Shadcn/ui: A collection of beautifully designed, reusable components.

Backend & AI Orchestration:

Python: The core language for our backend logic and AI agents.

LangChain: A framework for developing applications powered by language models.

LangGraph: A library for building stateful, multi-actor applications with LLMs.

n8n: A workflow automation tool to connect various services and APIs.

CrewAI: A framework for orchestrating role-playing, autonomous AI agents.

APIs & Services:

OpenAI: For state-of-the-art text and image generation.

Google APIs: For various integrations, potentially including Google Sheets for content scheduling or analytics.

Meta API: For posting to Instagram and Facebook.

LinkedIn API: For publishing content on LinkedIn.

Twitter (X) API: For automated tweeting.

Reddit API: For posting to relevant subreddits.

✨ Features
Automated Workflow Trigger: Kickstart the content creation process automatically based on predefined triggers (e.g., a new entry in a Google Sheet).

Platform-Specific Content Generation: The AI agent intelligently crafts content tailored to the tone, style, and character limits of each social media platform.

Intelligent Hashtag Creation: Automatically generates relevant and trending hashtags to maximize reach and engagement.

AI-Powered Image Generation: Creates unique, contextually relevant images to accompany the text posts.

Direct Platform Upload: Seamlessly posts the generated content directly to your connected social media accounts.

Approval Workflow: Includes an optional email-based approval step to review and confirm content before it goes live.

⚙️ Technical Workflow
The application operates through a sophisticated, event-driven workflow orchestrated by n8n and powered by AI agents.

Trigger Event: The process begins with a trigger, such as a webhook or a new row added to a Google Sheet containing the post title.

Content Generation:

The title is passed to an AI agent (built with LangChain/CrewAI) that generates the main body of the post.

The initial text is then formatted and tailored for each target platform (LinkedIn, Twitter, etc.).

Approval (Optional): An email is sent to a designated approver with the generated content. The workflow pauses until the content is confirmed.

Image Generation:

Once the text is finalized or approved, a prompt is sent to an image generation model (like DALL-E via OpenAI API) to create a relevant visual.

The system checks if an image was successfully generated.

Publishing:

The formatted text and the generated image are sent to the respective social media platform APIs (LinkedIn, Twitter, etc.) for publishing.

Logging & Confirmation: The status of the post (e.g., "Posted Successfully") is updated in the original data source, like the Google Sheet, for tracking purposes.
