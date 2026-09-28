# Case Intake Optimization Playbook
## Personal Injury Law Firm Operations Manual

**Version:** 1.0
**Last Updated:** January 2026
**Classification:** Internal Use Only

---

## Table of Contents

1. [Executive Summary](#executive-summary)
2. [Intake Process](#intake-process)
3. [Lead Qualification](#lead-qualification)
4. [Conversion Optimization](#conversion-optimization)
5. [Technology Stack](#technology-stack)
6. [Appendices](#appendices)

---

# Executive Summary

This playbook provides comprehensive protocols for optimizing case intake operations at a personal injury law firm. The goal is to maximize qualified case acquisition while maintaining ethical standards and providing exceptional client experience from first contact.

**Key Performance Targets:**
- Speed-to-lead: < 5 minutes during business hours
- First-call resolution rate: > 60%
- Qualified lead conversion rate: > 35%
- Retainer signing within 48 hours: > 70%
- Client satisfaction score: > 4.5/5

---

# Intake Process

## 1. Phone Intake System

### 1.1 Call Flow Architecture

```
┌─────────────────┐
│  Incoming Call  │
└────────┬────────┘
         │
         ▼
┌─────────────────┐     ┌──────────────────┐
│   IVR Greeting  │────►│  Route by Type   │
└─────────────────┘     └────────┬─────────┘
                                 │
         ┌───────────────────────┼───────────────────────┐
         │                       │                       │
         ▼                       ▼                       ▼
┌─────────────────┐   ┌─────────────────┐   ┌─────────────────┐
│   New Intake    │   │ Existing Client │   │  Vendor/Other   │
└────────┬────────┘   └────────┬────────┘   └────────┬────────┘
         │                     │                     │
         ▼                     ▼                     ▼
┌─────────────────┐   ┌─────────────────┐   ┌─────────────────┐
│ Intake Specialist│   │   Case Manager  │   │   Reception     │
└─────────────────┘   └─────────────────┘   └─────────────────┘
```

### 1.2 IVR Script

```
[Ring - Maximum 2 rings before answer]

"Thank you for calling [Firm Name]. If this is an emergency,
please hang up and dial 911.

For English, press 1 or stay on the line.
Para español, oprima el número 2.

If you've been injured and would like to speak with someone
about a potential case, press 1.

If you're an existing client, press 2.

For all other inquiries, press 3.

[If no selection after 5 seconds]
Please hold while we connect you with the next available
representative."
```

### 1.3 Phone Intake Script Templates

#### INITIAL GREETING SCRIPT

```
INTAKE SPECIALIST:
"Good [morning/afternoon/evening], thank you for calling [Firm Name].
My name is [Name], and I'm here to help you. May I ask who I'm
speaking with today?"

[Wait for response - Note caller's name]

"Thank you, [Caller Name]. I understand you may be going through
a difficult time right now. Before we begin, I want you to know
that everything you share with me today is confidential and
there's no obligation. How are you feeling today?"

[Allow empathetic pause - acknowledge their response]

"I appreciate you sharing that with me. To make sure I can help
you in the best way possible, may I ask you a few questions
about what happened?"
```

#### ACCIDENT INFORMATION GATHERING SCRIPT

```
INTAKE SPECIALIST:
"Let's start with some basic information about the incident.

1. INCIDENT TYPE
   'Can you tell me, in your own words, what happened?'
   [Listen actively - do not interrupt]
   [Note: type of accident, circumstances, other parties involved]

2. DATE AND LOCATION
   'When did this happen?'
   [If recent: express concern]
   [If older: note statute of limitations considerations]

   'Where did the accident occur - what city and state?'
   [Verify jurisdiction]

3. INJURIES
   'I'm sorry to hear about what you've been through. Can you
   tell me about any injuries you received?'

   [Follow-up questions:]
   - 'Did you go to the hospital or see a doctor?'
   - 'Are you still receiving medical treatment?'
   - 'How are these injuries affecting your daily life?'

4. OTHER PARTIES
   'Was anyone else involved in this incident?'

   [For auto accidents:]
   - 'Do you know if the other driver had insurance?'
   - 'Was a police report filed?'
   - 'Were there any witnesses?'

5. PRIOR REPRESENTATION
   'Have you spoken with any other attorneys about this matter?'
   [If yes: 'Are you currently represented?']
   [Note: Cannot solicit if represented]

6. DOCUMENTATION
   'Do you have any photos, medical records, or other
   documentation related to the incident?'
```

#### EMPATHY STATEMENTS (USE THROUGHOUT)

```
SITUATION-APPROPRIATE RESPONSES:

For serious injuries:
"I'm so sorry you're dealing with this. What you're going
through sounds incredibly difficult."

For frustration with insurance:
"That must be very frustrating. Insurance companies often
make this process harder than it needs to be."

For financial stress:
"I understand. Medical bills and lost wages can create
tremendous pressure on families."

For uncertainty:
"It's completely normal to have questions. That's exactly
why we're here."

For emotional distress:
"Please take your time. There's no rush, and I'm here
to listen."
```

#### QUALIFICATION TRANSITION SCRIPT

```
INTAKE SPECIALIST:
"Thank you for sharing all of that with me, [Caller Name].
Based on what you've told me, I'd like to have one of our
attorneys review your case.

Before I do that, I just need to gather a bit more information
to make sure we can provide you with the best possible
assistance.

[Proceed to contact information collection]

'What's the best phone number to reach you?'
'And your email address?'
'What's your current mailing address?'

'What's the best time for someone to call you back if needed?'
'Is it okay to leave a voicemail at this number?'
'Is it okay to send text messages to this number?'"
```

#### CLOSING SCRIPTS

**For Qualified Cases - Immediate Attorney Review:**
```
"[Caller Name], based on what you've shared with me today,
I believe one of our attorneys will want to speak with you
about your case.

[Option A - Attorney Available:]
'I have an attorney available right now. Would you be able
to hold for just a moment while I bring them up to speed?'

[Option B - Callback Required:]
'Our attorney, [Name], will be calling you within the next
[timeframe]. They will have reviewed all the information
you've provided. Is [phone number] still the best number
to reach you?'

In the meantime, here are a few important things to remember:
- Don't speak with the other party's insurance company
  without consulting us first
- Keep all documentation related to your accident
- Continue following your doctor's treatment plan
- Save any receipts for expenses related to your injuries

Do you have any questions for me right now?"
```

**For Cases Requiring Further Review:**
```
"Thank you for taking the time to speak with me today,
[Caller Name]. Your case will be reviewed by our legal team,
and someone will be in touch within [24-48 hours] to discuss
next steps.

Is there anything else you'd like to add before we wrap up?"
```

**For Cases We Cannot Accept:**
```
"[Caller Name], I appreciate you taking the time to share
your situation with me. After reviewing the details,
unfortunately this isn't a case our firm is able to take on
at this time.

[Provide brief, honest reason without providing legal advice]

I would encourage you to:
- Contact your state bar association's lawyer referral service
  at [phone number]
- Speak with another attorney who may specialize in this area
- [If applicable] Be aware that there may be time limits for
  filing a claim

I'm sorry we couldn't be of more help, but I wish you the
very best in resolving this matter."
```

### 1.4 Call Quality Scorecard

| Criteria | Points | Description |
|----------|--------|-------------|
| Greeting | 10 | Professional, warm, identified self and firm |
| Empathy | 15 | Demonstrated genuine concern throughout |
| Information Gathering | 20 | Collected all required data points |
| Active Listening | 15 | Didn't interrupt, acknowledged responses |
| Qualification | 15 | Properly assessed case viability |
| Expectations Setting | 10 | Clear next steps communicated |
| Closing | 10 | Professional, offered additional help |
| Compliance | 5 | Followed all legal/ethical requirements |
| **Total** | **100** | Minimum passing score: 80 |

---

## 2. Web Form Optimization

### 2.1 Form Design Principles

**Above-the-Fold Requirements:**
- Headline emphasizing value proposition
- Trust indicators (awards, case results, reviews)
- Minimal initial fields (name, phone, email, brief description)
- Clear privacy statement
- Mobile-responsive design

### 2.2 Optimized Contact Form Structure

#### PRIMARY INTAKE FORM (Homepage/Landing Pages)

```html
<!-- Form Structure - Implementation Reference -->

STEP 1: Initial Contact (Above the Fold)
┌─────────────────────────────────────────────────────────────┐
│  FREE CASE EVALUATION                                       │
│  Get the compensation you deserve                           │
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ First Name*                                          │   │
│  └─────────────────────────────────────────────────────┘   │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ Phone Number*                                        │   │
│  └─────────────────────────────────────────────────────┘   │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ Email Address*                                       │   │
│  └─────────────────────────────────────────────────────┘   │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ Type of Accident ▼                                   │   │
│  │  - Car Accident                                      │   │
│  │  - Truck Accident                                    │   │
│  │  - Motorcycle Accident                               │   │
│  │  - Slip and Fall                                     │   │
│  │  - Medical Malpractice                               │   │
│  │  - Workplace Injury                                  │   │
│  │  - Other                                             │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│           [ GET MY FREE CONSULTATION ]                      │
│                                                             │
│  🔒 Your information is secure and confidential            │
│  ⭐ Rated 4.9/5 from 500+ client reviews                   │
└─────────────────────────────────────────────────────────────┘

STEP 2: Progressive Disclosure (After Initial Submit)
┌─────────────────────────────────────────────────────────────┐
│  Thank you! Just a few more details to help us evaluate    │
│  your case:                                                 │
│                                                             │
│  When did the accident occur?*                             │
│  ┌──────────┐                                              │
│  │ MM/DD/YY │                                              │
│  └──────────┘                                              │
│                                                             │
│  Where did it happen? (City, State)*                       │
│  ┌─────────────────────────────────────────────────────┐   │
│  │                                                      │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  Briefly describe what happened:*                          │
│  ┌─────────────────────────────────────────────────────┐   │
│  │                                                      │   │
│  │                                                      │   │
│  │                                                      │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  Were you injured?*  ○ Yes  ○ No                           │
│                                                             │
│  Did you seek medical treatment?*  ○ Yes  ○ No             │
│                                                             │
│  Are you currently represented by an attorney?*            │
│  ○ Yes  ○ No                                               │
│                                                             │
│  Best time to call:                                        │
│  ○ Morning  ○ Afternoon  ○ Evening  ○ Anytime              │
│                                                             │
│           [ SUBMIT FOR FREE REVIEW ]                        │
└─────────────────────────────────────────────────────────────┘
```

### 2.3 Form Field Validation Rules

```
FIELD VALIDATION SPECIFICATIONS:

First Name:
- Required: Yes
- Min length: 2 characters
- Max length: 50 characters
- Pattern: Letters, hyphens, apostrophes only
- Error message: "Please enter your first name"

Phone Number:
- Required: Yes
- Format: Accept any format, normalize to (XXX) XXX-XXXX
- Validation: Must be valid US phone number
- Error message: "Please enter a valid phone number"

Email Address:
- Required: Yes
- Pattern: Standard email regex
- Error message: "Please enter a valid email address"

Accident Date:
- Required: Yes
- Validation: Cannot be future date
- Validation: Flag if > 2 years ago (statute concerns)
- Error message: "Please enter a valid date"

Description:
- Required: Yes
- Min length: 20 characters
- Max length: 2000 characters
- Error message: "Please provide more details (at least 20 characters)"
```

### 2.4 Thank You Page Optimization

```
THANK YOU PAGE ELEMENTS:

┌─────────────────────────────────────────────────────────────┐
│                                                             │
│  ✓ YOUR INFORMATION HAS BEEN RECEIVED                      │
│                                                             │
│  Thank you, [First Name]. A member of our legal team will  │
│  contact you within [X minutes/hours].                      │
│                                                             │
│  YOUR REFERENCE NUMBER: [Auto-generated]                   │
│                                                             │
│  ─────────────────────────────────────────────────────     │
│                                                             │
│  WHAT HAPPENS NEXT:                                        │
│                                                             │
│  1. ☐ Case Review                                          │
│     Our team is reviewing your information now              │
│                                                             │
│  2. ☐ Personal Call                                        │
│     An intake specialist will call you shortly              │
│                                                             │
│  3. ☐ Free Consultation                                    │
│     Discuss your case with an experienced attorney          │
│                                                             │
│  ─────────────────────────────────────────────────────     │
│                                                             │
│  WHILE YOU WAIT:                                           │
│                                                             │
│  📹 Watch: What to Expect in Your Free Consultation        │
│     [Embedded Video - 2 minutes]                           │
│                                                             │
│  📋 Download: Accident Documentation Checklist             │
│     [PDF Download Button]                                  │
│                                                             │
│  📞 Need immediate assistance? Call: [Phone Number]        │
│                                                             │
│  ─────────────────────────────────────────────────────     │
│                                                             │
│  CLIENT TESTIMONIALS:                                      │
│  [Rotating testimonial carousel]                           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 2.5 A/B Testing Protocol

| Test Element | Variation A | Variation B | Success Metric |
|--------------|-------------|-------------|----------------|
| CTA Button Text | "Get Free Consultation" | "Start My Free Case Review" | Form completion rate |
| Form Length | 4 fields | 6 fields | Submission rate |
| Trust Badges | Awards only | Awards + Reviews | Conversion rate |
| Headline | Empathy-focused | Results-focused | Submission rate |
| Form Position | Right sidebar | Center page | Submission rate |

---

## 3. Chat Intake Best Practices

### 3.1 Chat System Architecture

```
CHAT FLOW DECISION TREE:

Website Visitor
      │
      ▼
┌─────────────┐
│ Chat Widget │ (Proactive trigger after 30 seconds)
└──────┬──────┘
       │
       ▼
┌──────────────────┐     ┌─────────────────┐
│   AI Chatbot     │────►│ Human Handoff   │
│  (Initial Triage)│     │   Triggers      │
└──────────────────┘     └─────────────────┘
       │                         │
       │    ┌────────────────────┤
       │    │                    │
       ▼    ▼                    ▼
┌──────────────┐    ┌────────────────────┐
│   Qualified  │    │   Live Intake      │
│     Lead     │    │   Specialist       │
│  (Captured)  │    │   (Immediate)      │
└──────────────┘    └────────────────────┘
```

### 3.2 Chatbot Script Flow

#### PROACTIVE CHAT TRIGGER

```
[Trigger: Visitor on site > 30 seconds, scrolled > 50%]

BOT: "Hi there! 👋 I'm here to help if you have any questions
about your potential case. Were you or a loved one recently
injured?"

[Quick Reply Buttons:]
[ Yes, I need help ]  [ Just browsing ]  [ Have a question ]
```

#### QUALIFICATION CONVERSATION FLOW

```
USER: [Clicks "Yes, I need help"]

BOT: "I'm sorry to hear that. I'd like to help connect you
with the right person on our team.

First, can you tell me what type of incident occurred?

[ Car Accident ]
[ Truck Accident ]
[ Slip and Fall ]
[ Medical Issue ]
[ Workplace Injury ]
[ Something Else ]"

USER: [Clicks "Car Accident"]

BOT: "Thank you. Car accident cases are one of our primary
areas of focus.

When did the accident happen?

[ Within the last week ]
[ Within the last month ]
[ 1-6 months ago ]
[ 6-12 months ago ]
[ Over a year ago ]"

USER: [Clicks "Within the last month"]

BOT: "I understand. Were you injured in the accident?

[ Yes, I was injured ]
[ No injuries ]
[ Not sure yet ]"

USER: [Clicks "Yes, I was injured"]

BOT: "I'm sorry to hear that. Have you been able to see a
doctor or receive medical treatment?

[ Yes, I've seen a doctor ]
[ No, not yet ]
[ Going soon ]"

USER: [Clicks "Yes, I've seen a doctor"]

BOT: "Good - it's important to document your injuries.

One more question: Are you currently working with another
attorney on this matter?

[ No, I'm not ]
[ Yes, I am ]
[ I was, but not anymore ]"

USER: [Clicks "No, I'm not"]

BOT: "Thank you for that information. Based on what you've
shared, I'd like to connect you with one of our intake
specialists who can discuss your case in more detail.

To do that, I just need a bit of contact information:

What's your first name?"

USER: [Types name]

BOT: "Nice to meet you, [Name]. What's the best phone number
to reach you?"

USER: [Types phone]

BOT: "And your email address?"

USER: [Types email]

BOT: "Perfect! Here's what happens next:

✓ Your information has been sent to our team
✓ An intake specialist will call you within 5 minutes
✓ If you prefer, you can also call us directly at [number]

Is there anything specific you'd like to tell them before
they call?"

[Text input field]

BOT: "Thank you, [Name]. We'll be in touch very shortly.
In the meantime, is there anything else I can help you with?"

[ No, I'll wait for the call ]
[ I have another question ]
[ I'd prefer to call now ]
```

### 3.3 Human Handoff Triggers

| Trigger Condition | Action |
|-------------------|--------|
| Visitor types "speak to someone" or similar | Immediate handoff |
| Visitor expresses frustration | Immediate handoff |
| Complex case type detected | Immediate handoff |
| High-value indicators present | Priority handoff |
| Bot cannot answer question | Handoff with context |
| Visitor requests callback | Capture info + handoff |
| Business hours + qualified lead | Immediate handoff |
| After hours + qualified lead | Capture info + schedule callback |

### 3.4 Chat Response Time Standards

| Scenario | Target Response Time |
|----------|---------------------|
| Initial bot response | < 3 seconds |
| Bot follow-up messages | < 2 seconds |
| Human handoff connection | < 30 seconds |
| Live agent first response | < 60 seconds |
| Live agent subsequent responses | < 90 seconds |

---

## 4. After-Hours Intake Solutions

### 4.1 After-Hours System Options

```
TIERED AFTER-HOURS APPROACH:

TIER 1: Automated Systems (Always Active)
├── Website chat bot (24/7)
├── Web form submissions (24/7)
├── SMS auto-responder
└── Email auto-responder

TIER 2: Answering Service (Extended Hours)
├── Live operators
├── Basic qualification script
├── Warm transfer capability (if attorney on-call)
└── Message taking with priority flagging

TIER 3: On-Call Attorney (Emergency)
├── Severe injury cases only
├── Rotational schedule
├── Direct callback within 30 minutes
└── Weekend/holiday coverage
```

### 4.2 Answering Service Script

```
AFTER-HOURS ANSWERING SERVICE SCRIPT:

OPERATOR: "Thank you for calling [Firm Name]. Our office is
currently closed, but I can help you. My name is [Name].
Are you calling about a potential new case?"

[If YES:]

OPERATOR: "I'd be happy to take some information so one of
our attorneys can follow up with you. This should only take
a few minutes.

May I have your name please?"
[Record response]

"And a phone number where you can be reached?"
[Record response]

"What's the best time to call you back tomorrow?"
[Record response]

"Can you briefly tell me what happened?"
[Record response - listen for severity indicators]

[SEVERITY CHECK - If any of the following, escalate to on-call:]
- Death or life-threatening injury
- Currently hospitalized
- Major commercial vehicle accident
- Catastrophic injury (amputation, paralysis, severe burns)
- Mass casualty event

[If SEVERE:]
OPERATOR: "Given the seriousness of your situation, I'm going
to have one of our attorneys call you back within the next
30 minutes. Please keep your phone available. Is there
anything else you need right now?"

[If STANDARD:]
OPERATOR: "Thank you for that information. I've noted everything
you've shared. One of our intake specialists will call you
[first thing tomorrow morning / within 24 hours].

In the meantime, if this is a medical emergency, please call
911 or go to your nearest emergency room.

Is there anything else I can help you with tonight?"
```

### 4.3 After-Hours Priority Matrix

| Case Characteristics | Priority Level | Response Protocol |
|---------------------|----------------|-------------------|
| Death in family | CRITICAL | On-call attorney within 30 min |
| Currently hospitalized (serious) | CRITICAL | On-call attorney within 30 min |
| Major commercial accident | HIGH | On-call attorney within 2 hours |
| Significant injury, recent accident | HIGH | First call next business day AM |
| Moderate injury, standard accident | MEDIUM | Callback within 24 hours |
| Minor injury, information seeking | LOW | Callback within 48 hours |

### 4.4 Weekend/Holiday Coverage Schedule

```
ON-CALL ROTATION TEMPLATE:

Week 1: Attorney A (Primary) / Attorney B (Backup)
Week 2: Attorney B (Primary) / Attorney C (Backup)
Week 3: Attorney C (Primary) / Attorney A (Backup)
Week 4: Attorney A (Primary) / Attorney C (Backup)

HOLIDAY COVERAGE:
- Thanksgiving: [Assigned Attorney]
- Christmas Eve/Day: [Assigned Attorney]
- New Year's Eve/Day: [Assigned Attorney]
- Memorial Day: [Assigned Attorney]
- Labor Day: [Assigned Attorney]
- July 4th: [Assigned Attorney]

COMPENSATION:
- On-call stipend: $[X] per weekend/holiday
- Case sign-up bonus: Standard bonus applies
- Minimum response time: 30 minutes for critical cases
```

### 4.5 After-Hours Auto-Response Templates

#### EMAIL AUTO-RESPONDER

```
Subject: We Received Your Message - [Firm Name]

Dear [First Name/Valued Potential Client],

Thank you for contacting [Firm Name]. We received your message
and want you to know that your inquiry is important to us.

Our office is currently closed, but a member of our legal
team will reach out to you during our next business day,
which is [Day, Date].

OFFICE HOURS:
Monday - Friday: 8:00 AM - 6:00 PM [Timezone]
Saturday: 9:00 AM - 12:00 PM [Timezone]
Sunday: Closed

IF THIS IS AN EMERGENCY:
- For medical emergencies, please call 911
- For urgent legal matters involving serious injury,
  call our 24-hour emergency line: [Phone Number]

WHILE YOU WAIT:
- Gather any documentation related to your incident
- Take photos of injuries, property damage, or accident scenes
- Avoid speaking with insurance adjusters without legal counsel
- Keep records of all medical treatment

We look forward to speaking with you soon.

Sincerely,
The [Firm Name] Team

[Firm Address]
[Phone Number]
[Website]
```

#### SMS AUTO-RESPONDER

```
[Firm Name]: Thank you for your message. Our office is currently
closed but your inquiry has been received. We'll contact you
on the next business day. For emergencies involving serious
injury, call [Emergency Number]. Reply STOP to opt out.
```

---

# Lead Qualification

## 1. Case Screening Criteria by Case Type

### 1.1 Auto Accident Screening

```
AUTO ACCIDENT QUALIFICATION MATRIX

MUST HAVE (All Required):
┌─────────────────────────────────────────────────────────────┐
│ □ Accident occurred within statute of limitations           │
│ □ Caller was NOT at fault (or minimal comparative fault)    │
│ □ Documented injury requiring medical treatment             │
│ □ Not currently represented by another attorney             │
│ □ Accident occurred in serviceable jurisdiction             │
│ □ At-fault party has insurance or assets                    │
└─────────────────────────────────────────────────────────────┘

CASE VALUE INDICATORS:
┌─────────────────────────────────────────────────────────────┐
│ HIGH VALUE (+)                 │ LOW VALUE (-)              │
│ ────────────────────────────── │ ─────────────────────────  │
│ □ Surgery required/recommended │ □ Soft tissue only         │
│ □ Hospitalization              │ □ Pre-existing conditions  │
│ □ Broken bones/fractures       │ □ Minimal treatment        │
│ □ Multiple medical providers   │ □ Quick recovery expected  │
│ □ Lost wages documented        │ □ Low insurance limits     │
│ □ Commercial vehicle involved  │ □ Uninsured defendant      │
│ □ Clear liability              │ □ Disputed liability       │
│ □ Multiple defendants          │ □ Caller comparative fault │
│ □ Permanent injury/disability  │ □ Minor property damage    │
│ □ Policy limits > $100K        │ □ Inconsistent story       │
└─────────────────────────────────────────────────────────────┘

SCORING:
- 5+ High Value indicators = PRIORITY CASE
- 3-4 High Value indicators = STANDARD CASE
- 1-2 High Value indicators = EVALUATE FURTHER
- Majority Low Value indicators = LIKELY DECLINE
```

### 1.2 Truck Accident Screening

```
COMMERCIAL TRUCK ACCIDENT QUALIFICATION MATRIX

MUST HAVE (All Required):
┌─────────────────────────────────────────────────────────────┐
│ □ Commercial vehicle involvement confirmed                  │
│   (Semi-truck, 18-wheeler, delivery truck, bus)            │
│ □ Significant injury documented                             │
│ □ Within statute of limitations                             │
│ □ Accident occurred in serviceable jurisdiction             │
│ □ Not currently represented                                 │
└─────────────────────────────────────────────────────────────┘

PRIORITY INDICATORS (Immediate Attorney Review):
┌─────────────────────────────────────────────────────────────┐
│ □ Fatality involved                                         │
│ □ Catastrophic injury (TBI, spinal cord, amputation)       │
│ □ Multiple victims                                          │
│ □ Hazmat involvement                                        │
│ □ Major carrier involved (named trucking company)          │
│ □ Evidence of driver fatigue/hours violation               │
│ □ Evidence of intoxication                                  │
│ □ Evidence of distracted driving                            │
│ □ Vehicle defect suspected                                  │
│ □ Recent accident (within 72 hours)                         │
└─────────────────────────────────────────────────────────────┘

IMMEDIATE ACTIONS FOR QUALIFIED TRUCK CASES:
1. Escalate to senior attorney immediately
2. Dispatch investigator to scene (if within 72 hours)
3. Send spoliation letter to trucking company
4. Request black box data preservation
5. Identify and preserve witness information
```

### 1.3 Premises Liability Screening

```
PREMISES LIABILITY (SLIP/TRIP AND FALL) QUALIFICATION MATRIX

MUST HAVE (All Required):
┌─────────────────────────────────────────────────────────────┐
│ □ Incident on another party's property                      │
│ □ Property owner/manager negligence identifiable            │
│ □ Documented injury requiring medical treatment             │
│ □ Within statute of limitations                             │
│ □ Incident occurred in serviceable jurisdiction             │
│ □ Commercial property OR residential landlord               │
└─────────────────────────────────────────────────────────────┘

LIABILITY FACTORS (Must Identify At Least One):
┌─────────────────────────────────────────────────────────────┐
│ □ Known hazard not repaired                                 │
│ □ Lack of warning signs                                     │
│ □ Code violation                                            │
│ □ Inadequate maintenance                                    │
│ □ Poor lighting                                             │
│ □ Prior similar incidents                                   │
│ □ Defective condition                                       │
│ □ Weather-related hazard not addressed                      │
└─────────────────────────────────────────────────────────────┘

HIGH-VALUE PROPERTY TYPES:
□ Large retail chains (Walmart, Target, etc.)
□ Restaurant chains
□ Hotels and resorts
□ Grocery stores
□ Shopping malls
□ Apartment complexes (large management companies)
□ Casinos
□ Amusement parks
□ Government properties

LOW-VALUE/DECLINE FACTORS:
□ Private residence (homeowner)
□ Open and obvious hazard
□ Caller was trespassing
□ Minor injury only
□ No witnesses
□ No incident report filed
□ Surveillance unlikely
```

### 1.4 Medical Malpractice Screening

```
MEDICAL MALPRACTICE QUALIFICATION MATRIX

MUST HAVE (All Required):
┌─────────────────────────────────────────────────────────────┐
│ □ Treatment by licensed healthcare provider                 │
│ □ Within statute of limitations (varies by state)          │
│ □ Significant injury or death                               │
│ □ Injury causation appears linked to treatment              │
│ □ Not currently represented                                 │
│ □ Willing to obtain medical records                         │
└─────────────────────────────────────────────────────────────┘

CASE TYPE CATEGORIES:

SURGICAL ERRORS:
□ Wrong-site surgery
□ Retained surgical instruments
□ Anesthesia errors
□ Post-operative complications from negligence
□ Unnecessary surgery

DIAGNOSTIC ERRORS:
□ Delayed cancer diagnosis
□ Missed heart attack/stroke symptoms
□ Failure to diagnose infection
□ Misread imaging studies
□ Failure to order appropriate tests

MEDICATION ERRORS:
□ Wrong medication prescribed
□ Wrong dosage
□ Dangerous drug interactions
□ Pharmacy dispensing errors

BIRTH INJURIES:
□ Cerebral palsy from birth trauma
□ Erb's palsy/brachial plexus injury
□ Failure to perform timely C-section
□ Fetal monitoring failures
□ Maternal death or injury

MINIMUM THRESHOLD REQUIREMENTS:
┌─────────────────────────────────────────────────────────────┐
│ Due to high costs of medical malpractice litigation,        │
│ cases typically must meet minimum damage thresholds:        │
│                                                             │
│ - Death: ACCEPT for review                                  │
│ - Permanent disability: ACCEPT for review                   │
│ - Surgery required to correct: ACCEPT for review            │
│ - Extended hospitalization (7+ days): ACCEPT for review     │
│ - Significant lost wages (6+ months): ACCEPT for review     │
│ - Minor/temporary injury: LIKELY DECLINE                    │
└─────────────────────────────────────────────────────────────┘
```

### 1.5 Workplace Injury Screening

```
WORKPLACE INJURY QUALIFICATION MATRIX

WORKERS' COMPENSATION (Standard):
┌─────────────────────────────────────────────────────────────┐
│ □ Injury occurred during employment                         │
│ □ Employer has workers' comp insurance                      │
│ □ Significant injury affecting ability to work              │
│ □ Claim filed or assistance needed filing                   │
│ □ Dispute with employer/insurer                             │
└─────────────────────────────────────────────────────────────┘

THIRD-PARTY LIABILITY (Higher Value):
┌─────────────────────────────────────────────────────────────┐
│ □ Third party (not employer) caused injury                  │
│   - Subcontractor                                           │
│   - Property owner                                          │
│   - Equipment manufacturer                                  │
│   - Delivery driver                                         │
│ □ Defective equipment/machinery                             │
│ □ Toxic exposure from third-party product                   │
│ □ Construction site accident with multiple contractors      │
└─────────────────────────────────────────────────────────────┘

PRIORITY CASE INDICATORS:
□ Fatality
□ Catastrophic injury (amputation, paralysis, TBI, burns)
□ Industrial explosion
□ Construction collapse
□ Multi-victim incident
□ OSHA investigation initiated
□ Willful safety violations by employer
□ Third-party liability clear
```

---

## 2. Red Flags to Watch For

### 2.1 Client Red Flags

```
WARNING SIGNS DURING INTAKE:

REPRESENTATION ISSUES:
⚠️ Currently has attorney (solicitation concern)
⚠️ Recently fired previous attorney
⚠️ Has had multiple attorneys on case
⚠️ Active lawsuit already filed
⚠️ Settlement already received for same incident

CREDIBILITY CONCERNS:
⚠️ Story inconsistencies during conversation
⚠️ Vague or evasive about key details
⚠️ Unable to provide basic incident information
⚠️ Significant delay between incident and seeking help
⚠️ Prior claims history (frequent litigator)
⚠️ Exaggerated injuries not matching described accident
⚠️ Unwilling to provide medical records
⚠️ Refused/avoiding medical treatment

MOTIVATION CONCERNS:
⚠️ Primary focus on "how much can I get"
⚠️ Asking about guaranteed outcomes
⚠️ Pressure for immediate cash advance
⚠️ Mentions friend/family received large settlement
⚠️ Anger at defendant seems disproportionate

COMMUNICATION CONCERNS:
⚠️ Hostile or abusive toward staff
⚠️ Unrealistic expectations despite explanation
⚠️ Unwilling to follow intake process
⚠️ Demanding to speak only with attorney
⚠️ Threats if not immediately helped

CASE CONCERNS:
⚠️ Statute of limitations expired or imminent
⚠️ Pre-existing injury to same body part
⚠️ Caller admits significant fault
⚠️ No insurance on any party
⚠️ Minimal property damage in major injury claim
```

### 2.2 Red Flag Response Protocols

```
RED FLAG RESPONSE MATRIX:

┌──────────────────────────┬─────────────────────────────────┐
│ Red Flag                 │ Response Protocol               │
├──────────────────────────┼─────────────────────────────────┤
│ Currently represented    │ Politely decline, document      │
│                          │ conversation, do not solicit    │
├──────────────────────────┼─────────────────────────────────┤
│ Story inconsistencies    │ Ask clarifying questions,       │
│                          │ document discrepancies, flag    │
│                          │ for attorney review             │
├──────────────────────────┼─────────────────────────────────┤
│ Hostile behavior         │ Remain calm, document behavior, │
│                          │ involve supervisor if needed    │
├──────────────────────────┼─────────────────────────────────┤
│ SOL concern              │ Escalate immediately to         │
│                          │ attorney for quick evaluation   │
├──────────────────────────┼─────────────────────────────────┤
│ Multiple prior attorneys │ Obtain details on why, document │
│                          │ attorney review required        │
├──────────────────────────┼─────────────────────────────────┤
│ Pre-existing condition   │ Gather details, note for        │
│                          │ attorney, not automatic decline │
├──────────────────────────┼─────────────────────────────────┤
│ Uninsured defendant      │ Assess defendant assets,        │
│                          │ check UM/UIM coverage          │
└──────────────────────────┴─────────────────────────────────┘
```

### 2.3 Fraud Indicators

```
POTENTIAL FRAUD INDICATORS:

STAGED ACCIDENT INDICATORS:
⚠️ Multiple occupants all claiming injury
⚠️ Accident in known fraud corridor
⚠️ All occupants treating at same provider
⚠️ Vehicle damage inconsistent with injuries
⚠️ Prior similar accidents in history
⚠️ Referral from known fraud ring source

EXAGGERATION INDICATORS:
⚠️ Dramatic escalation of symptoms over time
⚠️ Injury claims far exceed impact force
⚠️ Refusing to provide recorded statement
⚠️ Unable to describe pain/symptoms specifically
⚠️ Social media contradicts claimed disability

DOCUMENTATION CONCERNS:
⚠️ Missing or altered documentation
⚠️ Inconsistent dates on records
⚠️ Provider has fraud history
⚠️ Bills seem inflated for treatment

IF FRAUD SUSPECTED:
1. Do not accuse caller
2. Continue gathering information professionally
3. Document all red flags thoroughly
4. Do not sign case without attorney review
5. Consult with firm's fraud protocol
```

---

## 3. Value Indicators

### 3.1 Case Value Assessment Framework

```
CASE VALUE CALCULATION FACTORS:

┌─────────────────────────────────────────────────────────────┐
│                    LIABILITY STRENGTH                        │
│                                                             │
│  Clear Defendant Liability (100%)          Score: 10        │
│  Strong Liability (75%+)                   Score: 8         │
│  Moderate Liability (50-75%)               Score: 5         │
│  Disputed Liability (25-50%)               Score: 3         │
│  Weak Liability (<25%)                     Score: 1         │
└─────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────┐
│                    INJURY SEVERITY                           │
│                                                             │
│  Catastrophic (death, paralysis, TBI)      Score: 10        │
│  Severe (surgery, multiple fractures)      Score: 8         │
│  Moderate (fractures, significant tissue)  Score: 5         │
│  Minor (sprains, soft tissue)              Score: 2         │
└─────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────┐
│                    RECOVERY POTENTIAL                        │
│                                                             │
│  Commercial policy ($1M+)                  Score: 10        │
│  High personal policy ($250K-$1M)          Score: 8         │
│  Standard policy ($100K-$250K)             Score: 5         │
│  Minimum limits ($25K-$100K)               Score: 3         │
│  Uninsured/low assets                      Score: 1         │
└─────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────┐
│                    DAMAGES DOCUMENTED                        │
│                                                             │
│  Extensive medical + lost wages + pain     Score: 10        │
│  Significant medical + some wage loss      Score: 7         │
│  Moderate medical treatment                Score: 5         │
│  Minimal documentation                     Score: 2         │
└─────────────────────────────────────────────────────────────┘

TOTAL SCORE INTERPRETATION:
- 35-40: Premium case - Immediate attorney involvement
- 28-34: High-value case - Priority handling
- 20-27: Standard case - Normal intake process
- 12-19: Marginal case - Careful evaluation needed
- Below 12: Likely decline - Review before rejection
```

### 3.2 High-Value Case Indicators

```
IMMEDIATE HIGH-VALUE TRIGGERS:

INJURY FACTORS:
□ Death (wrongful death claim)
□ Traumatic brain injury
□ Spinal cord injury / paralysis
□ Amputation
□ Severe burns (2nd/3rd degree, large area)
□ Multiple fractures
□ Internal organ damage
□ Permanent disfigurement
□ Loss of sensory function (vision, hearing)

LIABILITY FACTORS:
□ Commercial defendant (trucking company, corporation)
□ Government entity liability
□ Multiple defendants
□ Punitive conduct (DUI, egregious negligence)
□ Product defect
□ Clear safety violation documented
□ Prior similar incidents by defendant

DOCUMENTATION FACTORS:
□ Strong witness support
□ Video/photo evidence
□ Police report supports client
□ OSHA investigation
□ Code violations cited
□ Expert witnesses readily available

FINANCIAL FACTORS:
□ High wage earner (significant lost income)
□ High policy limits confirmed
□ Commercial insurance involved
□ Multiple insurance policies applicable
□ Defendant has substantial assets
```

---

## 4. Documentation Requirements

### 4.1 Intake Documentation Checklist

```
REQUIRED DOCUMENTATION TO REQUEST/GATHER:

ACCIDENT DOCUMENTATION:
□ Police/incident report
□ Photos of accident scene
□ Photos of vehicle damage
□ Photos of injuries
□ Witness contact information
□ Insurance information (all parties)
□ Dashcam/surveillance footage (if available)

MEDICAL DOCUMENTATION:
□ Hospital/ER records
□ Ambulance/EMS records
□ Primary care physician records
□ Specialist records
□ Physical therapy records
□ Imaging studies (X-rays, MRI, CT)
□ Surgical records (if applicable)
□ Prescription records
□ Medical bills

FINANCIAL DOCUMENTATION:
□ Lost wage verification
□ Tax returns (if self-employed)
□ Pay stubs
□ Benefits statements
□ Out-of-pocket expense receipts
□ Property damage estimates

INSURANCE DOCUMENTATION:
□ Client's auto insurance policy
□ Client's health insurance information
□ At-fault party's insurance information
□ UM/UIM coverage verification
□ Any correspondence from insurers
```

### 4.2 Intake Data Entry Standards

```
CRM DATA ENTRY REQUIREMENTS:

CONTACT INFORMATION (Required):
- Full legal name
- Date of birth
- Phone (primary + secondary)
- Email
- Mailing address
- Preferred contact method
- Best time to contact
- Communication preferences (voicemail OK, text OK)

INCIDENT INFORMATION (Required):
- Date of incident
- Time of incident (approximate)
- Location (address, city, state)
- Type of incident (standardized dropdown)
- Detailed description (narrative field)
- Police report number (if available)
- Responding agency

INJURY INFORMATION (Required):
- Injuries claimed (standardized list + free text)
- Hospitalized (Y/N)
- Hospital name
- Current treatment status
- Treating physicians (names)
- Pre-existing conditions disclosed

INSURANCE INFORMATION (As Available):
- Client's auto carrier
- Client's policy number
- At-fault party carrier
- At-fault policy number (if known)
- Health insurance carrier
- Health insurance policy number

QUALIFICATION DATA (Required):
- Currently represented (Y/N)
- Prior attorneys (Y/N, details)
- Case type classification
- Jurisdiction
- Statute of limitations date
- Value score (per matrix)
- Red flags noted

ADMINISTRATIVE (System-Generated):
- Intake date/time
- Intake specialist
- Lead source
- Campaign attribution
- Call recording link
- Follow-up status
```

---

# Conversion Optimization

## 1. Speed-to-Lead Benchmarks

### 1.1 Response Time Standards

```
SPEED-TO-LEAD REQUIREMENTS:

┌─────────────────────────────────────────────────────────────┐
│  CHANNEL          │  TARGET        │  MAXIMUM ACCEPTABLE    │
├───────────────────┼────────────────┼────────────────────────┤
│  Phone (direct)   │  Immediate     │  N/A (answered live)   │
│  Web form         │  < 5 minutes   │  15 minutes            │
│  Chat             │  < 2 minutes   │  5 minutes             │
│  Email            │  < 15 minutes  │  1 hour                │
│  Text/SMS         │  < 5 minutes   │  15 minutes            │
│  Referral         │  < 1 hour      │  4 hours               │
│  After-hours lead │  Next AM       │  Within 2 hours of     │
│                   │  (first thing) │  office opening        │
└───────────────────┴────────────────┴────────────────────────┘

WHY SPEED MATTERS:
- 78% of customers buy from the first responder
- Leads contacted within 5 minutes are 9x more likely to convert
- After 30 minutes, lead quality decreases by 21x
- Personal injury leads often contact multiple firms
```

### 1.2 Response Time Monitoring

```
SPEED-TO-LEAD DASHBOARD METRICS:

Real-Time Monitoring:
□ Current leads awaiting first contact
□ Average response time (rolling 24 hours)
□ Response time by channel
□ Response time by intake specialist
□ Leads exceeding target response time

Daily Review:
□ Total leads by channel
□ Average response time by hour
□ Response time distribution
□ Missed target percentage
□ Correlation: response time vs. conversion

Weekly Analysis:
□ Trend analysis
□ Specialist performance comparison
□ Channel performance comparison
□ Root cause analysis for misses
□ Improvement recommendations
```

### 1.3 Speed Optimization Tactics

```
TACTICS TO REDUCE RESPONSE TIME:

STAFFING:
□ Dedicated intake specialists during peak hours
□ Overflow protocols when queue exceeds threshold
□ Cross-training for backup coverage
□ Staggered shifts to cover all hours

TECHNOLOGY:
□ Automated lead alerts (push notifications)
□ Lead routing based on availability
□ Click-to-call functionality
□ Pre-populated callback screens
□ Auto-dialer for web leads

PROCESS:
□ "Hot lead" protocol for high-value indicators
□ Direct web-to-phone routing during hours
□ Voicemail drop for no-answer (immediate retry)
□ Parallel outreach (call + text + email)

ACCOUNTABILITY:
□ Real-time leaderboard display
□ Response time in performance reviews
□ Bonus tied to speed metrics
□ Alerts to management for misses
```

---

## 2. Follow-Up Sequences

### 2.1 Initial Contact Follow-Up Sequence

```
FOLLOW-UP SEQUENCE: NEW LEAD - NO CONTACT

DAY 1 (Same Day as Lead):
─────────────────────────────────────────
Attempt 1: Call (within 5 min of lead)
   └─ No answer → Leave voicemail
   └─ Immediately send text message
   └─ Send email #1 (intro + value prop)

Attempt 2: Call (2 hours after Attempt 1)
   └─ No answer → No voicemail
   └─ Send text #2

Attempt 3: Call (4 hours after Attempt 2)
   └─ No answer → Leave voicemail
   └─ Note: Different time of day

DAY 2:
─────────────────────────────────────────
Attempt 4: Call (morning, 9-10 AM)
   └─ No answer → No voicemail
   └─ Send text #3

Attempt 5: Call (afternoon, 2-3 PM)
   └─ No answer → Leave voicemail

Send email #2 (case study/testimonial)

DAY 3:
─────────────────────────────────────────
Attempt 6: Call (different time than Day 2)
   └─ No answer → No voicemail

Send text #4 (urgency message)

DAY 4:
─────────────────────────────────────────
Attempt 7: Call (morning)
   └─ No answer → Leave voicemail

Send email #3 (deadline/SOL awareness)

DAY 5:
─────────────────────────────────────────
Attempt 8: Call (afternoon)
   └─ Final voicemail

Send text #5 (final attempt message)
Send email #4 (final outreach)

DAY 7:
─────────────────────────────────────────
Move to nurture sequence (if no response)
OR
Close as "Unable to Contact"

TOTAL TOUCHES: 8 calls, 5 texts, 4 emails = 17 touches
```

### 2.2 Follow-Up Message Templates

#### VOICEMAIL SCRIPTS

```
VOICEMAIL #1 (Initial):
"Hi [Name], this is [Your Name] calling from [Firm Name].
I received your information about your [accident type] and
wanted to reach out personally to discuss your case.

We'd like to help you understand your options and answer
any questions you might have. Please call me back at
[phone number]. Again, that's [phone number].

I look forward to speaking with you soon."

VOICEMAIL #2 (Day 2):
"Hi [Name], [Your Name] from [Firm Name] again. I know
you're probably busy dealing with everything after your
accident, but I wanted to make sure you received my
previous message.

We've helped thousands of people in situations similar
to yours, and I'd love the opportunity to discuss how
we might be able to help you.

Please call me at your convenience at [phone number].
Thanks, and I hope to hear from you soon."

VOICEMAIL #3 (Final):
"Hi [Name], this is [Your Name] from [Firm Name]. This
is my final attempt to reach you regarding your [accident type]
inquiry.

I want you to know that there may be important deadlines
that could affect your case, so I encourage you to speak
with an attorney soon, even if it's not us.

If you'd still like to discuss your situation, my number
is [phone number]. I wish you the best in your recovery."
```

#### TEXT MESSAGE TEMPLATES

```
TEXT #1 (Immediate):
"Hi [Name], this is [Your Name] from [Firm Name]. I just
tried calling about your case inquiry. Please call me back
at [number] or reply to schedule a time to talk. We're here
to help."

TEXT #2 (2 hours later):
"[Name], following up on your [accident type] inquiry.
We'd like to discuss your options. When's a good time to
connect? - [Your Name], [Firm Name]"

TEXT #3 (Day 2):
"[Name], still hoping to connect with you about your case.
Many clients like you have recovered significant compensation.
Call us at [number] or reply with a good time. - [Firm Name]"

TEXT #4 (Day 3 - Urgency):
"[Name], important reminder: there are time limits to file
injury claims in [State]. We want to make sure you don't
miss any deadlines. Please call [number]. - [Firm Name]"

TEXT #5 (Final):
"[Name], this is our final outreach. If you've decided to
go a different direction, we understand. If you change your
mind, we're here: [number]. Best of luck with your recovery.
- [Firm Name]"
```

#### EMAIL TEMPLATES

```
EMAIL #1: Introduction
─────────────────────────────────────────
Subject: Your Free Case Evaluation - [Firm Name]

Dear [Name],

Thank you for contacting [Firm Name] regarding your
[accident type]. I'm reaching out personally to let you
know that your case is important to us.

I've tried calling you at [phone number] and wanted to
make sure you received my message. We understand you're
dealing with a lot right now - physical pain, medical
bills, insurance calls, and the stress of it all.

That's why we're here. Our team has helped thousands of
accident victims recover the compensation they deserve,
and we'd like to do the same for you.

HERE'S WHAT WE OFFER:
• Free, no-obligation case evaluation
• No upfront costs - we only get paid if you win
• 24/7 support throughout your case
• Experienced attorneys who specialize in [case type]

NEXT STEPS:
Simply reply to this email or call me directly at
[phone number] to schedule your free consultation.

I look forward to speaking with you.

Sincerely,
[Your Name]
[Title]
[Firm Name]
[Phone] | [Email]

---
EMAIL #2: Social Proof
─────────────────────────────────────────
Subject: How We Helped [Similar Client] After Their Accident

Dear [Name],

I wanted to follow up on my previous message and share a
quick story that might be relevant to your situation.

Recently, we represented [Client First Name], who was
involved in a [similar accident type]. Like you, [he/she]
wasn't sure what to do next or whether [he/she] even had
a case.

After our free consultation, we took on [his/her] case
and ultimately recovered [$X] in compensation for medical
bills, lost wages, and pain and suffering.

"[Brief testimonial quote]" - [Client First Name]

Every case is different, but we'd love the opportunity
to evaluate yours and let you know what options might
be available to you.

Call me at [number] or reply to this email.

Sincerely,
[Your Name]

---
EMAIL #3: Urgency/Deadline
─────────────────────────────────────────
Subject: Important Deadline Information for Your Case

Dear [Name],

I want to make sure you're aware of something important.

In [State], there are strict time limits (called statutes
of limitations) for filing personal injury claims. If you
miss these deadlines, you may lose your right to seek
compensation entirely.

For [accident type] cases in [State], the deadline is
typically [X years] from the date of the accident.

I'm not trying to pressure you - I just want to make
sure you have the information you need to make the
best decision for yourself and your family.

If you'd like to discuss your options, I'm here:
📞 [Phone Number]
📧 [Email]

Take care,
[Your Name]

---
EMAIL #4: Final Outreach
─────────────────────────────────────────
Subject: Closing Your File - [Name]

Dear [Name],

I've reached out several times regarding your [accident
type] inquiry, and I understand you may have decided
to pursue other options or may simply be too busy to
respond.

Whatever the reason, I want you to know that we're here
if you ever need us. If your situation changes, don't
hesitate to reach out.

In the meantime, I'll be closing your file in our system.
This doesn't prevent you from contacting us in the future.

A few reminders:
• Continue following your doctor's treatment plan
• Keep all documentation related to your accident
• Be cautious when speaking with insurance adjusters
• Don't miss any filing deadlines

I wish you a full recovery and the best of luck.

Sincerely,
[Your Name]
[Firm Name]
```

### 2.3 Follow-Up Tracking Matrix

```
LEAD STATUS TRACKING:

┌────────────────────────────────────────────────────────────┐
│ STATUS          │ DEFINITION               │ NEXT ACTION   │
├─────────────────┼──────────────────────────┼───────────────┤
│ New             │ Just received            │ First contact │
│ Contacted       │ Spoke with lead          │ Follow-up     │
│ Attempting      │ Outreach in progress     │ Continue seq  │
│ Callback Set    │ Appointment scheduled    │ Confirm call  │
│ Qualified       │ Meets criteria           │ Attorney call │
│ Consultation    │ Attorney reviewing       │ Decision      │
│ Retainer Sent   │ Agreement sent           │ Track signing │
│ Signed          │ Retainer executed        │ Onboarding    │
│ Declined        │ Firm declined case       │ Decline letter│
│ Lost            │ Client chose other firm  │ Archive       │
│ Unresponsive    │ No response to outreach  │ Nurture/close │
│ Not Qualified   │ Doesn't meet criteria    │ Referral/close│
└─────────────────┴──────────────────────────┴───────────────┘
```

---

## 3. Nurture Campaigns for Non-Ready Leads

### 3.1 Nurture Campaign Strategy

```
NURTURE CAMPAIGN CATEGORIES:

1. NOT READY YET (Timing Issue)
   - Still deciding
   - Waiting for medical treatment to complete
   - Dealing with other priorities
   - Timeline: 30-90 day nurture

2. LOST TO COMPETITOR (Win-Back)
   - Signed with another firm
   - May become unhappy
   - Timeline: 6-12 month periodic touch

3. UNRESPONSIVE (Re-Engagement)
   - Never reached
   - Initial interest but ghosted
   - Timeline: 30-60 day reactivation

4. NOT QUALIFIED NOW (Future Potential)
   - Case too early (treatment ongoing)
   - Insufficient damages currently
   - May refer others
   - Timeline: Ongoing relationship building
```

### 3.2 Nurture Email Sequences

```
"NOT READY YET" NURTURE SEQUENCE:
(Bi-weekly emails for 90 days)

Week 2: Educational Content
Subject: "5 Things Insurance Companies Don't Want You to Know"
Content: Educational article about insurance tactics

Week 4: FAQ Content
Subject: "Your Questions Answered: Personal Injury FAQs"
Content: Common questions and answers

Week 6: Case Study
Subject: "Client Spotlight: [First Name]'s Recovery Story"
Content: Anonymized success story similar to their case

Week 8: Checklist Resource
Subject: "Free Download: Accident Documentation Checklist"
Content: Valuable resource with soft CTA

Week 10: Deadline Reminder
Subject: "Time-Sensitive: Understanding Filing Deadlines"
Content: Statute of limitations information

Week 12: Final Check-In
Subject: "Still Thinking About Your Case? Let's Talk"
Content: Personal note offering to reconnect

─────────────────────────────────────────

"WIN-BACK" SEQUENCE:
(Monthly emails for 12 months)

Month 1: No contact (respect their decision)

Month 2: Value-Add
Subject: "Resource for Your Case: Medical Records Organizer"
Content: Helpful tool regardless of who represents them

Month 3: Skip

Month 4: Check-In
Subject: "How's Your Case Going?"
Content: Genuine inquiry, offer second opinion

Month 5-6: Skip

Month 7: Success Story
Subject: "Results We've Achieved This Year"
Content: Highlight wins without being pushy

Month 8-9: Skip

Month 10: Direct Offer
Subject: "Not Happy with Your Attorney? We Can Help"
Content: Explain how switching works, no pressure

Month 11: Skip

Month 12: Final Touch
Subject: "One Year Later - We're Still Here"
Content: Anniversary of their inquiry, door always open
```

### 3.3 Nurture Campaign Performance Metrics

```
NURTURE CAMPAIGN KPIs:

Email Metrics:
□ Open rate (benchmark: 25-30%)
□ Click-through rate (benchmark: 3-5%)
□ Unsubscribe rate (benchmark: <0.5%)
□ Reply rate

Conversion Metrics:
□ Nurture to re-engaged rate
□ Re-engaged to qualified rate
□ Nurture to signed client rate
□ Time in nurture before conversion

Campaign Health:
□ List growth rate
□ List decay rate
□ Campaign ROI
□ Revenue attributed to nurture
```

---

## 4. Retainer Signing Process

### 4.1 Retainer Process Flow

```
RETAINER SIGNING WORKFLOW:

┌─────────────────┐
│ Case Qualified  │
│ by Attorney     │
└────────┬────────┘
         │
         ▼
┌─────────────────┐     ┌──────────────────────────┐
│ Retainer Call   │────►│ Explain Agreement Terms  │
│ Scheduled       │     │ Answer Questions         │
└─────────────────┘     └────────────┬─────────────┘
                                     │
         ┌───────────────────────────┴───────────────┐
         │                                           │
         ▼                                           ▼
┌─────────────────┐                       ┌─────────────────┐
│ In-Person Sign  │                       │ Electronic Sign │
│ (Preferred)     │                       │ (If Remote)     │
└────────┬────────┘                       └────────┬────────┘
         │                                         │
         └───────────────────┬─────────────────────┘
                             │
                             ▼
                   ┌─────────────────┐
                   │ Welcome Package │
                   │ & Onboarding    │
                   └────────┬────────┘
                            │
                            ▼
                   ┌─────────────────┐
                   │ Case Assignment │
                   │ & First Steps   │
                   └─────────────────┘
```

### 4.2 Retainer Call Script

```
RETAINER SIGNING CALL SCRIPT:

INTRODUCTION:
"Hi [Name], this is [Your Name] from [Firm Name]. I'm calling
because [Attorney Name] has reviewed your case and we'd like
to move forward with representing you. Do you have a few
minutes to discuss the next steps?"

[Confirm they have time]

RECAP:
"Great. First, let me briefly recap what we understand about
your situation to make sure we have everything correct:

[Summarize: accident type, date, injuries, treatment status]

Is there anything you'd like to add or correct?"

REPRESENTATION EXPLANATION:
"Based on our review, we believe you have a strong case and
we'd like to represent you. Here's how our representation
works:

1. CONTINGENCY FEE
   We work on a contingency basis, which means you pay
   nothing upfront. Our fee is [X]% of any recovery we
   obtain for you. If we don't win, you don't owe us
   anything for our attorney fees.

2. CASE COSTS
   There are case-related expenses like medical records,
   court filing fees, and expert witnesses. We advance
   these costs during your case, and they're only reimbursed
   from your recovery at the end.

3. WHAT WE'LL DO
   - Investigate your accident thoroughly
   - Gather all evidence and documentation
   - Handle all communication with insurance companies
   - Negotiate for maximum compensation
   - File a lawsuit if necessary
   - Keep you informed every step of the way

4. YOUR RESPONSIBILITIES
   - Follow your doctor's treatment plan
   - Keep us informed of any changes
   - Attend appointments and depositions as needed
   - Be honest and thorough with information

Do you have any questions about how this works?"

[Answer questions]

SIGNING PROCESS:
"If you're ready to move forward, I can send you the
representation agreement electronically. You'll receive:

1. The contingency fee agreement
2. HIPAA authorization (so we can obtain your medical records)
3. Lien authorization

You can review and sign these electronically, and I'll be
available to answer any questions. Alternatively, if you
prefer, you can come to our office to sign in person.

Which would work better for you?"

CLOSING:
"Excellent. I'll send those documents to [email address]
right now. Once you've signed, your case will be assigned
to [Case Manager Name], who will be your primary point
of contact. [He/She] will reach out within 24 hours to
introduce [himself/herself] and discuss next steps.

Thank you for trusting [Firm Name] with your case. We're
committed to fighting for the compensation you deserve.
Is there anything else I can help you with right now?"
```

### 4.3 Electronic Signature Protocol

```
E-SIGNATURE PROCESS:

1. DOCUMENT PREPARATION
   □ Fee agreement customized with client info
   □ Fee percentage confirmed
   □ Jurisdiction-specific language included
   □ HIPAA authorization attached
   □ Any additional authorizations needed

2. SENDING PROCESS
   □ Use approved e-signature platform (DocuSign, HelloSign, etc.)
   □ Include cover message explaining documents
   □ Set appropriate expiration (72 hours recommended)
   □ Enable reminders (24 hours, 48 hours)
   □ Copy case manager on completion notification

3. COVER MESSAGE TEMPLATE:
   "Dear [Name],

   Thank you for choosing [Firm Name] to represent you.

   Please find attached the following documents for your
   signature:

   1. Contingency Fee Agreement - This outlines our
      representation terms
   2. HIPAA Authorization - Allows us to obtain your
      medical records
   3. [Additional documents as applicable]

   To sign:
   • Click the link below
   • Review each document carefully
   • Click the signature fields to sign
   • You'll receive a copy once complete

   If you have any questions, please call me at [number].

   Sincerely,
   [Your Name]"

4. FOLLOW-UP PROTOCOL:
   □ If not signed within 24 hours: Phone call
   □ If not signed within 48 hours: Phone + text
   □ If not signed within 72 hours: Escalate to attorney

5. POST-SIGNATURE:
   □ Confirm receipt of signed documents
   □ Send welcome email with case manager introduction
   □ Create client file in case management system
   □ Initiate medical records requests
   □ Schedule intake questionnaire completion
```

### 4.4 Retainer Signing KPIs

```
RETAINER CONVERSION METRICS:

Time-Based Metrics:
□ Time from qualification to retainer sent
   Target: < 2 hours
□ Time from retainer sent to signed
   Target: < 48 hours
□ Total time from first contact to signed
   Target: < 5 days (for standard cases)

Conversion Metrics:
□ Retainer sent to signed rate
   Target: > 75%
□ Qualified lead to signed rate
   Target: > 60%
□ First contact to signed rate
   Target: > 35%

Quality Metrics:
□ Signed cases that don't meet criteria
   Target: < 5%
□ Client cancellation within 10 days
   Target: < 3%
□ Client satisfaction at signing
   Target: > 4.5/5
```

---

# Technology Stack

## 1. CRM Recommendations

### 1.1 CRM Selection Criteria

```
ESSENTIAL CRM FEATURES FOR PI LAW FIRMS:

INTAKE-SPECIFIC:
□ Multi-channel lead capture (web, phone, chat, referral)
□ Automated lead distribution/routing
□ Lead scoring capabilities
□ Duplicate detection
□ Custom intake forms/questionnaires
□ Real-time lead alerts
□ Speed-to-lead tracking

COMMUNICATION:
□ Built-in phone system/VoIP integration
□ SMS/text messaging
□ Email integration
□ Call recording
□ Voicemail drop
□ Communication logging
□ Template management

AUTOMATION:
□ Workflow automation
□ Drip campaign management
□ Task automation
□ Reminder systems
□ Follow-up sequences
□ Status-based triggers

INTEGRATION:
□ Case management system integration
□ E-signature integration (DocuSign, etc.)
□ Calendar integration
□ Marketing platform integration
□ Accounting software integration
□ API availability

REPORTING:
□ Real-time dashboards
□ Custom report builder
□ Lead source attribution
□ Conversion funnel tracking
□ Staff performance metrics
□ ROI calculations

COMPLIANCE:
□ TCPA compliance features
□ Call recording consent
□ Data security/encryption
□ Audit trails
□ Role-based access
```

### 1.2 Recommended CRM Platforms

```
TIER 1: LEGAL-SPECIFIC CRMs

1. LITIFY
   Best for: Large firms wanting Salesforce power with legal customization
   Strengths:
   - Built on Salesforce platform
   - Deep legal workflow automation
   - Excellent matter management
   - Strong reporting
   Cost: $$$$$ (Enterprise pricing)

2. LEAD DOCKET
   Best for: PI firms focused on intake optimization
   Strengths:
   - Purpose-built for PI intake
   - Strong phone/SMS integration
   - Automated follow-up sequences
   - Real-time dashboards
   Cost: $$$ (Mid-market)

3. FILEVINE
   Best for: Firms wanting combined CRM + case management
   Strengths:
   - Full matter lifecycle
   - Excellent automation
   - Good mobile experience
   - Strong reporting
   Cost: $$$-$$$$ (Scalable pricing)

4. LAWMATICS
   Best for: Smaller firms wanting automation + marketing
   Strengths:
   - User-friendly interface
   - Marketing automation built-in
   - E-signature included
   - Good value
   Cost: $$ (SMB pricing)

TIER 2: GENERAL CRMs WITH LEGAL CUSTOMIZATION

5. SALESFORCE + LEGAL ADD-ONS
   Best for: Large firms with IT resources
   Strengths:
   - Highly customizable
   - Extensive integrations
   - Scalable
   Cost: $$$$-$$$$$ (Varies widely)

6. HUBSPOT + LEGAL CUSTOMIZATION
   Best for: Marketing-focused firms
   Strengths:
   - Excellent marketing automation
   - Free tier available
   - Good for content marketing
   Cost: $-$$$$ (Tiered pricing)
```

### 1.3 CRM Implementation Roadmap

```
CRM IMPLEMENTATION PHASES:

PHASE 1: FOUNDATION (Weeks 1-4)
─────────────────────────────────────────
□ System configuration
□ User setup and permissions
□ Basic workflow setup
□ Data migration planning
□ Integration setup (phone, email)
□ Initial staff training

PHASE 2: INTAKE SETUP (Weeks 5-8)
─────────────────────────────────────────
□ Lead capture forms
□ Lead routing rules
□ Intake questionnaires
□ Status/stage configuration
□ Basic automation (alerts, tasks)
□ Follow-up sequences

PHASE 3: AUTOMATION (Weeks 9-12)
─────────────────────────────────────────
□ Advanced workflows
□ Drip campaigns
□ Reporting dashboards
□ Integration refinement
□ Staff advanced training
□ Process optimization

PHASE 4: OPTIMIZATION (Ongoing)
─────────────────────────────────────────
□ Performance monitoring
□ A/B testing
□ Continuous improvement
□ Advanced reporting
□ New feature adoption
□ Regular training updates
```

---

## 2. Call Tracking Setup

### 2.1 Call Tracking Architecture

```
CALL TRACKING SYSTEM ARCHITECTURE:

┌─────────────────────────────────────────────────────────────┐
│                    TRACKING NUMBERS                         │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────┐       │
│  │ Google  │  │  TV     │  │ Radio   │  │ Direct  │       │
│  │  Ads    │  │  Ads    │  │  Ads    │  │  Mail   │       │
│  └────┬────┘  └────┬────┘  └────┬────┘  └────┬────┘       │
│       │            │            │            │              │
│       └────────────┴─────┬──────┴────────────┘              │
│                          │                                  │
│                          ▼                                  │
│            ┌──────────────────────────┐                    │
│            │  CALL TRACKING PLATFORM  │                    │
│            │  (CallRail, CallTrackingMetrics, etc.)        │
│            └────────────┬─────────────┘                    │
│                         │                                  │
│       ┌─────────────────┼─────────────────┐               │
│       │                 │                 │               │
│       ▼                 ▼                 ▼               │
│  ┌─────────┐      ┌─────────┐      ┌─────────┐          │
│  │ Call    │      │  CRM    │      │Analytics│          │
│  │Recording│      │ Push    │      │Reporting│          │
│  └─────────┘      └─────────┘      └─────────┘          │
└─────────────────────────────────────────────────────────────┘
```

### 2.2 Tracking Number Strategy

```
TRACKING NUMBER ALLOCATION:

BY MARKETING CHANNEL:
□ Google Ads (PPC) - Dynamic number insertion
□ Google Organic (SEO) - Pool of website numbers
□ Bing Ads - Dedicated tracking number
□ Facebook/Meta Ads - Dedicated tracking number
□ TV Advertising - Dedicated number per station/daypart
□ Radio Advertising - Dedicated number per station
□ Billboards - Dedicated number per location
□ Direct Mail - Dedicated number per campaign
□ Referral Program - Dedicated tracking number
□ Main Office Line - Non-tracked main number

BY WEBSITE BEHAVIOR:
□ Homepage visitors - Number pool rotation
□ Service page visitors - Page-specific numbers
□ Blog visitors - Content-specific numbers
□ Repeat visitors - Session-based tracking

NAMING CONVENTION:
[Channel]_[Campaign]_[Date]_[Variant]
Example: Google_AutoAccident_202501_A
```

### 2.3 Call Tracking Platform Configuration

```
CALL TRACKING SETUP CHECKLIST:

BASIC SETUP:
□ Create account and verify domain
□ Purchase/port tracking numbers
□ Configure routing to main intake line
□ Set business hours and after-hours routing
□ Enable call recording (with consent IVR)
□ Set up whisper messages for staff
□ Configure voicemail

WEBSITE INTEGRATION:
□ Install tracking script on all pages
□ Configure dynamic number insertion
□ Set up number pool (minimum 4 numbers)
□ Define session timeout settings
□ Test cross-device tracking

CRM INTEGRATION:
□ Connect to CRM via API
□ Map call data fields
□ Configure lead creation triggers
□ Set up call disposition sync
□ Test end-to-end data flow

REPORTING SETUP:
□ Configure standard reports
□ Set up automated report delivery
□ Create custom dashboards
□ Enable keyword-level tracking
□ Set up conversion goals

QUALITY ASSURANCE:
□ Test all tracking numbers
□ Verify recordings functioning
□ Check CRM data accuracy
□ Validate attribution data
□ Document all configurations
```

### 2.4 Call Tracking Metrics

```
CALL TRACKING KPIs:

VOLUME METRICS:
□ Total calls by source
□ Calls by day/hour
□ Calls by geographic area
□ New vs. repeat callers
□ Answered vs. missed calls

QUALITY METRICS:
□ Average call duration
□ First-time caller percentage
□ Qualified call percentage
□ Conversion rate by source
□ Cost per call by source

ATTRIBUTION METRICS:
□ Calls by campaign
□ Calls by keyword (PPC)
□ Calls by landing page
□ Calls by ad creative
□ Multi-touch attribution data

OPERATIONAL METRICS:
□ Answer rate
□ Ring time before answer
□ Hold time
□ Transfer rate
□ Abandonment rate
```

---

## 3. Attribution Modeling

### 3.1 Attribution Model Types

```
ATTRIBUTION MODELS FOR PI FIRMS:

1. FIRST-TOUCH ATTRIBUTION
   Definition: 100% credit to first interaction
   Use case: Understanding awareness drivers
   Example: Client first saw TV ad → signs
            TV gets 100% credit

2. LAST-TOUCH ATTRIBUTION
   Definition: 100% credit to final interaction
   Use case: Understanding conversion drivers
   Example: Client searched Google → signs
            Google gets 100% credit

3. LINEAR ATTRIBUTION
   Definition: Equal credit to all touchpoints
   Use case: Balanced view of full journey
   Example: TV → Radio → Google → signs
            Each gets 33% credit

4. TIME-DECAY ATTRIBUTION
   Definition: More credit to recent touchpoints
   Use case: Emphasizing conversion path
   Example: TV (10%) → Radio (20%) → Google (70%)

5. POSITION-BASED (U-SHAPED)
   Definition: 40% first, 40% last, 20% middle
   Use case: Valuing awareness + conversion
   Example: TV (40%) → Radio (10%) → Referral (10%) → Google (40%)

RECOMMENDED FOR PI FIRMS:
Primary: Position-Based (U-Shaped)
Secondary: First-Touch (for media buying)
Tertiary: Last-Touch (for digital optimization)
```

### 3.2 Attribution Implementation

```
ATTRIBUTION TRACKING SETUP:

DATA COLLECTION REQUIREMENTS:
□ All digital touchpoints tracked (UTM parameters)
□ All calls tracked with source
□ All forms tagged with source
□ Offline touchpoints captured (asked at intake)
□ Timeline of all interactions logged

UTM PARAMETER STANDARD:
utm_source = Platform (google, facebook, tv, radio)
utm_medium = Channel type (cpc, organic, broadcast, print)
utm_campaign = Campaign name (auto_accident_jan2026)
utm_content = Ad/creative identifier (ad_v2)
utm_term = Keyword (car accident lawyer)

INTAKE SOURCE CAPTURE:
"How did you hear about us?"
□ TV Commercial
□ Radio Ad
□ Billboard
□ Google Search
□ Friend/Family Referral
□ Previous Client
□ Attorney Referral
□ Social Media
□ Other: ________

DATA INTEGRATION FLOW:
Marketing Platforms → CRM → Attribution Platform → Reporting
```

### 3.3 Attribution Dashboard Metrics

```
ATTRIBUTION REPORTING FRAMEWORK:

CHANNEL PERFORMANCE:
┌──────────────────────────────────────────────────────────┐
│ Channel     │ Leads │ Cases │ Revenue │ Cost  │ ROI     │
├─────────────┼───────┼───────┼─────────┼───────┼─────────┤
│ Google Ads  │  150  │   25  │  $500K  │ $50K  │ 10.0x   │
│ TV          │   80  │   15  │  $450K  │ $75K  │  6.0x   │
│ SEO         │  100  │   18  │  $360K  │ $20K  │ 18.0x   │
│ Referral    │   50  │   20  │  $600K  │  $5K  │ 120.0x  │
│ Radio       │   40  │    6  │  $120K  │ $30K  │  4.0x   │
└─────────────┴───────┴───────┴─────────┴───────┴─────────┘

ATTRIBUTION-ADJUSTED PERFORMANCE:
(Using position-based model)
┌──────────────────────────────────────────────────────────┐
│ Channel     │ First │ Assist │ Last  │ Total  │ Adj ROI│
├─────────────┼───────┼────────┼───────┼────────┼────────┤
│ Google Ads  │  15%  │  20%   │  45%  │  28%   │ 8.5x   │
│ TV          │  40%  │  15%   │  10%  │  22%   │ 7.8x   │
│ SEO         │  20%  │  25%   │  15%  │  20%   │ 15.0x  │
│ Referral    │  10%  │  10%   │  25%  │  18%   │ 98.0x  │
│ Radio       │  15%  │  30%   │   5%  │  12%   │  5.5x  │
└─────────────┴───────┴────────┴───────┴────────┴────────┘

MULTI-TOUCH PATH ANALYSIS:
Common conversion paths:
1. TV → Google Brand Search → Website → Call (22%)
2. Google Non-Brand → Website → Retargeting → Call (18%)
3. Referral → Website → Call (15%)
4. Radio → Google Brand Search → Website → Form (12%)
5. SEO → Website → Form (10%)
```

---

## 4. Reporting Dashboards

### 4.1 Executive Dashboard

```
EXECUTIVE DASHBOARD - DAILY VIEW

┌─────────────────────────────────────────────────────────────┐
│                    DAILY INTAKE SUMMARY                     │
│                    [Date: January 24, 2026]                 │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  NEW LEADS TODAY          CASES SIGNED TODAY               │
│  ┌─────────────┐          ┌─────────────┐                  │
│  │     47      │          │      8      │                  │
│  │   ▲ 12%     │          │   ▲ 33%     │                  │
│  │  vs. avg    │          │  vs. avg    │                  │
│  └─────────────┘          └─────────────┘                  │
│                                                             │
│  CONVERSION RATE          AVG RESPONSE TIME                │
│  ┌─────────────┐          ┌─────────────┐                  │
│  │    38%      │          │   4.2 min   │                  │
│  │   ▲ 5%      │          │   ▼ 15%     │                  │
│  │  vs. avg    │          │  vs. target │                  │
│  └─────────────┘          └─────────────┘                  │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                    LEAD SOURCE BREAKDOWN                    │
│                                                             │
│  Google Ads    ████████████████░░░░  35% (16)              │
│  SEO           ██████████░░░░░░░░░░  22% (10)              │
│  TV            ████████░░░░░░░░░░░░  17% (8)               │
│  Referral      ██████░░░░░░░░░░░░░░  13% (6)               │
│  Other         █████░░░░░░░░░░░░░░░  13% (7)               │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                    PIPELINE STATUS                          │
│                                                             │
│  New/Attempting    ████████████░░░░░░░░  42 leads          │
│  Qualified         █████████░░░░░░░░░░░  28 leads          │
│  Consultation      █████░░░░░░░░░░░░░░░  15 leads          │
│  Retainer Sent     ███░░░░░░░░░░░░░░░░░   9 leads          │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                    MTD PERFORMANCE                          │
│                                                             │
│  Leads: 892    Cases: 156    Est. Value: $4.2M             │
│  Target: 1,000  Target: 175   Target: $5.0M                │
│  Progress: 89%  Progress: 89% Progress: 84%                │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 4.2 Intake Manager Dashboard

```
INTAKE MANAGER DASHBOARD - OPERATIONAL VIEW

┌─────────────────────────────────────────────────────────────┐
│                   REAL-TIME QUEUE STATUS                    │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  LEADS AWAITING FIRST CONTACT: 3                           │
│  ┌────────────────────────────────────────────────────┐    │
│  │ John S. (Car Accident) - 4 min - Web Form          │    │
│  │ Maria G. (Truck Accident) - 2 min - Phone VM ⚠️    │    │
│  │ Robert T. (Slip & Fall) - 1 min - Chat             │    │
│  └────────────────────────────────────────────────────┘    │
│                                                             │
│  STAFF AVAILABILITY:                                       │
│  ┌─────────────┬──────────┬─────────────┬─────────────┐   │
│  │ Specialist  │ Status   │ Current     │ Today       │   │
│  ├─────────────┼──────────┼─────────────┼─────────────┤   │
│  │ Sarah M.    │ On Call  │ -           │ 12 leads    │   │
│  │ James K.    │ On Call  │ John S.     │ 15 leads    │   │
│  │ Lisa P.     │ Busy     │ Maria G.    │ 11 leads    │   │
│  │ Michael R.  │ Break    │ -           │ 9 leads     │   │
│  └─────────────┴──────────┴─────────────┴─────────────┘   │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                   FOLLOW-UP QUEUE                           │
│                                                             │
│  OVERDUE (Action Required):         12 leads               │
│  DUE TODAY:                         34 leads               │
│  SCHEDULED THIS WEEK:               89 leads               │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                   TODAY'S METRICS                           │
│                                                             │
│  Calls Answered:      127 │ Avg Handle Time:    8.5 min   │
│  Calls Missed:          4 │ First Call Res:       62%     │
│  Answer Rate:        97%  │ Callback Completed:   89%     │
│  Avg Wait Time:     12 sec│ Quality Score:        87      │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                   ALERTS & NOTIFICATIONS                    │
│                                                             │
│  ⚠️ HIGH PRIORITY: Truck accident lead - Maria G.          │
│     Severe injury reported - escalate to attorney          │
│                                                             │
│  ⚠️ SOL WARNING: 3 leads approaching statute deadline      │
│     Review list and take action                            │
│                                                             │
│  ℹ️ Callback reminder: 5 scheduled callbacks in next hour  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 4.3 Marketing Dashboard

```
MARKETING PERFORMANCE DASHBOARD

┌─────────────────────────────────────────────────────────────┐
│                   CHANNEL PERFORMANCE - MTD                 │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ┌───────────┬────────┬────────┬─────────┬────────┬──────┐│
│  │ Channel   │ Spend  │ Leads  │ CPL     │ Cases  │ CPA  ││
│  ├───────────┼────────┼────────┼─────────┼────────┼──────┤│
│  │ Google    │ $45K   │ 320    │ $141    │ 52     │ $865 ││
│  │ TV        │ $65K   │ 180    │ $361    │ 28     │$2,321││
│  │ Radio     │ $25K   │ 85     │ $294    │ 12     │$2,083││
│  │ SEO       │ $15K   │ 210    │ $71     │ 38     │ $395 ││
│  │ Facebook  │ $12K   │ 95     │ $126    │ 14     │ $857 ││
│  │ Referral  │ $3K    │ 102    │ $29     │ 42     │ $71  ││
│  └───────────┴────────┴────────┴─────────┴────────┴──────┘│
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                   CONVERSION FUNNEL                         │
│                                                             │
│  Impressions    ████████████████████████████  2.4M         │
│       │                                                     │
│       ▼         12% CTR                                    │
│  Clicks         ████████████████████████     288K          │
│       │                                                     │
│       ▼         0.35% CVR                                  │
│  Leads          ██████████████               992           │
│       │                                                     │
│       ▼         68% Qualification Rate                     │
│  Qualified      █████████████                675           │
│       │                                                     │
│       ▼         28% Close Rate                             │
│  Signed         █████                        186           │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                   LEAD QUALITY TRENDS                       │
│                                                             │
│  Quality Score by Week:                                    │
│                                                             │
│  Week 1  ████████████████░░░░  76%                        │
│  Week 2  █████████████████░░░  82%                        │
│  Week 3  ██████████████████░░  85%                        │
│  Week 4  ███████████████████░  88%  (Current)             │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                   TOP PERFORMING CAMPAIGNS                  │
│                                                             │
│  1. Google - Auto Accident Exact Match    ROI: 12.5x      │
│  2. SEO - Car Accident Lawyer [City]      ROI: 18.2x      │
│  3. Facebook - Retargeting Campaign       ROI: 9.8x       │
│  4. Google - Truck Accident Campaign      ROI: 8.4x       │
│  5. TV - Evening News Spots               ROI: 6.2x       │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 4.4 Quality Assurance Dashboard

```
QUALITY ASSURANCE DASHBOARD

┌─────────────────────────────────────────────────────────────┐
│                   CALL QUALITY METRICS                      │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  OVERALL QUALITY SCORE:  87/100  (Target: 85)              │
│                                                             │
│  Score Components:                                         │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ Greeting & Professionalism  │ 92% │ ██████████████░│   │
│  │ Empathy & Rapport           │ 88% │ █████████████░░│   │
│  │ Information Gathering       │ 85% │ ████████████░░░│   │
│  │ Qualification Accuracy      │ 82% │ ███████████░░░░│   │
│  │ Closing & Next Steps        │ 89% │ █████████████░░│   │
│  │ Compliance                  │ 95% │ ███████████████│   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                   SPECIALIST PERFORMANCE                    │
│                                                             │
│  ┌───────────┬───────┬────────┬─────────┬────────────────┐ │
│  │ Name      │ Score │ Calls  │ Convert │ Areas to Coach │ │
│  ├───────────┼───────┼────────┼─────────┼────────────────┤ │
│  │ Sarah M.  │ 94    │ 285    │ 42%     │ None           │ │
│  │ James K.  │ 89    │ 312    │ 38%     │ Closing        │ │
│  │ Lisa P.   │ 85    │ 268    │ 35%     │ Qualification  │ │
│  │ Michael R.│ 78    │ 245    │ 31%     │ Empathy        │ │
│  │ Team Avg  │ 87    │ 277    │ 37%     │                │ │
│  └───────────┴───────┴────────┴─────────┴────────────────┘ │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                   RECENT CALL REVIEWS                       │
│                                                             │
│  ⭐⭐⭐⭐⭐ Sarah M. - 1/24 2:15 PM - Auto Accident        │
│  Excellent rapport, thorough qualification, perfect close   │
│                                                             │
│  ⭐⭐⭐⭐☆ James K. - 1/24 11:30 AM - Slip & Fall         │
│  Good info gathering, could improve urgency in closing      │
│                                                             │
│  ⭐⭐⭐☆☆ Michael R. - 1/24 10:45 AM - Truck Accident    │
│  Missed empathy opportunities, rushing caller               │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                   COMPLIANCE ALERTS                         │
│                                                             │
│  ✓ All calls recorded with consent - 100%                  │
│  ✓ No TCPA violations detected                             │
│  ✓ Currently represented screening - 100% compliance       │
│  ⚠️ 2 calls missing disposition - Follow up required       │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

# Appendices

## Appendix A: Intake Specialist Training Curriculum

```
INTAKE SPECIALIST TRAINING PROGRAM

WEEK 1: FOUNDATIONS
─────────────────────────────────────────
Day 1-2: Company & Legal Basics
□ Firm history, values, and mission
□ Personal injury law fundamentals
□ Types of cases we handle
□ Ethical obligations and boundaries
□ Confidentiality requirements

Day 3-4: Systems Training
□ CRM overview and navigation
□ Phone system operation
□ Call recording and compliance
□ Data entry standards
□ Documentation requirements

Day 5: Shadowing
□ Listen to live calls (minimum 20)
□ Review recorded calls (10 examples)
□ Observe intake process end-to-end

WEEK 2: SKILLS DEVELOPMENT
─────────────────────────────────────────
Day 1-2: Communication Skills
□ Active listening techniques
□ Empathy and rapport building
□ Handling emotional callers
□ Difficult conversation management
□ Professional phone etiquette

Day 3-4: Script Mastery
□ Opening scripts (memorization)
□ Qualification questions
□ Objection handling
□ Closing techniques
□ Role-play exercises (20+ scenarios)

Day 5: Case Type Training
□ Auto accident specifics
□ Truck accident specifics
□ Premises liability specifics
□ Medical malpractice basics
□ Workplace injury basics

WEEK 3: QUALIFICATION & CONVERSION
─────────────────────────────────────────
Day 1-2: Lead Qualification
□ Screening criteria by case type
□ Red flag identification
□ Value assessment
□ Statute of limitations awareness
□ When to escalate

Day 3-4: Conversion Techniques
□ Building urgency appropriately
□ Overcoming hesitation
□ Setting expectations
□ Retainer process explanation
□ Follow-up strategy

Day 5: Assessment & Feedback
□ Written knowledge test
□ Role-play evaluation
□ Call simulation scoring
□ Feedback and coaching plan

WEEK 4: SUPERVISED PRACTICE
─────────────────────────────────────────
Day 1-3: Supervised Calls
□ Take calls with supervisor monitoring
□ Real-time feedback and coaching
□ Gradually increase independence
□ Quality review of all calls

Day 4-5: Independent with Review
□ Handle calls independently
□ All calls reviewed within 24 hours
□ Daily coaching sessions
□ Readiness assessment

ONGOING: CONTINUOUS DEVELOPMENT
─────────────────────────────────────────
□ Weekly call reviews (minimum 5)
□ Monthly skills assessment
□ Quarterly refresher training
□ New case type training as needed
□ Advanced certification program
```

## Appendix B: Quality Assurance Rubric

```
CALL QUALITY EVALUATION FORM

Intake Specialist: _____________  Date: ____________
Evaluator: ___________________  Call ID: __________
Call Type: ___________________  Duration: _________

SCORING KEY:
5 = Exceptional  4 = Good  3 = Satisfactory  2 = Needs Improvement  1 = Unsatisfactory

┌─────────────────────────────────────────────────────────────┐
│ CATEGORY 1: OPENING (15 points)                             │
├─────────────────────────────────────────────────────────────┤
│ □ Answered within 2 rings                        /3        │
│ □ Proper greeting with name and firm             /4        │
│ □ Warm, professional tone                        /4        │
│ □ Asked open-ended opening question              /4        │
│                                    Subtotal:     /15       │
├─────────────────────────────────────────────────────────────┤
│ CATEGORY 2: EMPATHY & RAPPORT (20 points)                   │
├─────────────────────────────────────────────────────────────┤
│ □ Acknowledged caller's situation                /5        │
│ □ Used appropriate empathy statements            /5        │
│ □ Maintained calm, supportive demeanor           /5        │
│ □ Let caller speak without interrupting          /5        │
│                                    Subtotal:     /20       │
├─────────────────────────────────────────────────────────────┤
│ CATEGORY 3: INFORMATION GATHERING (25 points)               │
├─────────────────────────────────────────────────────────────┤
│ □ Gathered incident details                      /5        │
│ □ Gathered injury information                    /5        │
│ □ Gathered medical treatment status              /5        │
│ □ Gathered insurance information                 /5        │
│ □ Gathered contact information                   /5        │
│                                    Subtotal:     /25       │
├─────────────────────────────────────────────────────────────┤
│ CATEGORY 4: QUALIFICATION (20 points)                       │
├─────────────────────────────────────────────────────────────┤
│ □ Assessed liability factors                     /5        │
│ □ Identified red flags appropriately             /5        │
│ □ Checked for current representation             /5        │
│ □ Made appropriate qualification decision        /5        │
│                                    Subtotal:     /20       │
├─────────────────────────────────────────────────────────────┤
│ CATEGORY 5: CLOSING (15 points)                             │
├─────────────────────────────────────────────────────────────┤
│ □ Set clear expectations for next steps          /5        │
│ □ Confirmed contact information                  /3        │
│ □ Offered to answer additional questions         /4        │
│ □ Ended professionally                           /3        │
│                                    Subtotal:     /15       │
├─────────────────────────────────────────────────────────────┤
│ CATEGORY 6: COMPLIANCE (5 points)                           │
├─────────────────────────────────────────────────────────────┤
│ □ No unauthorized legal advice given             /2        │
│ □ Recording consent obtained                     /2        │
│ □ Proper data entry completed                    /1        │
│                                    Subtotal:     /5        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│                              TOTAL SCORE:        /100      │
│                                                             │
│ OVERALL RATING:                                             │
│ □ Exceeds Standards (90-100)                               │
│ □ Meets Standards (80-89)                                  │
│ □ Needs Improvement (70-79)                                │
│ □ Does Not Meet Standards (<70)                            │
│                                                             │
└─────────────────────────────────────────────────────────────┘

EVALUATOR COMMENTS:
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________

COACHING RECOMMENDATIONS:
_____________________________________________________________
_____________________________________________________________
_____________________________________________________________

Evaluator Signature: ________________  Date: _________________
```

## Appendix C: Statute of Limitations Quick Reference

```
STATUTE OF LIMITATIONS BY STATE - PERSONAL INJURY

┌────────────────┬────────────────┬──────────────────────────┐
│ STATE          │ PERSONAL INJURY│ SPECIAL NOTES            │
├────────────────┼────────────────┼──────────────────────────┤
│ Alabama        │ 2 years        │                          │
│ Alaska         │ 2 years        │                          │
│ Arizona        │ 2 years        │                          │
│ Arkansas       │ 3 years        │                          │
│ California     │ 2 years        │ 6 mo discovery for med mal│
│ Colorado       │ 2 years        │ 3 years for auto         │
│ Connecticut    │ 2 years        │                          │
│ Delaware       │ 2 years        │                          │
│ Florida        │ 4 years        │ 2 years for med mal      │
│ Georgia        │ 2 years        │                          │
│ Hawaii         │ 2 years        │                          │
│ Idaho          │ 2 years        │                          │
│ Illinois       │ 2 years        │                          │
│ Indiana        │ 2 years        │                          │
│ Iowa           │ 2 years        │                          │
│ Kansas         │ 2 years        │                          │
│ Kentucky       │ 1 year         │ 2 years for auto         │
│ Louisiana      │ 1 year         │                          │
│ Maine          │ 6 years        │                          │
│ Maryland       │ 3 years        │                          │
│ Massachusetts  │ 3 years        │                          │
│ Michigan       │ 3 years        │                          │
│ Minnesota      │ 2 years        │                          │
│ Mississippi    │ 3 years        │                          │
│ Missouri       │ 5 years        │                          │
│ Montana        │ 3 years        │                          │
│ Nebraska       │ 4 years        │                          │
│ Nevada         │ 2 years        │                          │
│ New Hampshire  │ 3 years        │                          │
│ New Jersey     │ 2 years        │                          │
│ New Mexico     │ 3 years        │                          │
│ New York       │ 3 years        │                          │
│ North Carolina │ 3 years        │                          │
│ North Dakota   │ 6 years        │                          │
│ Ohio           │ 2 years        │                          │
│ Oklahoma       │ 2 years        │                          │
│ Oregon         │ 2 years        │                          │
│ Pennsylvania   │ 2 years        │                          │
│ Rhode Island   │ 3 years        │                          │
│ South Carolina │ 3 years        │                          │
│ South Dakota   │ 3 years        │                          │
│ Tennessee      │ 1 year         │                          │
│ Texas          │ 2 years        │                          │
│ Utah           │ 4 years        │                          │
│ Vermont        │ 3 years        │                          │
│ Virginia       │ 2 years        │                          │
│ Washington     │ 3 years        │                          │
│ West Virginia  │ 2 years        │                          │
│ Wisconsin      │ 3 years        │                          │
│ Wyoming        │ 4 years        │                          │
│ Washington DC  │ 3 years        │                          │
└────────────────┴────────────────┴──────────────────────────┘

IMPORTANT NOTES:
- These are general guidelines; specific circumstances may apply
- Medical malpractice often has different/shorter limits
- Discovery rules may extend deadlines in some cases
- Government claims often require earlier notice
- Always verify current statutes with attorney
- When in doubt, treat as URGENT

ESCALATION PROTOCOL FOR SOL CONCERNS:
□ Less than 6 months remaining → Immediate attorney review
□ Less than 3 months remaining → URGENT - same day review
□ Less than 1 month remaining → CRITICAL - immediate action
```

## Appendix D: Decline Letter Templates

```
DECLINE LETTER - TEMPLATE A
(Standard Decline - Case Not Viable)

[Date]

[Client Name]
[Address]
[City, State ZIP]

Re: Your Inquiry Regarding [Incident Type] on [Date]

Dear [Client Name],

Thank you for contacting [Firm Name] regarding your [incident
type] that occurred on [date]. We appreciate the opportunity
to review your matter and understand how difficult this time
must be for you.

After careful consideration, we have determined that our firm
is not able to take on representation of your case at this
time. Please understand that this decision is not a judgment
about the validity of your claim, but rather reflects our
assessment of various factors including our current caseload
and areas of specialization.

IMPORTANT: This letter does not constitute legal advice, and
you should not rely on this letter for any legal purpose. There
may be time limits (statutes of limitations) that apply to your
potential claim. We strongly encourage you to consult with
another attorney promptly to ensure your rights are protected.

RESOURCES:
• [State] Bar Association Lawyer Referral: [Phone Number]
• American Bar Association: www.findlegalhelp.org

We wish you the best in resolving this matter and in your
recovery.

Sincerely,

[Attorney Name]
[Firm Name]

---

DECLINE LETTER - TEMPLATE B
(Statute of Limitations Concern)

[Date]

[Client Name]
[Address]
[City, State ZIP]

Re: Your Inquiry Regarding [Incident Type] on [Date]

Dear [Client Name],

Thank you for contacting [Firm Name] regarding your [incident
type]. We have reviewed the information you provided.

We are writing to inform you that we are unable to accept
representation in this matter. Additionally, we want to make
you aware of an important time consideration:

URGENT NOTICE: Based on the date of your incident ([date])
and the applicable laws in [State], the time limit for filing
a claim may be [approaching/have passed]. The statute of
limitations for [case type] claims in [State] is generally
[X years] from the date of the incident.

We strongly urge you to contact another attorney IMMEDIATELY
to discuss your options. Do not delay, as missing this deadline
could permanently bar you from pursuing your claim.

For attorney referrals, contact:
• [State] Bar Association: [Phone Number]
• Local Bar Association: [Phone Number]

This letter does not constitute legal advice. We are providing
this notice as a courtesy and encourage you to seek independent
legal counsel without delay.

Sincerely,

[Attorney Name]
[Firm Name]

---

DECLINE LETTER - TEMPLATE C
(Outside Practice Area)

[Date]

[Client Name]
[Address]
[City, State ZIP]

Re: Your Inquiry Regarding [Matter Type]

Dear [Client Name],

Thank you for considering [Firm Name] for your legal needs.
We appreciate you taking the time to contact us about your
[matter type] matter.

After reviewing the information you provided, we have
determined that this matter falls outside our firm's primary
practice areas. Our firm focuses specifically on personal
injury matters including auto accidents, truck accidents,
premises liability, and similar cases.

For matters involving [their matter type], we recommend
contacting an attorney who specializes in that area of law.

SUGGESTED RESOURCES:
• [State] Bar Association Lawyer Referral: [Phone Number]
• [Specific practice area association if applicable]

We wish you the best in finding appropriate representation
for your matter.

Sincerely,

[Attorney Name]
[Firm Name]
```

---

## Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | January 2026 | [Author] | Initial release |

---

**CONFIDENTIALITY NOTICE:** This document contains proprietary
information belonging to [Firm Name]. Distribution outside the
organization is prohibited without written authorization.

---

*End of Document*
