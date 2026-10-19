<!--
author:   PM
email:    pm@tbc.com
version:  1.1.0
language: en
narrator: UK English Female
voice:    UK English Male //not working
male:     UK English Male
female:   UK English Female
USmale:   US English Male
USfemale: US English Female
comment:  A PlayBook of interactive activity types for trainers of English to adult job-seekers in Belgium (VDAB, Actiris, Forem, Le Forem, CVO, etc.).
icon: https://www.bruxellesformation.brussels/wp-content/uploads/2023/09/BXF_20135_ICONES-COMM_01.png
edit:     true

import:   https://raw.githubusercontent.com/MINT-the-GAP/lia-kachel/main/README.md
import:   https://raw.githubusercontent.com/MINT-the-GAP/lia-orthography/main/README.md
import:   https://raw.githubusercontent.com/LiaTemplates/Speech-Recognition-Quiz/refs/tags/0.0.1/README.md

@style
// See more on CSS https://gemini.google.com/app/820a61fee9ad5af6
  .lia-quiz__feedback
  {
    display: none !important;
  }
  .lia-effect--inline {
    border: 0;
  }
  lia-btn__icon {
    margin-left:  .2em;
    margin-right: .2em;
  }  
  x.lia-header__middle + img {
    display: none !important;
  }
  x.lia_header__middle
  {
    background: url("https://upload.wikimedia.org/wikipedia/commons/6/65/Flag_of_Belgium.svg") no-repeat; 
  }
@end

@sayx: <script modify="false">"HTML: <button style=\"cursor:pointer;padding:0.2rem 0.7rem;border-radius:6px;background:#fff;color:#222;border:1px solid #888\" onclick=\"var u=new SpeechSynthesisUtterance(`@0`);u.lang='en-GB';u.rate=1;speechSynthesis.cancel();speechSynthesis.speak(u);\">🔊 Listen</button>"</script>
@sayUS: <script modify="false">"HTML: <button style=\"cursor:pointer;padding:0.2rem 0.7rem;border-radius:6px;background:#fff;color:#222;border:1px solid #888\" onclick=\"var u=new SpeechSynthesisUtterance(`@0`);u.lang='en-US';u.rate=1;speechSynthesis.cancel();speechSynthesis.speak(u);\">🔊 Listen (US)</button>"</script>
@sayslow: <script modify="false">"HTML: <button style=\"cursor:pointer;padding:0.2rem 0.7rem;border-radius:6px;background:#fff;color:#222;border:1px solid #888\" onclick=\"var u=new SpeechSynthesisUtterance(`@0`);u.lang='en-GB';u.rate=0.6;speechSynthesis.cancel();speechSynthesis.speak(u);\">🐢 Slow</button>"</script>
@A: <script modify="false">"HTML: <button style=\"cursor:pointer;padding:0.2rem 0.7rem;border-radius:6px;background:#fff;color:#222;border:1px solid #888\" onclick=\"var u=new SpeechSynthesisUtterance(`@0`);u.lang='en-GB';u.rate=1;speechSynthesis.cancel();speechSynthesis.speak(u);\">🔊 A</button>"</script>
@B: <script modify="false">"HTML: <button style=\"cursor:pointer;padding:0.2rem 0.7rem;border-radius:6px;background:#fff;color:#222;border:1px solid #888\" onclick=\"var u=new SpeechSynthesisUtterance(`@0`);u.lang='en-US';u.rate=1;speechSynthesis.cancel();speechSynthesis.speak(u);\">🔊 B</button>"</script>

@say
<button onclick="responsiveVoice.speak(`@0`,`@1`)" style="padding:6px 12px;cursor:pointer">🔊</button>
@end

-->

# 🎭 English Language: The PlayBook

> **A showcase of activity types built with [LiaScript](https://liascript.github.io)** for trainers of adult learners.

Every example uses a **job-search theme** (CVs, interviews, Actiris appointments, workplace English), so you can copy, paste and re-skin it for your own groups.

**Todo**

- [ ] Add native drag-and-drop examples
- [ ] How to disable modes e.g. presentation mode
- [ ] Use comment box more: add > 
- [ ] Use native bullet points (in fact they reveal in presentation mode)
- [ ] Explore other modes - perhaps for revealing questions
- [ ] Add a Conti EPI dictation sequence
- [ ] Embed H5P, and more in iFrame
- [ ] See how LiaScript might work with MS Teams (can we embed?)
- [ ] Add @Orthography e.g. first letter only scaffold
- [ ] Fix speech template: 1) better support messages 2) type as hear 3)...


**Embededd Audio Clip**

Made with Clip Recorder

<audio controls src="data:audio/wav;base64,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"></audio>
## How to use this PlayBook

1. **Navigate** with the sidebar (☰) or the arrow keys.
2. **Click ✎ / "edit"** (top right, if enabled) to see the Markdown source of any slide.
3. **Copy** the pattern you like, change the content, done.

### Contents

| Part | What's inside |
|------|---------------|
| 1 | Classic activities: gap-fill, matching, ordering, MCQ, true/false, odd one out… |
| 2 | TTS (text-to-speech) activities: audio ↔ text, audio ↔ audio, audio gap-fills, dictation |
| 3 | Conti-style EPI (Extensive Processing Instruction) activities |
| 4 | Breaking-News-English-style interactive tasks |
| 5 | Trainer's cheat sheet: quiz syntax at a glance |

### ⚙️ Quick tech notes

* 🔊 buttons use the **browser's / ResponsiveVoice speech engine**. If a button is silent, click once anywhere on the page (browsers block audio before interaction) and check your volume.
* All TTS buttons are defined **once, in the header macros** (`@say`, `@sayUS`, `@sayslow`, `@A`, `@B`). To change the voice or speed for the whole course, edit the header only.
* Inside macros avoid commas and brackets in the spoken text, e.g. `@say(I am looking for a job)`.
* The narrator voice (`narrator:` in the header) can also read slides aloud. Use the 🔊 icon in the LiaScript toolbar.

---

# Part 1: Classic Activities

> To read a text using ResponsiveVoice, the best voices in LiaScript, use the macro `@say(UK English Female,\`Tell me...\`)` Enclose the text in backticks to avoid the text being cut a the first comma!

@say(`Tell me about yourself, I've heard so much!`,@female)
<br>

@say(hi,@male)
<br>

## 1.1 Gap-fill (typing)

**Complete the job-interview sentences. Type one word.**

1. I'm applying **[[for]]** the position of receptionist.
2. I have been working as a cleaner **[[since]]** 2019.
3. Could you tell me more **[[about]]** the working hours?
4. I am good **[[at]]** solving problems.
5. I look forward to **[[hearing]]** from you.

[[?]] Hint: think about the preposition that follows the verb or adjective.

---

## 1.2 Gap-fill (dropdown menu)

**Choose the correct word.**

Dear Mr Janssens,

I am writing **[[ (to) | for | at ]]** apply for the job advertised **[[ on | (in) | at ]]** *Le Soir*. I have **[[ (three) | third | thirty ]]** years' experience **[[ (in) | on | at ]]** customer service. Please find my CV **[[ attached | (attached) | attaching ]]**.

Yours **[[ (sincerely) | faithfully | truly ]]**,

Maria Lopez

> 💡 *Dropdown quizzes are perfect for grammar traps where learners need to see all options.*

---

## 1.3 Gap-fill with a word bank

**Use each word once. There are two extra words.**

<div style="padding:10px;border:2px dashed #888;border-radius:8px;text-align:center;font-size:1.2em">

experience  salary  deadline  reference  skills  vacancy  colleague</div>

<br>
1. There is a **[[vacancy]]** for a warehouse operator at our company.
2. The **[[deadline]]** for applications is Friday 5 pm.
3. What **[[salary]]** are you expecting?
4. My previous manager can give me a **[[reference]]**.
5. Do you have any **[[experience]]** in retail?

---

## 1.4 Matching (word ↔ definition)

**Match each word to its meaning.**

1. **Applicant** → [[ (a person who applies for a job) | a person who pays you | a person who works with you | a person who trains you ]]
2. **Employer** → [[ a person who applies for a job | (a person or company that gives people work) | a person who works with you | a person who leaves a job ]]
3. **Colleague** → [[ a person who applies for a job | a person who pays you | (a person who works with you) | a person who trains you ]]
4. **Resign** → [[ to be fired | to start a job | (to leave a job by choice) | to get a promotion ]]
5. **Shift** → [[ a holiday | (a period of time when you work) | a tax | a contract ]]

---

## 1.5 Matching (halves of collocations)

**Match the verbs and the nouns.**

| | |
|---|---|
| 1. **attend** | [[ (an interview) | a CV | a salary | a deadline ]] |
| 2. **submit** | [[ an interview | (an application) | a meeting | a break ]] |
| 3. **meet** | [[ an interview | a CV | a salary | (a deadline) ]] |
| 4. **negotiate** | [[ an interview | a CV | (a salary) | a shift ]] |
| 5. **update** | [[ an interview | (your CV) | a salary | a deadline ]] |

---

## 1.6 Put the words in order (typing the sentence)

**Unjumble the sentence. Write it in full with a capital letter ignored, no full stop.**

1. *a / have / interview / I / tomorrow / job* →
   [[i have a job interview tomorrow]]

2. *you / send / could / me / the / form / please* →
   [[could you please send me the form]]

3. *been / how / have / working / long / you / here* →
   [[how long have you been working here]]

---

## 1.7 Put the words in order (slot by slot)

**Choose the right word for each position.**

*Words: **do / you / what / for / living / a***

[[ (what) | do | you | for | living | a ]]
[[ what | (do) | you | for | living | a ]]
[[ what | do | (you) | for | living | a ]]
[[ what | do | you | for | living | (a) ]]
[[ what | do | you | for | (living) | a ]]

*(Hint: the answer has 5 positions: the sixth word, "for", belongs to another sentence. Can you find it? 😉)*

---

## 1.8 Put the dialogue in order

**Number the lines from 1 to 5.**

* [[ 1 | 2 | 3 | (4) | 5 ]] "Great. Can you start next Monday?"
* [[ 1 | (2) | 3 | 4 | 5 ]] "Good morning. I'm here for the interview."
* [[ (1) | 2 | 3 | 4 | 5 ]] "Hello, welcome to Delhaize. Please take a seat."
* [[ 1 | 2 | (3) | 4 | 5 ]] "Thank you. I have two years' experience in a supermarket."
* [[ 1 | 2 | 3 | 4 | (5) ]] "Yes, of course. Thank you very much!"

---

## 1.9 Multiple-choice question (single answer)

**What does "I'm available from Monday" mean?**

[( )] I am ill on Monday.
[(X)] I can start on Monday.
[( )] I am busy on Monday.
[( )] I finish work on Monday.
***
**Explanation:** *Available* means "free to do something". In job-search English it often means "able to start working".
***

---

## 1.10 Multiple choice (multiple answers)

**Which of these are good questions to ask at the end of an interview? Select all.**

[[X]] What are the next steps in the process?
[[ ]] How much money do you earn?
[[X]] What does a typical day look like in this role?
[[ ]] Can I leave early on Fridays?
[[X]] Is there any training for new employees?

---

## 1.11 True or false

**Read the job ad and decide.**

> **WANTED: Part-time cleaner**
> Mon–Fri, 6 am – 10 am. Must have own transport. Experience preferred but not essential. Salary: €13 per hour. Apply by email.

1. The job is full-time.

   [(X)] False
   [( )] True

2. You need to have a car, a bike or another way to get to work.

   [( )] False
   [(X)] True

3. You must have previous experience.

   [(X)] False
   [( )] True

4. You can apply by email.

   [( )] False
   [(X)] True

---

## 1.12 Odd one out TBC

**Which word is different?**

1. xxx

[( )] manager  
[( )] supervisor  
[(X)] contract  
[( )] director

2. xxx

[( )] interview  
[( )] application  
[(X)] hammer  
[( )] CV

3. xxx

[(X)] cheerful  
[( )] tired  
[( )] stressed  
[( )] bored
***
*Cheerful* is a positive feeling; the others are negative.
***

4. xxx

[( )] nurse  
[( )] plumber  
[(X)] salary  
[( )] electrician

---

## 1.13 Categorising

**Is it a job, a skill or a document?**

1. electrician → [[ (job) | skill | document ]]
2. teamwork → [[ job | (skill) | document ]]
3. contract → [[ job | skill | (document) ]]
4. driving licence → [[ job | skill | (document) ]]
5. accountant → [[ (job) | skill | document ]]
6. problem-solving → [[ job | (skill) | document ]]

---

## 1.14 Error correction

**One word in each sentence is wrong. Type the correct word.**

1. I have **work** here since 2020. → [[worked]]
2. She is very good **in** languages. → [[at]]
3. He **don't** like working at night. → [[doesn't]]
4. I am **agree** with you. → [[agree]]

## 1.15 Scaffolding

**Orthgraphy plugin**

Set CSS to fixed width using:
.orthography-wrap + .lia-paragraph
dots make work better than underscores (which are treated as Markdown sometimes)

@orthography(`<!-- data-solution-button="4" doublespacehelp="on" -->`,`I a_ r___`,`I am rich`)
[[?]] I a. r...
***
This is feedback
***

**Native TBC** 

Reformat CSS so underscrores are included or and no border. To remove "?" set placeholder="". Set field width to exact size of correct response.

<pre>I a[[m]] r[[ich]]</pre>

---

# Part 2: TTS-based Activities 🔊

> ℹ️ Learners **listen** first, then answer. The spoken text is hidden from the page, which makes these true listening tasks.

## 2.1 Match audio to text

**Click each 🔊 and choose the written sentence you hear.**

**Audio 1:** @say(Could you repeat that please,@male)
[[ (Could you repeat that please?) | Could you complete that please? | Could you repeat the plate please? ]]

**Audio 2:** @say(I have been working here since March,@male)
[[ I have worked here since March. | (I have been working here since March.) | I had been working here since March. ]]

**Audio 3:** @say(When can you start,@male)
[[ What can you start? | (When can you start?) | Where can you start? ]]

**Audio 4:** @say(I would like to apply for the position,@male)
[[ to play | to reply | (to apply) ]]

---

## 2.2 Match audio to text (minimal pairs)

**Same sound, different word. Which one do you hear?**

**A:** @say(I live in Ghent,@female)
[[ (live) | leave ]] 

**B:** @say(She is going to work on a ship,@voice)
[[ sheep | (ship) ]]

**C:** @say(Please fill in the form,@voice)
[[ (fill) | feel ]]

**D:** @say(Can I have the full details,@voice)
[[ fool | (full) ]]

---

## 2.3 Match audio to audio

**The 🔊 on the left is a question. Match it to the best answer on the right.**

| Questions | Answers |
|-----------|---------|
| **Q1** @say(Where do you work) | **A** @say(I work at a hospital) |
| **Q2** @say(How long have you been there) | **B** @say(For about five years) |
| **Q3** @say(Why do you want this job) | **C** @say(Because I enjoy working with people) |
| **Q4** @say(Can you start on Monday) | **D** @say(Yes I can) |

Which answer matches each question?

* Q1 → [[ (A) | B | C | D ]]
* Q2 → [[ A | (B) | C | D ]]
* Q3 → [[ A | B | (C) | D ]]
* Q4 → [[ A | B | C | (D) ]]

---

## 2.4 Gap-fill using audio (word bank with distractors)

**Listen to the whole sentence, then complete the gaps with words from the bank.**

<div style="padding:8px;border:2px dashed #888;border-radius:8px;text-align:center;font-size:1.1em">
**interview early arrive arrived dress address smartly</div>
<br>

**Sentence 1** @say(You should arrive early for an interview,@female)

You should [[ (arrive) | arrived | address ]] [[ (early) | smartly | dress ]] for an [[ (interview) | dress | arrive ]].

**Sentence 2** @say(It is important to dress smartly,@female)

It is important to [[ arrive | (dress) | address ]] [[ early | (smartly) | interview ]].

**Sentence 3** @say(Please write your address here,@female)

Please write your [[ dress | arrived | (address) ]] here.

---

## 2.5 Gap-fill with dropdowns: two different audios

**Two short audios, A and B, are almost the same. Listen to each one and choose the correct word for each.**

**Audio A:** @say(They're applying for the same job,@male)

**Audio B:** @say(Their application is ready,@female)

1. Which audio is "They're"? → [[ (A) | B ]]
2. Which audio is "Their"? → [[ A | (B) ]]

Now complete the sentences:

* Audio A: [[ (They're) | Their | There ]] applying for the same job.
* Audio B: [[ They're | (Their) | There ]] application is ready.

---

## 2.6 Another two-audio gap-fill (past vs present)

**Listen carefully to both. Which tense is used?**

**Audio A:** @say(I work in a factory,@female)

**Audio B:** @say(I worked in a factory,@male)

* Audio A is [[ (present simple) | past simple ]]
* Audio B is [[ present simple | (past simple) ]]

Complete the CV line that matches **Audio B**:

*"From 2018 to 2021 I [[ work | (worked) | working ]] in a factory."*

---

## 2.7 Dictation (type what you hear)

**Listen as often as you like. Type the sentence (no punctuation, lower case).**

1. @say(Thank you for inviting me to the interview,@female)
   [[thank you for inviting me to the interview]]

2. @say(I am available to start immediately,@male)
   [[i am available to start immediately]]

3. @say(Could you give me your phone number,@USfemale)
   [[could you give me your phone number]]

---

## 2.8 Listening comprehension: short phone call TBC

**Listen to the voicemail and answer.**

@say(Hello this is Anna Smith. I am calling about your appointment on Thursday. It has been moved from ten o'clock to eleven thirty. Please call me back on zero four seven five five five one two three four,@male)

1. Who is calling? 
[( )] An employee 
[(X)] An employer  
[( )] An employment

2. Which day is the appointment? 
[( )] Tuesday  
[(X)] Thursday  
[( )] Friday

3. What is the new time? 
[( )] 10:00  
[( )] 11:00  
[(X)] 11:30

4. What should the listener do? 
[(X)] Call back  
[( )] Send an email  
[( )] Do nothing

---

# Part 3: Conti-style EPI Activities

> Based on **Gianfranco Conti's Extensive Processing Instruction (EPI)**: *a sentence builder → lots of receptive processing (listening/reading) → structured production.* The same chunks are recycled again and again.

## 3.0 The sentence builder - TBC redo SB

> TBC Perhaps use multiple small tables where every combination can be valid. Consider macro that reads or displays valid combinations for various activities e.g. speak or display a valid combination with a missing word etc.

Study this **sentence builder** first. Every activity in Part 3 recycles these chunks.

| **Who** | **Verb phrase** | **Time** | **Place** |
|---------|-----------------|----------|-----------|
| I | work | every day | in a shop |
| I | worked | last year | in a factory |
| I | am looking for a job | at the moment | in Brussels |
| I | would like to work | next year | in a hospital |
| She | works | every weekend | in a restaurant |
| He | worked | two years ago | in an office |
|  |  | currently | in catering |
|  |  | now | in I.T. |
|  |  | during the summer | in retail |


@say(I worked last year in a factory,@male)

---

## 3.1 Listening: tick what you hear TBC

**Listen to each sentence and choose the chunk you hear.**

**1.** @say(I work every day in a shop,@male)
Time: [[ (every day) | last year | next year ]] Place: [[ (in a shop) | in a factory | in an office ]]

**2.** @say(He worked two years ago in an office,@female)
Who: [[ I | She | (He) ]] Verb: [[ work | works | (worked) ]]

**3.** @say(I would like to work next year in a hospital,@USmale)
Verb: [[ am looking for a job | (would like to work) | worked ]] Place: [[ in Brussels | (in a hospital) | in a restaurant ]]

---

## 3.2 Spot the missing word

**Listen. One word is missing in the written version. Which one?**

@say(I worked last year in a factory,@female)

Written: *"I worked year in a factory."* Missing word: [[last]]

@say(She works every weekend in a restaurant,@male)

Written: *"She works weekend in a restaurant."* Missing word: [[every]]

@say(I am looking for a job in Brussels,@USfemale)

Written: *"I am looking a job in Brussels."* Missing word: [[for]]

---

## 3.3 Faulty echo - TBC redo

**Listen to the sentence, then read the "echo". Is the echo correct or faulty? If faulty, type the wrong word.**

**1.** @say(I work every day in a shop,@female)
Echo: *"I work every week in a shop."*

[( )] Correct  
[(X)] Faulty → wrong word: [[day]]

**2.** @say(He worked two years ago in an office,@male)
Echo: *"He worked two years ago in an office."*

[(X)] Correct  
[( )] Faulty

**3.** @say(She works every weekend in a restaurant,@USfemale)
Echo: *"She works every weekend in a hospital."*

[( )] Correct  
[(X)] Faulty → wrong word: [[restaurant]]

---

## 3.4 Delayed dictation

**Listen once. Wait 5 seconds. Then write the sentence from memory.**

@say(I would like to work next year in a hospital,@female)<br>

[[I would like to work next year in a hospital]]

*(Variation: ask learners to do this in pairs: A listens, B writes, then swap.)*

---

## 3.5 Backchaining (listen & repeat) - TBC fix sayslow macro

**Say each chunk aloud after the audio, starting from the end.**

1. @sayslow(in a factory)
2. @sayslow(last year in a factory)
3. @sayslow(worked last year in a factory)
4. @say(I worked last year in a factory,@female)

> 🎤 This is a pronunciation scaffold: the learner builds up fluency without losing the intonation of the full sentence.

---

## 3.6 Sentence puzzle (choose the right chunk) TBC

**Build correct sentences from the builder.**

1. [[ (I) | She | He ]] [[ (work) | works | worked ]] every day in a shop.
2. [[ I | (She) | They ]] [[ work | (works) | worked ]] every weekend in a restaurant.
3. [[ I | She | (He) ]] [[ work | works | (worked) ]] two years ago in an office.
4. I [[ work | worked | (would like to work) ]] next year in a hospital.

---

## 3.7 Odd one out (reading)

**Which chunk does not fit?**

1. *every day / last year / two years ago* → [[ (every day) | last year | two years ago ]] *(present habit vs past times)*
2. *in a shop / in an office / yesterday* → [[ in a shop | in an office | (yesterday) ]]
3. *works / worked / working* → [[ works | worked | (working) ]] *(not a finite form in the builder)*

---

## 3.8 Narrow listening: three speakers

**Three candidates introduce themselves. Everyone says similar things. Listen to all three.**

**Speaker 1 (Ali):** @say(I worked last year in a factory and I am looking for a job in Brussels,@male)

**Speaker 2 (Sofia):** @say(I work every day in a shop and I would like to work in a hospital next year,@female)

**Speaker 3 (Piet):** @say(He worked two years ago in an office but now he is looking for a job,@USmale)


**Who…?**

* …is currently in a shop job? [[ Ali | (Sofia) | Piet ]]
* …wants to work in a hospital? [[ Ali | (Sofia) | Piet ]]
* …worked in a factory? [[ (Ali) | Sofia | Piet ]]
* …is described in the third person (not speaking about themselves)? [[ Ali | Sofia | (Piet) ]]

---

## 3.9 Mind-reading / pair task (non-digital)

**Instructions for trainers (print or screenshare):**

1. Learner A silently picks one sentence from the builder.
2. Learner B guesses: *"Do you work every day in a shop?"*
3. A answers *"Yes, I do"* or *"No, I don't."*
4. First to guess in 5 questions wins!

> Use the sentence builder (3.0) as a visual support.

---

# Part 4: Breaking-News-English-style Tasks TBC

> Inspired by the interactive, text-based activities popular at breakingnewsenglish.com. They work well as warm-ups and homework.

## 4.1 Add the spaces

**The spaces are missing. Type the sentence with spaces.**

*"Thejobinterviewstartsatnineo'clocktomorrowmorning."*

[[the job interview starts at nine o'clock tomorrow morning]]

*"Pleasebringyourpassportandyourdrivinglicence."*

[[please bring your passport and your driving licence]]

*"Weareofferingafulltimecontractwithtrainingincluded."*

[[we are offering a full time contract with training included]]

---

## 4.2 Add the spaces: headline edition

**Fix the headline.**

*"UNEMPLOYMENTFALLSASNEWJOBSAREADVERTISED"*

[[unemployment falls as new jobs are advertised]]

---

## 4.3 Unscramble the letters

**Rearrange the letters to make a job-related word.**

1. **ntiverewi** → [[interview]]
2. **ylasar** → [[salary]]
3. **cllgeouea** → [[colleague]]
4. **tcnrtaco** → [[contract]]
5. **ptnaicpal** → [[applicant]]

---

## 4.4 Spelling: which one is correct?

{{1}}
[( )] recieve  
[(X)] receive  
[( )] recive

{{2}} 
[(X)] experience  
[( )] experiance  
[( )] expirience

{{3}}
[( )] colleage  
[( )] collegue  
[(X)] colleague

{{4}}
[( )] vacancy  
[(X)] vacancy  
[( )] vaccancy

> *Tip: change item 4's options to avoid duplicate correct answers when you reuse it.*

---

## 4.5 Synonym match

**Match the word on the left with a word of similar meaning.**

1. **Salary** → [[ (pay) | tax | holiday ]]
2. **Boss** → [[ colleague | (manager) | customer ]]
3. **Job** → [[ (work) | rest | school ]]
4. **Fire (somebody)** → [[ hire | (dismiss) | promote ]]
5. **Tired** → [[ (exhausted) | energetic | cheerful ]]

---

## 4.6 Fast reading: true/false before you read

**Guess first, then read the text to check.**

1. Most people in Belgium work 38 hours a week. [(X)] True  [( )] False
2. Belgium has three official languages. [(X)] True  [( )] False
3. You must always use "Dear Sir or Madam" in a cover letter. [( )] True  [(X)] False

> *Belgium has three official languages: Dutch, French and German. The standard full-time week is 38 hours.*

---

## 4.7 Number the lines (story sequencing)

**Put the story in order.**

* [[ 1 | 2 | (3) | 4 ]] She went to the interview and answered all the questions.
* [[ (1) | 2 | 3 | 4 ]] Fatima saw a job advert on the VDAB website.
* [[ 1 | (2) | 3 | 4 ]] She sent her CV and a cover letter.
* [[ 1 | 2 | 3 | (4) ]] A week later she got the job!

---

## 4.8 Cloze race: first letters given

**Complete each word. The first letter is given.**

1. I am looking f[[or]] a j[[ob]] in logistics.
2. Can you t[[ell]] me about your experience?
3. We offer a competitive s[[alary]].
4. Please s[[end]] your CV by email.

---

---
 
# Part 5: Drag-and-Drop Tiles (MINT the GAP)
 
> This part uses the **[lia-kachel](https://github.com/MINT-the-GAP/lia-kachel)** template by Martin Lommatzsch and Jihad Hyadi (MINT the GAP). *Kachel* is German for "tile". It adds mouse, touch and pen **drag-and-drop** to LiaScript's native tile quizzes (`[->[...]]`), so it works on phones and tablets too.
>
> It is loaded with a single `import:` line in the header of this file. For stable courses you can pin a version instead of `main`, for example `.../lia-kachel/0.7.0/README.md`.
 
## 5.1 Tiles: drag words into gaps TBC FAULTY
 
**Drag the correct word into each gap.** Each gap has its own pool of tiles. The correct tile is marked with round brackets; the others are distractors.
 
<!-- data-randomize="true" -->
I am applying [->[(for)|to|at]] the position of warehouse operator. I have been working [->[(in)|on|at]] logistics [->[(since)|for|from]] 2019, and I am good [->[(at)|in|on]] working in a team.
 
> 💡 Syntax: `[->[(right)|wrong|wrong]]`. Add `<!-- data-randomize="true" -->` on the line above to shuffle the tiles.
 
---
 
## 5.2 Tiles: matching TBC FAULTY
 
**Drag each job into the correct description.**
 
<!-- data-randomize="true" -->
Someone who fixes pipes and taps is a [->[(plumber)|nurse|cashier]]. \
Someone who looks after patients is a [->[(nurse)|plumber|cashier]]. \
Someone who works at the till in a supermarket is a [->[(cashier)|nurse|plumber]]. \
Someone who drives a lorry is a [->[(driver)|nurse|plumber]].
 
---
 
## 5.3 Tiles: duplicate labels
 
Gaps can use have more than one correct tile.
 
<!-- data-randomize="true" -->
Complete the polite phrases: \
[->[(Could)|Can|May]] you repeat that, please? \
[->[(Would)|Do|Are]] you like some water? \
Thank you [->[(very)|(so)|many]] much for your time.
 
---
 
## 5.4 Tiles: sequence in any order TBC FAULTY
 
`@Kachelfolge` lets learners place the correct tiles in **any order**. It checks the *set*, not the position. Good for lists with no fixed order.
 
<!-- data-randomize="true" -->
Name four documents you should bring to a job interview:
@Kachelfolge(`[->[(CV)|bicycle]][->[(passport)|umbrella|sandwich]][->[(diploma)|football]][->[(ID card)|holiday photos]]`)
 
<!-- data-randomize="true" -->
Choose three good things to do before an interview:
@Kachelfolge(`[->[(research the company)|arrive late]][->[(prepare answers)|switch on your alarm]][->[(plan your journey)|forget your CV]]`)
 
---
 
## 5.5 Tiles: unknown number of answers
 
`@KachelfolgeN` shows only **one** gap at first. A new gap appears each time you fill the last one, so the learner does not know how many answers are needed. A ✛ field at the end hides the count until the check. 
Note: the [+] tile is the only indication of where the selected tiles end.


<!-- data-randomize="true" -->
**Which of these are good questions to ask the interviewer? Drag them in, in any order.**
@KachelfolgeN(`[->[(What does a typical day look like?)|How much can I earn tomorrow?]][->[Can I leave early on Fridays?|(What training is offered?)|Do you like me?]][->[(What are the next steps?)|Who is your favourite player?]][->[Do I have to work?|(What are the opportunities for growth?)]]`)
 
> ⚠️ Put each `@Kachelfolge` / `@KachelfolgeN` call on **its own line**, and include wrong tiles plus `data-randomize` so the number of answers can't be guessed.
 
---
 
## 5.6 Tiles: grouped sort in a table
 
`@KachelgruppeN` puts a progressive tile sequence in each table cell, and one `@KachelgruppenCheck` underneath checks the whole table. Tiles can only go into their own group. Each group has its own progressive gaps.
 
| Category | Drag the words here |
| :------: | :-----------------: |
| Jobs | @KachelgruppeN(jobsort,`[->[(electrician)]][->[(accountant)]][->[(nurse)]][->[(plumber)]]`) |
| Skills | @KachelgruppeN(jobsort,`[->[(teamwork)]][->[(problem-solving)]][->[(communication)]]`) |
| Documents | @KachelgruppeN(jobsort,`[->[(CV)]][->[(contract)]][->[(cover letter)]][->[(reference)]]`) |
@KachelgruppenCheck(jobsort)
 
> ⚠️ Rules: no blank line between the table and `@KachelgruppenCheck`; the key (`jobsort`) is identical in all cells and in the check; it starts with a letter and is unique on the slide; and the cells cover all drop targets in the table.
 
---
 
## 5.7 Tiles: content-based checking
TBC FAULTY: duplicate tiles 
 
Wrap the quiz in `<div class="Kachel">` and each gap is checked by the **text on the tile**, so identical tiles are interchangeable.
 
<div class="Kachel">
Choose **a** or **an**.
 
<!-- data-solution-button="3" data-randomize="true" -->
She is [->[(an)|a]] electrician. \
He has [->[(a)|an]] job interview tomorrow. \
I have [->[(an)|a]] application form and [->[(a)|an]] CV. \
It is [->[(an)|a]] honest answer.
 
</div>
> 💡 Capital letters and punctuation count, so `an` and `An` are different tiles.
 
---
 
## 5.8 Tiles: a single gap in running text
 
A quiz with only one tile target should sit inside a sentence, not on its own line.
 
<!-- data-randomize="true" -->
The person who works for a company is called an [->[(employee)|employer|applicant]].
 
---
 
# Part 6: Spelling & Dictation (lia-orthography) TBC
 
> This part uses the **[lia-orthography](https://github.com/MINT-the-GAP/lia-orthography)** community template by MINT the GAP (see the [LiaScript blog post](https://liascript.github.io/blog/lia-orthography-spelling-exercises-in-liascript/)). It adds three macros: **`@orthography`** (inline correction), **`@orthographytext`** (full-text correction with red/green diff feedback) and **`@diktat`** (a dictation gap read aloud by the narrator).
>
> It is loaded with a second `import:` line in this file's header. Note that the template is at an early version (0.0.1), so test your activities before class.
 
## 6.1 Inline correction
 
**Each sentence has a spelling mistake. Type the corrected sentence.**

@orthography(`<!-- data-solution-button="4" -->`,`Es ist jetze um sechse.`,`Es ist jetzt um sechs.`)
[[?]] This is a hint
 
> 💡 Argument 1 is a LiaScript quiz options comment (here: a solution button after 2 attempts). Argument 2 is the faulty text. Argument 3 is the reference answer used for grading.
 
---
 
## 6.2 Correct the paragraph
 
**Rewrite the paragraph without errors. After checking, the differences are highlighted in red and green.**
 
@orthographytext(
  `<!-- data-solution-button="2" -->`,
  `Dear Mr Peeters, I am writting to apply for the postion of recepcionist. I have two years of experiance and I am very reliabel. I look forward to hearing from you.`,
  `Dear Mr Peeters, I am writing to apply for the position of receptionist. I have two years of experience and I am very reliable. I look forward to hearing from you.`
)
 
---
 
## 6.3 Typical grammar and spelling slips in emails
 
**Correct the paragraph.**
 
@orthographytext(
  ` `,
  `Their is a meeting tomorow at nine. Please bring you're CV and a copy of you're diploma. Its important to arrive on time.`,
  `There is a meeting tomorrow at nine. Please bring your CV and a copy of your diploma. It's important to arrive on time.`
)
 
---
 
## 6.4 Dictation gaps - WORKS
 
**Click to hear each missing word, then type its spelling.** The narrator reads only the gap word, not the whole sentence.
 
Please send your @diktat(application) to the @diktat(manager) by @diktat(Wednesday).
 
The @diktat(interview) is at a @diktat(quarter) past @diktat(ten) in the @diktat(reception) area.
 
I am looking for a @diktat(permanent) @diktat(contract) with good @diktat(opportunities).
 
> 🔊 The `@diktat` voice comes from the `narrator:` line in the header (here UK English Female).
 
---
 
## 6.5 Dictation: tricky workplace words
 
**Listen and spell.**
 
My @diktat(colleague) works in the @diktat(department) of @diktat(accounting).
 
The company offers @diktat(training) and a good @diktat(salary).
 
Please check your @diktat(schedule) and your @diktat(address) carefully.
 
---
 
## 6.6 Mixed practice: differentiate by level
 
Use short inline items for lower levels and the full-text version for higher levels:
 
**A2:**
 
@orthography(
  ` `,
  `She work in a shop.`,
  `She works in a shop.`
)
 
**B1:**
 
@orthography(
  ` `,
  `I have been work here since two thousand nineteen.`,
  `I have been working here since two thousand nineteen.`
)
 
**B2:**
 
@orthographytext(
  ` `,
  `Having completed my studies in 2020 I have gained substancial experiance in costumer service. I am confident that I would be a valuble asset to you're team.`,
  `Having completed my studies in 2020, I have gained substantial experience in customer service. I am confident that I would be a valuable asset to your team.`
)
 
---
 
# Part 7: Voice recognition

@SpeechRecognition.support

Say "Hello world":  

[[!]]
@SpeechRecognition(en-UK, Hello world)


https://liascript.github.io/blog/speech-recognition-quiz-in-liascript/


# Trainer's Cheat Sheet
 
## Quiz syntax at a glance TBC
 
| Activity | Syntax | Example |
|----------|--------|---------|
| Typing gap-fill | `[[answer]]` | `I live in [[Brussels]].` |
| Dropdown | `[[ (right) | wrong | wrong ]]` | `[[ (on) | in | at ]]` |
| Single choice | `[(X)]` / `[( )]` | `[(X)] Yes  [( )] No` |
| Multiple choice | `[[X]]` / `[[ ]]` | `[[X]] A  [[ ]] B` |
| Hint | `[[?]] text` | placed under a quiz |
| Explanation | `***` … `***` | placed under a quiz |
| TTS button | `@say(text)` | `@say(Good morning)` |
| Drag-and-drop tile | `[->[(right)|wrong]]` | `[->[(for)|to|at]]` |
| Tiles, any order | `@Kachelfolge(...)` | on its own line |
| Tiles, unknown count | `@KachelfolgeN(...)` | on its own line |
| Tile table groups | `@KachelgruppeN(key, ...)` + `@KachelgruppenCheck(key)` | in a table |
| Tiles by content | `<div class="Kachel">` … `</div>` | wraps a tile quiz |
| Inline correction | `@orthography(options, wrong, right)` | faulty sentence |
| Text correction | `@orthographytext(options, wrong, right)` | full paragraph with diff |
| Dictation gap | `@diktat(word)` | read word and gap-fill |
 
## Activity ideas to adapt
 
* **Matching** → dropdown per line.
* **Word order** → typed answer, or one dropdown per position.
* **Add spaces** → typed answer; paste your own text without spaces.
* **Audio ↔ audio** → label buttons A/B/C, then dropdowns choose the letter.
* **EPI** → one sentence builder, many short activities recycling the same chunks.
## Tips for trainers
 
1. Keep one theme per module: learners benefit from recycled vocabulary.
2. Use `@sayslow` for lower levels and `@sayUS` to expose learners to different accents.
3. Add `***` explanation blocks so learners get feedback immediately.
4. Use classroom mode: share your screen and let groups vote before revealing answers.
5. Host your `.md` file on GitHub, then open it via `https://liascript.github.io/course/?https://raw.githubusercontent.com/YOU/REPO/main/ESL_PlayBook.md`.
---
 
> 🎉 **Well done!** Now copy a pattern and make it yours.
 