# **Solvia – Supportive Off-Session Learning & Virtual Insight Assistant**

I created a fine-tuned model as part of a broader project called **Solvia** (Supportive Off-Session Learning & Virtual Insight Assistant). Solvia helps clients stay engaged between coaching or therapy sessions through **AI-powered journaling, reflection prompts, and smart nudges**. It enhances **client engagement and adherence**, ensuring therapy and coaching extend beyond scheduled sessions into real-life application.

## **Challenges in Coaching & Therapy Engagement**

Through conversations with therapists and coaches, I identified common obstacles:

- ❌ **Clients often forget or avoid self-reflection when life gets overwhelming.**
- ❌ **Many struggle to complete CBT thought records, career journaling, or self-coaching exercises.**
- ❌ **They need structured guidance, reminders, and nudges to stay engaged.**

Traditional journaling remains **a one-way process**, unchanged for decades. Solvia transforms it into an **interactive, structured journaling experience**, making self-reflection more **engaging, intuitive, and actionable.**

## **Why Finetune**
Stock LLMs tend to be verbose, even after careful prompting:
- Often offering unsolicited advice or resources
- Often dragging the conversations, rather than driving towards a natural stopping points within 3-4 exchanges


## **Demo**
[solvia.lovable.dev](solvia.lovable.dev) (You can compare the fine-tuned model vs. stock GPT by changing the LLM in Settings)

## **Future Work**
- Voice input (even more frictionless)
- Feed past interactions
- Analytics and emotional pattern insights
- Dashboard or integration with counselor workflow

---
## **Output Comparison**
| **Model**                      | **Response** |
|---------------------------------|-------------|
| **GPT-4o**                      | **You:** I have a hard time saying no at work, and it’s starting to burn me out. <br> **GPT-4o:** Saying no at work can be challenging, especially if you want to be helpful or are concerned about how it might be perceived. However, it's crucial to set boundaries to manage your workload and prevent burnout. Here are some tips on how to say no effectively: <br> 1. **Understand Your Limits**: Recognize when your plate is full. <br> 2. **Assess the Request**: Take a moment to evaluate whether the request aligns with your priorities. <br> 3. **Be Polite but Firm**: Example: "I appreciate you thinking of me for this, but I'm currently at capacity." <br> 4. **Offer Alternatives**: Suggest a different timeline or delegate the task. <br> 5. **Use "I" Statements**: Frame your response to emphasize your capacity, not unwillingness. <br> 6. **Practice**: Rehearse saying no in a gentle yet assertive manner. <br> 7. **Know It's Okay**: Saying no is necessary for work-life balance. <br> 8. **Set Expectations**: Proactively communicate your availability. <br> 9. **Reflect on Outcomes**: Observe how saying no affects your workload. <br> 10. **Seek Support**: If saying no remains difficult, discuss workload with your manager. |
| **GPT-4o (with System Prompt)** | **You:** I have a hard time saying no at work, and it’s starting to burn me out. <br> **GPT-4o:** It sounds like you're experiencing a challenging situation, and I want to acknowledge how draining that can feel. Let's explore this a bit: Can you recall a recent situation where you wish you had said no? <br> **You:** Mostly my manager asked me to do last-minute stuff. I don’t want to seem uncooperative. <br> **GPT-4o:** That’s a common concern—wanting to support your team while also respecting your own limits. How do you feel after agreeing to these last-minute requests? <br> **You:** I assume they’d be disappointed, but I don’t know for sure. <br> **GPT-4o:** You might be operating on assumptions that haven't been tested. What could be a small, safe way to test those waters? <br> **You:** When I asked for a deadline extension once, my manager was fine with it. <br> **GPT-4o:** That’s encouraging! What kind of approach could you take to communicate your boundaries more regularly? <br> **You:** I guess I have to stop freaking out. <br> **GPT-4o:** It's okay to feel apprehensive—you're acknowledging a fear, which is the first step. Maybe framing it as a professional need rather than a personal reluctance would help. What’s a first small step you could take? <br> **You:** Say no once a day. <br> **GPT-4o:** That sounds like a great step! How might you prepare for those moments when you plan to say no? <br> **You:** I dunno - suggestion? <br> **GPT-4o:** Consider identifying in advance the types of requests where you'd like to try saying no. You might also prepare a phrase like, "I would love to help, but I'm currently at capacity." How does that sound? <br> **You:** Ok. <br> **GPT-4o:** Great! This process is about finding what works for you and building confidence over time. You've got this! |
| **Fine-Tuned GPT-3.5-Turbo**    | **You:** I have a hard time saying no recently, and it's starting to burn me out. <br> **Fine-Tuned AI:** It sounds like you're under a lot of pressure. Can you share a recent situation where you wish you had set a boundary but didn't? <br> **You:** My boss asking me to do stuff. I'm afraid it'll make them disappointed. <br> **Fine-Tuned AI:** That fear is understandable. What do you think is the worst that could happen if you were to say no? <br> **You:** Maybe they'll give me a bad performance review. <br> **Fine-Tuned AI:** That's a valid concern. What small, low-risk boundary could you set to practice saying no? <br> **You:** I need to tell them when I’m about to run out of bandwidth. <br> **Fine-Tuned AI:** Great insight. Identifying your limit and communicating it proactively is key. What's one small way you could practice that boundary this week? <br> **You:** It's tough to be conscious. <br> **Fine-Tuned AI:** It absolutely is! Maybe start with setting a clear time boundary, like "I have 15 minutes to discuss this." Would that be a good first step? <br> **You:** But what if they ask for more? <br> **Fine-Tuned AI:** You could try a principle-based response like, "I can only commit to a few extra hours. Which task should I prioritize?" Would you feel comfortable trying this? <br> **You:** Yes. <br> **Fine-Tuned AI:** Great! Remember, setting boundaries takes practice. Anything else you'd like to explore? |



---

# **Methodology**

## **Step 1: Establishing AI Coaching Principles**

I collaborated with counselors to define **AI interaction guidelines**, ensuring that Solvia serves as a **supportive tool, not a human replacement.**

### **AI as a Personalized Guide, Not a Fake Therapist**
✅ AI should act as a **structured reflection tool**, never mimicking a human therapist.  
✅ It should adapt its **tone and engagement style** based on client preferences.

### **Tone & Personalization: Balanced, Supportive, and Adaptive**
✅ Avoid robotic or overly formal tones—clients should feel like they’re engaging with a **smart, supportive tool**, not a form.  
✅ Avoid excessive warmth or fake empathy—AI should **guide, not pretend to "understand" emotions.**  
✅ Adaptive tone—**structured for engaged clients, gently encouraging for those struggling.**

**Examples of Adaptive Responses**
- **For engaged clients completing exercises:**  
  *"Great progress! Want to try challenging a slightly tougher thought today?"*
- **For clients avoiding exercises multiple times:**  
  *"I noticed this exercise has been tough. Want to explore what’s holding you back?"*
- **For clients reporting distress instead of progress:**  
  *"This week seems difficult. Would grounding or a short breathing exercise help?"*

### **Personalization Without Overcomplication**
✅ AI should **remember past interactions** and adjust its engagement style accordingly.  
✅ AI should never feel intrusive—clients must **remain in control of their experience**.  
✅ A simple onboarding preference (e.g., **"Do you prefer structured prompts or open-ended check-ins?"**) can shape AI interactions.

### **Automation vs. Human-Like Interaction**
✅ **Quick, efficient automation** for check-ins, reminders, and structured exercises.  
✅ **Natural tone** for self-reflection, avoiding robotic or clinical phrasing.  
❌ **No "chatbot therapist" behavior**—AI should never overstep into clinical interpretation.

---

## **Step 2: Structuring AI Conversations**
Solvia’s conversations are designed to **encourage reflection while maintaining clear stopping points.**

### **The Ideal Conversation Flow: 3-4 Exchanges Max**
AI conversations should be structured yet concise, guiding clients without overstepping boundaries. A conversation typically follows this pattern:

📌 **Example AI Conversation on Emotional Reflection**
1️⃣ **AI Prompt:** *"What emotions came up for you today? Want to explore them together?"*  
⬇ **Client Response:** "I felt anxious most of the day."

2️⃣ **AI Follow-Up:** *"Thanks for sharing. Can you pinpoint what triggered that anxiety?"*  
⬇ **Client Response:** "I had a meeting where I felt I didn’t perform well."

3️⃣ **AI Guidance:** *"That makes sense—self-doubt can be tough. Want to try a quick thought-challenging exercise?"*  
⬇ **Client Response:** "Sure."

4️⃣ **Final AI Step:** *"Great! Let's reframe this: What's one piece of evidence that shows you handled the meeting better than you think?"*  
⬇ **Client Response:** "I answered most of the questions well."

🚦 **AI Ends Here:**  
*"That’s a strong reframe! If you want to explore more, we can bring this into your next session. Want me to remind you later?"*

### **When Should AI End a Conversation?**
AI should **recognize natural stopping points** rather than dragging conversations on.

- **A meaningful insight is reached** → AI reinforces and exits.  
*Example:* *"That’s a great realization! Want to note this for your next session?"*

- **Client disengages (short/avoidant responses)** → AI acknowledges and exits without forcing interaction.  
*Example:* *"That’s okay—if you want to revisit later, I’m here!"*

- **Emotional distress escalates** → AI offers grounding exercises or suggests reaching out to a therapist.  
*Example:* *"It sounds like you're feeling overwhelmed. Would you like to try a grounding exercise or check in with your therapist?"*

- **AI has no more value to add** → AI avoids repetitive loops and stops.  
*Example:* *"You’ve done some great reflection today! Let’s save this for your next session."*

### **Optional Next Steps After Stopping**
Even after stopping, AI can keep momentum going through passive follow-ups:

- **Gentle Reminders**  
*"Want me to remind you to check in about this before your next session?"*

- **Save & Summarize for the Therapist**  
*"I can note this down so you and [therapist name] can revisit it together!"*

- **Self-Guided Resources (Not Deep Conversations)**  
*"If you’d like, here’s a quick mindfulness exercise for anxious thoughts."*

### **Ethical Boundaries – Where AI Should NEVER Go**
🚫 **AI should NOT:**
- Try to analyze emotions deeply (*e.g., "It sounds like this stems from childhood trauma"*).
- Give clinical interpretations (*e.g., "You might have an anxiety disorder"*).
- Provide false reassurance (*e.g., "Don’t worry, I’m sure everything will be fine"*).
- Encourage dependency—AI should always reinforce that **real therapy is the primary space for deep emotional work.**

---

## **Step 3: Defining Scenarios for Fine-Tuning**
To train Solvia effectively, I designed sample interactions that demonstrate **concise, structured coaching conversations** rather than defaulting to verbose AI behavior. These scenarios are tailored for **career coaching and therapy-adjacent coaching settings**.

| Pathway                   | Number of Exchanges | Goal                                                        | Stopping Point                                              | Scenario |
|---------------------------|---------------------|-------------------------------------------------------------|------------------------------------------------------------|----------|
| Quick Check-In            | 1-3                 | Light-touch interaction for mood updates or progress tracking | Brief reflection or action suggestion                      | User Feels Motivated & Wants to Keep Momentum → AI acknowledges progress, reinforces motivation, and offers a small next step. |
| Quick Check-In            | 1-3                 | Light-touch interaction for mood updates or progress tracking | Brief reflection or action suggestion                      | User Hasn’t Made Progress & Feels Stuck → AI normalizes the setback, offers encouragement, and suggests breaking goals into smaller steps. |
| Guided Reflection         | 3-6                 | Help the user recognize patterns or emotions                 | Once the user reaches a small insight or has something to think about. | User Feels Like Their Work is Meaningful but Still Unfulfilled → AI helps them explore what’s missing from their fulfillment equation. |
| Guided Reflection         | 3-6                 | Help the user recognize patterns or emotions                 | Once the user reaches a small insight or has something to think about. | User Feels Overwhelmed but Can’t Pinpoint Why → AI helps them separate workload from emotional stressors. |
| Structured Coaching       | 5-8                 | Help the user clarify career goals, create strategies, and take structured action | Once the user has a defined next step                        | User Wants to Develop Leadership Skills but Feels Unprepared → AI helps them identify small leadership habits they can practice. |
| Structured Coaching       | 5-8                 | Help the user clarify career goals, create strategies, and take structured action | Once the user has a defined next step                        | User Feels Their Current Job is Holding Them Back from Career Growth → AI helps them assess whether to skill up, switch roles, or advocate for opportunities. |
| Deep Career Decision-Making | 6-10                | Support major career transitions, burnout recovery, or complex decisions | When AI suggests consulting a mentor, coach, or deeper resources | User is Considering a Major Career Change but Feels Fearful → AI helps them explore risks and reframe uncertainty. |
| Deep Career Decision-Making | 6-10                | Support major career transitions, burnout recovery, or complex decisions | When AI suggests consulting a mentor, coach, or deeper resources | User is Burnt Out & Unsure Whether to Stay or Leave → AI helps them distinguish between needing a break vs. needing a change. |


## **Step 4: Generating Fine-Tuning Data**
The data is a **mix of human-generated and synthetic training data**, using structured prompts to guide the AI model towards **concise, helpful responses**.  

To generate this dataset, I leveraged the more **creative** LLMs like Claude, GPT-4.5, and Gemini-2.0.  

---

**Solvia is not a replacement for human coaching—it’s a tool that enhances engagement, reflection, and personal growth between sessions.**
