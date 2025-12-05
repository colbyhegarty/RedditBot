# Reddit Story Accessibility Tool

This project provides a simple, API-compliant application that reads a small number of public Reddit posts and generates accessibility-friendly summaries or audio versions for personal consumption. The purpose of the tool is to help users who prefer listening or who benefit from summarized content discover posts they may have missed while still directing engagement back to Reddit.

All content retrieved through the Reddit Data API comes from public subreddits only.  
No private data, direct messages, or user-specific information is accessed.

---

## 🔍 Purpose

Many Redditors enjoy long-form posts and discussions, but not everyone has time or the ability to read large amounts of text.  
This tool helps by:

- Fetching a small set of **top daily/weekly posts** from specific subreddits.
- Generating short **summaries**.
- Offering optional **text-to-speech audio** for accessibility.
- Providing links back to the **original Reddit posts**.

The application does **not** post, comment, vote, or automate any user actions on the Reddit platform.

---

## ⚙️ How It Works

1. Reads top posts from selected subreddits (e.g., AskReddit, AITA, TrueOffMyChest).
2. Extracts the title and body if available.
3. Generates a summary or optional audio narration.
4. Outputs the results locally with direct links to Reddit.

All API usage stays within Reddit's rate limits and Responsible Builder Policy guidelines.

---

## 🛠 Tech Stack

- Python 3.10+
- Reddit API via PRAW or HTTP requests
- Optional: TTS library for audio output
- Optional: Simple video composer for personal accessibility use

---

## 📄 Example Configuration

The project uses an example config file to map which subreddits to read and how many posts to fetch.

```json
{
  "subreddits": ["AskReddit", "relationship_advice", "TrueOffMyChest"],
  "limit": 3,
  "output_audio": false
}
