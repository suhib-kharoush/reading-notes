# The Best Whiteboard Interview Advice

- Whiteboard-style interviews are ubiquitous in the tech industry.
- For those who not had the pleasure, whiteboard interviewing is the practice of asking candidates to solve technical questions on a whiteboard, piece of paper, or computer during the interview. This kind of environment can feel like a pressure cooker and cause even the most competent engineer to fall apart.

#### The Advice: Communicate!
![](https://hackernoon.com/_next/image?url=https%3A%2F%2Fcdn.hackernoon.com%2Fphotos%2F3nhao37bBEfHA9RTQ0WNVWfXPD02-7z632c4&w=1920&q=75)

#### First, Restate the Question
- Do you understand what they’re asking you to do? Prove it. Restate the question for them and seek affirmation.

#### Ask About Edge Cases
- It’s still not time to dive right into coding the solution. Think for a bit about the inputs and expected output and think about potential edge cases to the problem. Ask about them.

#### Ask About Test Cases
- This is free and you should take advantage of it. Simply ask if there are any test cases that the function should pass. 

#### Write Pseudocode and Ask If It Makes Sense
- You’ll find yourself constrained by trying to remember the methods or other idiosyncrasies of the language rather than trying to come up with the correct logic. Instead, let your interviewer know you’re going to start by writing pseudocode and fill in the actual code later.

#### Write the Actual Code and Ask if it Looks Good
- At this point, you just need to plug the appropriate code for your language in. If you forget some syntax or a method name, you should be able to ask your interviewer for this information without too much grief. If they give you trouble, just say you’ll leave it as pseudocode for now.

#### Stuck? Ask for Help!
- If you’re having trouble along the way, it’s not illegal to ask for some help. Just phrase it conversationally.


### 7 tips to ace a programming interview:

##### 1. Take a few minutes.
- Speaking as an interview coach, this is one misstep that I see all the time during mock interviews. The canonical tip that everyone gives is, “talk more!”.

##### 2. Write down the steps of the solution.
- Write down the general steps of how you will solve it on one side of the whiteboard, where it’s visible but won’t get in the way. You don’t need to be verbose, just get the steps in order and somewhat readable.

##### 3. Write pseudocode first.
- Often we run into problems halfway through writing the code, and there’s no point wasting time over syntax when you might have to throw the code away. Instead, write some half-baked code-looking stuff that lays out the structure of how your code will work. Do it over on the side of the whiteboard, so you have space left to work.
cur_idx = array.length / 2

```````
cur_idx = array.length / 2
l_marker = 0
r_marker = array.length
while (markers are more than 1 apart)
  if array[cur_idx] === search_val
    return true
  else if array[cur_idx] < search_val
    cur_idx goes halfway towards r_marker
    l_marker = cur_idx
  else if array[cur_idx] > search_val
    cur_idx goes halfway towards l_marker
    r_marker = cur_idx
return false
```````

##### 4. Don’t sweat the small stuff.
- Programming interviews are not about how well you’ve remembered your semicolons, nor are they about being able to remember all of the flags on a TCP packet. They’re about demonstrating depth and breadth of knowledge, personality strengths, and problem-solving abilities. If you make a mistake, it’s okay. Brush it off and move on.

##### 5. Sit down. Be humble.
- A programming interview isn’t just a written exam. It’s an assessment of your programming abilities, and there are plenty of things that fall into that category beyond mere coding prowess.

##### 6. Come prepared.
-  If you want to be ready, you have to put in the time. It’s important in order to maximize your chances of acing the interview, but it’s also important for your peace of mind during the interview and afterwards. In the interview, knowing that you’ve done all you can to prepare helps you stay calm and cool, and increases your chances of success.

##### 7.  Review your work.
- You won’t always finish questions in the time permitted, but occasionally you’ll have extra time after coming up with a solution. If this happens, it’s tempting to say “Well, I’m done!”. Interviews are stressful and we want them to be over as fast as possible. 