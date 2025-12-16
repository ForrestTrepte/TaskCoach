# TaskCoach

Daily conversations to help me make the most of my time and energy.

## The experiment

Will chatting with an LLM each morning to plan my tasks for the day help me to be more disciplined and productive?

Each workday for 6 weeks (TODO) I chatted with Claude Desktop. This included personal tasks (TODO examples) and professional tasks (including this project itself, creating/enhancing the prompt, setting up/enhancing the tasks MCP server).

During this time I wasn't employed, so I didn't have the natural pull of work colleagues and work initiatives that needed to be completed. Left to my own devices, tasks feel less urgent, and I was looking for help with motivation and discipline.

Results:
1. Increased discipline due to feeling of accountability. Valuable to establish a habit of planning daily tasks and setting goals. Could have done this without an LLM, but having an external entity created a feeling of accountability. I genuinely wanted to show the LLM coach that I had completed the tasks that I had committed to. And writing them down prevented me slacking off early, saying "good enough" for the day when I hadn't completed everything I set out to do.
2. LLM assistance with organization was mildly helpful. Task list integration worked extremely well once the kinks were worked out. Calendar integration was occasionally helpful (for context of a busy day or appointments related to tasks already on the schedule), but usually calendar integration wasn't essential for me probably because my schedule isn't too hectic.
3. LLM insight was minimal. I imagined that the LLM might have deep insight about how to organize tasks, better ways of working, anti-procrastination techniques, or help recognizing and tackling things that I was avoiding. In practice, there was *some* useful insight from the LLM (see [Insights](insights.md) for examples), but little that I wasn't already aware of. Not sure what I was expecting when the LLM doesn't really know me and has a limited windows into my life, how I work, and only a few words that I've jotted down about each task.

Of these, #1 was *by far* the most helpful. #2 and #3 are mildly nice, but #1 is the reason I intend to continue using TaskCoach going forward.

## Helpful patterns

* I found a useful pattern for representing blocked issues. Track tasks that can't be worked on right now because they are waiting from somebody else to do something or for something external to happen. Create a subtask representing the point that I reached and a subtask with the next step and due date when I expect to pick it up again. Often, I include the word "await" in a task to indicate that I'm waiting on something.
* An option to consider when not finishing a task is to split off the part that was completed and create a task for the remaining. Less clear if this is a good idea--satisfaction of checking it off when not really complete yet. Perhaps better to leave uncompleted and discuss remaining part in planning?

(TODO scan prompt for additional helpful patterns)

## The Technology

Claude desktop
Google task list integration via google_workspace_mcp
* Spent an inordinate amount of time setting this up, troubleshooting, and enhancing it. But it is now working smoothly.
Daily coach prompt

## Try it for yourself!

Interested in having your own daily productivity conversations with an LLM coach? Here's how you can try it out:
(TODO)

### Continuation

When a conversation hits the maximum length:
1. Claude Settings > Privacy > Export data
2. Await email from Anthropic with link to download data
3. Unzip download, open command line in folder
4. Ensure [ai-chat-md-export](https://github.com/sugurutakahashi-1234/ai-chat-md-export) tool is installed (`npm install -g ai-chat-md-export`)
5. `ai-chat-md-export -i .\conversations.json -p claude`
6. Find and rename the most recent conversation's markdown file to conversation.md
7. If the most recent day was started but not completed, consider trimming it out so you'll' start fresh in the new conversation
8. Open a chat with [continuation.md](continuation.md), attaching prompt.md and conversation.md
9. Download the resulting artifiact (e.g. to replace `C:\s\TaskCoach\prompt.md`)

Or, before hitting the maximum length:
1. Paste [continuation.md](continuation.md) into the chat
2. Remove the second bullet point (conversation.txt)
3. Attach prompt.md
4. Send the message
5. Download the resulting artifiact (e.g. to `C:\s\TaskCoach`)

Review the result by diffing it with the previous version. Apply manual edits that come to mind based on your experience using the task coach.

Paste the result into a new Claude conversation using Ctrl+Shift+V. (Regular Ctrl+V would create an attachment instead of putting the instructions directly into the conversation.)

## Future work

This is working pretty well for me, so I'm not necessarily planning to enhance this further. If I did, here are the things I would consider working on:
1. Easy setup for other users to try it out.
  * Easy creation and configuration of Google task service credentials
  * Template for customizing the prompt to the needs of different people.
  * Perhaps the MCP server initiates an LLM-guided "getting to know you" session to build the initial prompt.
2. Automatic continuation into new conversations. Perhaps store the prompt in a special task or as data maintained in the MCP server.
3. More insightful conversations. I have tried to prompt the LLM to initiate thought-provoking discussions without a great deal of success. Perhaps this isn't possible, but it would be nice to try and make it work.
4. User interface for selecting target tasks for the day (user or LLM can add tasks to a list of targets for the day)
5. Experiment with other LLMs (Claude, Gemini)

If I were to continue working on this it would be due to feedback from other users saying they intend to use it and would appreciate the above enhancements. Or active users suggesting other enhancements they would like to see. If that's you, please drop me a note! (TODO how to contact, profile email, or issues including positive feedback)