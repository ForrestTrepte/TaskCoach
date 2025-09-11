# TaskCoach
Daily conversations to help me make the most of my time and energy.

## Continuation

When a conversation hits the maximum length:
1. Claude Settings > Privacy > Export data
2. Await email from Anthropic with link to download data
3. Unzip download, open command line in folder
4. Ensure [ai-chat-md-export](https://github.com/sugurutakahashi-1234/ai-chat-md-export) tool is installed (`npm install -g ai-chat-md-export`)
5. `ai-chat-md-export -i .\conversations.json -p claude`
6. Find and rename the most recent conversation's markdown file to conversation.md
7. Open a chat with [continuation.md](continuation.md), attaching prompt.md and conversation.md
8. Download the resulting artifiact (e.g. to `C:\s\TaskCoach`)
