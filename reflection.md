# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
The game was as expected, a space to enter guesses and button to  submit, a new game button and a hint button. Side bar to change difficulty
- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").

  + Hints were reversed
  + History of guesses not displaying correctly
---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
  + Claude 
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
  + Reverse the hints for the guesses. I tested this by running the app again after the AI gave me the suggestion.
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
  + Checking the ranges in the difficulty the AI did not consider the fact that the function would have incorrect ranges such as Normal having a higher range than Hard.
---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
  + I decided a bug was really fixed by trying to intentionally break it again. For example, after fixing the reversed hints, I guessed numbers both higher and lower than the secret number to confirm the hint logic worked in both directions. If I couldn’t reproduce the original issue after multiple attempts, I considered it fixed.
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
  + One manual test I ran was switching between difficulty levels and then starting a new game to check if the number range matched the selected difficulty. This showed me that the ranges were inconsistent at first, especially when Normal had a higher range than Hard.

- Did AI help you design or understand any tests? How?

  + AI did help me think about edge cases, especially around validating difficulty ranges and checking how the guessing logic responded. It suggested walking through example inputs step by step, which helped me understand where the logic was failing.
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
+ I would explain Streamlit reruns as the app refreshing from top to bottom whenever you click a button or submit input. Session state is like a memory box that maintains those refreshes. If you don’t store important values in session state, they get reset each time.


---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
  + One habit I want to reuse is manually testing features immediately after making small changes instead of waiting until the end. Testing right after each fix made it easier to isolate what caused each issue.
- What is one thing you would do differently next time you work with AI on a coding task?
 + Next time I work with AI on a coding task, I would give more detailed context about my existing logic instead of just describing the bug.
- In one or two sentences, describe how this project changed the way you think about AI generated code.
 + This project changed how I think about AI-generated code because I realized it’s more like a collaborator than an answer key. It can point me in the right direction, but I still need to understand and verify everything myself.
