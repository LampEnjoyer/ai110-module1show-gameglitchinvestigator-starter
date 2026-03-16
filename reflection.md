# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?

The game looked like a regular guessing game until you actually started playing it.

- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").

  The hints were backwards. If I were to answer 50, and the secret number is 38. It would tell me too high and I needed to go higher. If I entered 50 again it would then reverse it.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
Claude
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
The AI suggested how to fix the swapping of results. The AI pointed out where exactly the guess was being processed. I noticed that the program would parse the guess as a string if the guess number was 2. After fixing it, I played the same game with the same numbers and it was correct.
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
The AI suggested a way to ensure that if you were to switch difficulties, it wouldn't carry over the new one. I did my own test and found that the program already accounted for this.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
I ran a few tests with the same input before and after making changes. If what I saw was expected, the I concluded that the bug is fixed.
- Describe at least one test you ran (manual or using pytest)  
I kept inputting the same number over and over to see if the program would stay consistent.
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?
No, I made my own tests.
---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
- What change did you make that finally gave the game a stable secret number?

The secret number never changed, only the way it was parsing the input. If it was an even guess, it would parse it as a string and compare it as an integer. This would lead to faulty comparisons because we are comparing diferent types. I removed the modulo 2 statement, so that the code would never parse the input as a string.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
One habit I want to reuse in future projects is frequently committing small changes to Git so I can track progress and easily revert mistakes.
- What is one thing you would do differently next time you work with AI on a coding task?

Next time I work with AI on a coding task, I would provide clearer prompts and more specific context about the problem to get more accurate and useful responses.
- In one or two sentences, describe how this project changed the way you think about AI generated code.

I don't think this project changed the way I view about AI generated code. If the code is really simple, AI generated code would be fine. However, if it required extensive knowledge about the program, you would need to list out everything.
