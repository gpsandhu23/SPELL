# SPELL

## What is SPELL?

SPELL (Software Product Engineering Language Layout) is a specification for an abstraction layer that bridges the gap between human intent and AI-powered software development. It provides a structured way to describe software products in natural language, enabling AI coding tools like Cursor or GitHub Copilot to transform these descriptions into functional software.

The primary goal of SPELL is to capture sufficient detail in natural language that allows AI tools to quickly and accurately build software that matches the user's actual requirements. By providing a standardized way to express software specifications, SPELL aims to make the software development process more efficient and reduce the gap between what users want and what gets built.

## SPELL Parameters

The SPELL specification is designed to capture user intent through a set of carefully chosen parameters. Each parameter focuses on understanding what the end user needs from the software, rather than technical implementation details.

### Core Parameters (All Required)

#### 1. **Product Vision**
A clear, concise statement of what the software does and who it's for.
- Example: "A task management app for remote teams that prioritizes simplicity over features"

#### 2. **User Pain Points**
Understanding what problems users currently face helps AI tools build solutions that directly address real needs.
- What frustrations do users have with existing solutions?
- What manual processes are they trying to eliminate?
- Example: "Currently tracking tasks across 5 different tools, losing context when switching"

#### 3. **User Stories**
Concrete scenarios describing how users will interact with the software.
- Format: "As a [user type], I want to [action] so that [outcome]"
- Include at least 3-5 primary user stories

#### 4. **Core Features**
List of essential functionality, described from the user's perspective.
- Focus on what users can do, not how it's implemented
- Prioritize features (must-have vs nice-to-have)

#### 5. **Non-Goals**
Explicitly stating what the software should NOT do prevents over-engineering.
- Features to explicitly avoid
- Complexity boundaries
- Example: "NOT a full project management suite, NOT for enterprise deployment"

#### 6. **Success Metrics**
How users will measure if the software is working for them.
- User-focused metrics (e.g., "complete a task in under 2 minutes")
- Measurable outcomes from user perspective

### User Context (All Required)

#### 1. **Target Users**
Specific description of who will use this software.
- Demographics, technical skill level, context of use
- Primary vs secondary user groups

#### 2. **Usage Context**
Understanding when and where users will use the software.
- Primary usage environment (office, mobile, field work)
- Time constraints (quick sessions vs extended use)
- Device preferences
- Example: "Used primarily on mobile during commute, sessions under 2 minutes"

#### 3. **User Experience Flow**
Step-by-step description of the main user journey through the application.
- What does the user see first?
- How do they navigate between features?
- What are the key interaction points?
- Includes look & feel preferences (modern, minimalist, playful, professional, etc.)

### Interaction Design (All Required)

#### 1. **Key Interactions with Examples**
The primary ways users will interact with the software.
- Click, type, swipe, voice, etc.
- Most common actions users will perform
- Concrete examples of interaction patterns
- Example: "User opens app → sees today's entry prompt → types thoughts → auto-saves on pause"

#### 2. **Onboarding Experience**
Defining the initial user experience to ensure quick adoption.
- What should users experience in first 5 minutes?
- What's the minimum setup required?
- How do users learn the interface?
- Example: "Zero setup required, guided tour on first launch, can create first entry immediately"

#### 3. **Error Handling & Recovery**
How the software should behave when things go wrong.
- Common error scenarios
- Recovery paths
- User communication style
- Example: "Friendly error messages with clear next steps, auto-save to prevent data loss"

### Technical Context (Required where applicable)

#### 1. **Data & Privacy**
How user data is handled from the user's perspective.
- Where is data stored? (user's device, cloud, both)
- Who can access the data? (just me, my team, public)
- What happens to data if I stop using the app?
- Example: "All journal entries stored locally on device, with optional encrypted cloud backup"

#### 2. **User Access Model**
How users access and identify themselves in the software.
- No account needed (anonymous use)
- Individual accounts (personal use)
- Team/organization accounts (collaborative use)
- Example: "Email-based accounts with option for team workspaces"

#### 3. **Technical Constraints & Requirements**
Combined platform, connectivity, and performance requirements.
- Platform preferences (web, mobile, desktop)
- Connectivity needs (offline/online capabilities)
- Performance expectations
- Accessibility requirements
- Example: "Works offline, syncs automatically when connected, must be accessible via screen readers"

#### 4. **Multi-User Behavior** (Required if multi-user)
How multiple users interact within the software.
- Real-time collaboration needs
- Sharing and permission models
- Conflict resolution expectations
- Example: "Multiple users can edit simultaneously with live cursors like Google Docs"

#### 5. **Integration Needs** (Required if applicable)
External tools or services users expect to work with.
- Import/export requirements
- API connections users need
- Common workflow integrations
- Example: "Must integrate with Google Calendar and export to PDF"

#### 6. **Migration Path** (Required if applicable)
How users will transition from existing solutions.
- How to import existing data
- Transition from current tools
- Data export capabilities
- Example: "Import from Apple Notes, Google Keep, plain text files"

#### 7. **Scalability Expectations**
User expectations about how software will grow with their needs.
- Expected data volume over time
- Number of users/items to support
- Performance expectations as usage grows
- Example: "Should handle up to 10,000 journal entries without slowing down"

### Example Usage

```yaml
product_vision: "A daily journal app for mindfulness practitioners"
user_pain_points:
  - "Currently using paper journal, hard to track patterns over time"
  - "Existing apps are too complex with unnecessary features"
user_stories:
  - "As a busy professional, I want to quickly capture my thoughts in under 30 seconds"
  - "As a mindfulness practitioner, I want to see my mood patterns over time"
core_features:
  - Quick entry with minimal friction
  - Mood tracking with simple visual indicators
  - Weekly/monthly reflection summaries
non_goals:
  - "NOT a social media platform"
  - "NOT a full-featured note-taking app"
success_metrics:
  - "Complete a journal entry in under 30 seconds"
  - "Identify mood patterns within first week of use"
```

### Why These Matter

The key principle of SPELL is that every parameter should answer "What does the user need?" rather than "How should we build it?" This user-centric approach ensures that AI tools can make appropriate technical decisions while staying focused on delivering value to users.

By providing this structured way to express software requirements, SPELL helps bridge the gap between human intent and AI-powered development, leading to software that better matches user needs and expectations.
