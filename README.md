# LandingAi
1. Project Overview
This project is a simple AI system that improves existing landing pages based on an
advertisement message.
The main idea is very practical, Instead of creating a completely new landing page,
the system takes an existing page and enhances it so that it better matches the
advertisement and improves conversions.
For example, if an ad says “50% OFF Shoes”, the system modifies the landing page
to highlight urgency, discounts, and stronger call-to-action buttons, while still keeping
the original product and meaning intact.
2. How the System Works
The system works in a very straightforward flow:
First, the user enters two inputs:
● An ad creative (example: promotional message or offer)
● A landing page URL
Then the system extracts important information from the landing page like title,headings, and text content.
After that, this information is passed to an AI model along with the ad text. The AI
behaves like a CRO (Conversion Rate Optimization) expert and rewrites parts of the
page to improve engagement and conversion.
Finally, the system shows:
● The original page content
● The improved AI version
● A comparison of conversion score before and after optimization
So the user can clearly see what changed and why it was improved.
3. Key Components / Agent Design
The system is built using a few simple but important components:
3.1 Scraper Module
This part collects content from the landing page. It extracts things like:
● Page title
● Headings (h1, h2)
● Paragraph content
This helps the AI understand what the page is about.
3.2 AI CRO Engine
This is the main part of the system.
It acts like a “conversion expert” and:
● Understands the advertisement intent
● Identifies what can be improved on the page
● Writes better headlines and CTAs
● Adds urgency and clarity where needed
It ensures the page is improved without changing the actual product or meaning.
3.3 Scoring System
There is a simple scoring system that checks how strong the content is for
conversions.
It looks at things like:
● presence of urgency words (like “limited”, “now”)
● call-to-action strength (like “shop now”, “buy now”)
● promotional signals (like “discount”, “% off”)
Based on this, it gives a score before and after AI improvement.
3.4 Frontend Interface
A simple Gradio interface is used where users can:
● Enter ad text
● Enter URL
● Click generate
● View original vs optimized page
This makes the system easy to test and demo
4. How I Handled Common Problems?
4.1 Random Changes in AI Output
Sometimes AI can generate unpredictable or inconsistent results. To avoid this, I
strictly control the output format using a fixed structure (headline, CTA, section, etc.).
I also applied fallback values if anything is missing, so the system never breaks.
4.2 Broken UI Issues
Web pages sometimes fail to load properly or return incomplete data. To handle this,
I always check if the scraped data is empty.
If something is missing, I have replaced it with safe default values like “Untitled
Page” or “No content available” so the UI still works smoothly.
4.3 Hallucinations (Fake or Wrong Content)
I made sure the AI does not invent new products or change the meaning of the page.
I clearly instruct the model to:
● only improve existing content
● not create new products or services
● stay aligned with the original page context
This keeps outputs realistic and usable.
4.4 Inconsistent Outputs
AI outputs can sometimes vary in format. To solve this, I did not rely on strict JSON.
Instead, I have used a structured text format and parse it safely. I have also used
fallback logic so even incomplete outputs are still usable.
5. Final Understanding
Overall, this project shows how AI can be used in a simple but practical way to
improve marketing landing pages.
Instead of redesigning everything manually, the system automatically enhances
clarity, urgency, and conversion focus based on user intent.
It is a lightweight prototype, but it demonstrates real-world use of AI in CRO and
digital marketing.
