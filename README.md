# 🤖 Sir Talk-A-Lot — AWS Lex Knowledge Quiz Chatbot

> *"Let's see if your Amazon S3 knowledge is giving Cloud Pro energy ☁️"*

![AWS](https://img.shields.io/badge/Built%20With-Amazon%20Lex-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Status](https://img.shields.io/badge/Status-Live%20%26%20Deployed-brightgreen?style=for-the-badge)
![Language](https://img.shields.io/badge/Language-English%20ZA-blue?style=for-the-badge)
![Project](https://img.shields.io/badge/Praesignis-AWS%20re%2FStart-orange?style=for-the-badge)

---

## 👋 Meet Sir Talk-A-Lot

**Sir Talk-A-Lot** is an interactive AI-powered quiz chatbot built on **Amazon Lex** for our fictional client, **CloudLearners Inc.** Designed to make AWS learning fun, engaging, and interactive — Sir Talk-A-Lot quizzes users on their Amazon S3 knowledge through a conversational interface with personality, Gen Z energy, and real AWS knowledge baked in.

This project was built as part of the **Praesignis AWS re/Start Programme — Project 3.**

---

## 🎯 What Problem Does It Solve?

Traditional AWS learning can be dry and overwhelming. CloudLearners Inc. needed a way to make knowledge checks **fun, conversational, and accessible** for their learners. Sir Talk-A-Lot solves this by:

- Turning passive studying into an **active quiz experience**
- Giving **instant feedback** on correct and incorrect answers
- Using **branching logic** to personalise the conversation flow
- Making learners feel encouraged whether they get it right or wrong

---

## ☁️ What Is Amazon Lex?

**Amazon Lex** is an AWS AI service that allows developers to build conversational interfaces — also known as chatbots — using the same deep learning technology that powers Amazon Alexa.

Key capabilities:
- **Natural Language Processing (NLP)** — understands what users type or say
- **Intent recognition** — identifies what the user wants to do
- **Slot filling** — captures specific values from user input
- **Branching logic** — routes conversations based on conditions
- **Multi-platform deployment** — can be embedded in websites, apps, and more

---

## 🏗️ Project Architecture

```
User Input (Text)
       ↓
Amazon Lex Bot — Sir_Talks-a-alot
       ↓
S3Quiz Intent
       ↓
┌─────────────────────────────────┐
│         Conversation Flow        │
│                                  │
│  Initial Response                │
│  (Welcome + Question 1)          │
│         ↓                        │
│  QuizAnswer1 Slot                │
│  (Captures A, B, or C)           │
│         ↓                        │
│  Conditional Branches            │
│  (Correct / Incorrect / Default) │
│         ↓                        │
│  QuizAnswer2 Slot → Q3 → Q4 → Q5│
│         ↓                        │
│  Closing Response                │
│  (Quiz Complete!)                │
└─────────────────────────────────┘
       ↓
FallbackIntent (handles unknown input)
```

---

## 🧠 Key AWS Concepts Used

| Concept | What It Does In Our Bot |
|---------|------------------------|
| **Intent** | `S3Quiz` — the goal of running the quiz |
| **Utterances** | Phrases like `Start quiz` that trigger the bot |
| **Slots** | `QuizAnswer1-5` — captures the user's A/B/C answer |
| **Custom Slot Type** | `QuizAnswerType` — recognises A, B, C as valid inputs |
| **Conditional Branches** | Routes to correct/incorrect response per answer |
| **FallbackIntent** | Handles anything the bot doesn't understand |
| **Closing Response** | Final message after the quiz is complete |
| **ElicitSlot** | Tells the bot which slot to capture next |

---

## 📋 Quiz Structure

Sir Talk-A-Lot runs a **5-question multiple choice quiz** on Amazon S3:

| # | Question | Correct Answer |
|---|----------|---------------|
| Q1 | What does Amazon S3 stand for? | A) Simple Storage Service |
| Q2 | What is Amazon S3 mainly used for? | A) Cloud Storage |
| Q3 | Which of the following is an Amazon S3 use case? | B) Backup and disaster recovery |
| Q4 | Which of the following are features of Amazon S3? | C) Unlimited storage & Versioning |
| Q5 | Which S3 Storage Class works best for infrequent but rapid access? | B) S3 Standard-Infrequent Access |

---

## 💬 Conversation Flow

```
User:           "Start quiz"
Sir Talk-A-Lot: 👋 Welcome message + Question 1
User:           "A / B / C"
Sir Talk-A-Lot: ✅ Correct! or ❌ Incorrect! + Question 2
User:           "A / B / C"
Sir Talk-A-Lot: ✅ Correct! or ❌ Incorrect! + Question 3
                        ...continues through Q4 and Q5...
Sir Talk-A-Lot: 🎉 Quiz Complete! Well done!
```

---

## 🚀 How To Run Sir Talk-A-Lot

### Prerequisites
- An AWS Account
- Access to Amazon Lex (us-east-1 region)
- English (ZA) language configured

### Steps
1. Log into the **AWS Management Console**
2. Navigate to **Amazon Lex**
3. Open the **Sir_Talks-a-alot** bot
4. Click **Draft version → English (ZA) → Intents**
5. Click **Build** to compile the bot
6. Click **Test** to open the chat window
7. Type `Start quiz` to begin! 🎉

---

## 📸 Screenshots

### Bot Overview — Amazon Lex Console
> *Screenshot of the Sir_Talks-a-alot bot on the Lex bots dashboard showing Available status*

```
📷 [ SCREENSHOT: Lex Bots Dashboard — Sir_Talks-a-alot Available ]
```

---

### S3Quiz Intent — Utterances
> *Screenshot showing all sample utterances configured for the S3Quiz intent*

```
📷 [ SCREENSHOT: S3Quiz Intent — Sample Utterances ]
```

---

### Initial Response — Welcome Message + Question 1
> *Screenshot of the initial response message showing the welcome text and Question 1*

```
📷 [ SCREENSHOT: Initial Response — Welcome + Q1 ]
```

---

### Slot Configuration — QuizAnswer1
> *Screenshot showing the QuizAnswer1 slot with custom slot type QuizAnswerType and values A, B, C*

```
📷 [ SCREENSHOT: QuizAnswer1 Slot Configuration ]
```

---

### Conditional Branching — Question 1
> *Screenshot of the conditional branches for QuizAnswer1 showing Branch 1 (A = correct), Branch 2 (B = wrong), Branch 3 (C = wrong), and Default*

```
📷 [ SCREENSHOT: QuizAnswer1 Conditional Branches ]
```

---

### Branching Logic — Correct Answer Response
> *Screenshot showing the correct answer response and ElicitSlot next step pointing to QuizAnswer2*

```
📷 [ SCREENSHOT: Correct Answer Branch — ElicitSlot to QuizAnswer2 ]
```

---

### FallbackIntent — Welcome Message
> *Screenshot of the FallbackIntent closing response showing the Sir Talk-A-Lot welcome message*

```
📷 [ SCREENSHOT: FallbackIntent — Welcome Message ]
```

---

### Live Test — Full Quiz In Action
> *Screenshot of the test window showing a full quiz run from Start quiz to Quiz Complete*

```
📷 [ SCREENSHOT: Test Window — Full Quiz Run ]
```

---

### Successfully Built Message
> *Screenshot showing the green Successfully built confirmation message*

```
📷 [ SCREENSHOT: Successfully Built Confirmation ]
```

---

## ⚙️ Technical Challenges & Solutions

Building Sir Talk-A-Lot wasn't without its challenges. Here's what we encountered and how we solved it:

| Challenge | Solution |
|-----------|----------|
| Invalid conditional expression error | Changed syntax from `SlotName = A` to `{SlotName} = "A"` |
| Bot looping back to welcome message | Changed Slot capture failure response from FallbackIntent to Wait for user input |
| Single letters A/B/C not recognised | Created custom slot type `QuizAnswerType` instead of AMAZON.AlphaNumeric |
| ElicitSlot invalid slotToElicit error | Set all slots as Required and set correct Next step in each branch |
| Closing response not showing | Turned on the Active toggle on the Closing response section |

---

## 👥 Meet The Team

| Member | Role | Contribution |
|--------|------|-------------|
| Neo | Bot Architect & Builder | Built the entire bot in AWS Lex, configured all slots, branching logic, and debugged all errors |
| Member 2 | Content Researcher | Researched Amazon S3 facts and wrote quiz questions and answers |
| Member 3 | PowerPoint Designer | Built the client presentation slides |
| Member 4 | Script Writer | Wrote the Sir Talk-A-Lot script and conversation flow |
| Member 5 | Presenter | Delivered the live demo and presentation to CloudLearners Inc. |

---

## 📚 What We Learned

Through building Sir Talk-A-Lot we developed skills in:

- ✅ Designing and deploying a chatbot using **Amazon Lex**
- ✅ Creating **intent-driven** conversational flows
- ✅ Implementing **branching logic** for dynamic responses
- ✅ Debugging **AWS Lex build errors** independently
- ✅ Using **custom slot types** for precise input capture
- ✅ Configuring **ElicitSlot** next steps for multi-question flows
- ✅ Presenting **technical solutions** to a non-technical audience
- ✅ Collaborating as a team on a **cloud-based project**

---

## 🔗 Resources

- [Amazon Lex Documentation](https://docs.aws.amazon.com/lex/)
- [AWS re/Start Programme](https://aws.amazon.com/training/restart/)
- [Praesignis](https://www.praesignis.com)
- [Amazon S3 Documentation](https://docs.aws.amazon.com/s3/)

---

## 📄 Licence

This project was built for educational purposes as part of the **Praesignis AWS re/Start Programme — Project 3.**

---

<div align="center">

Built with 💪 and ☁️ by the Sir Talk-A-Lot Team

*Praesignis AWS re/Start Programme 2026*

**"Keep stacking those cloud skills ☁️"**

</div>
