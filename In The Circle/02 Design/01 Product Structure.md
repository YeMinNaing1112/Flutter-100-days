# Product Structure — In The Circle

> **Phase:** Design  
> **Status:** MVP screen inventory confirmed; screen-level details remain open.  
> **Product philosophy:** Connect → Support → Grow

## 1. Navigation model

The application will use a **bottom navigation bar** with three primary destinations:

1. **My Day** — the user's home screen.
2. **Partner** — a deeper view of the partner's daily activities and progress.
3. **Our Goals** — a dedicated space for goals and responsibilities shared by both partners.

There will be **no separate Emotional Security tab**. Emotional security should be supported within the My Day and Partner experiences.

## 1.1 Solo and connected experiences

- A person can use In The Circle on their own without needing a partner connection.
- Each account can have **only one active partner connection at a time**, reflecting the product's focus on committed, two-person relationships.
- **My Day remains fully usable in Solo Mode**, including personal routines, tasks, and individual progress. It does not show a partner-progress overview when the user is not connected.
- The three main tabs remain visible in both Solo Mode and Connected Mode.
- In Solo Mode, opening **Partner** or **Our Goals** takes the user to an in-page locked/connection state explaining that connecting with a partner unlocks that feature.
- Do not interrupt the solo experience with pop-ups, unsolicited prompts, or repeated connection reminders. The connection invitation appears only after the user intentionally opens a partner-dependent tab.
- After a partner connection is established, the Partner and Our Goals destinations become available, and the partner-progress overview can appear on My Day.
- The exact wording and visual design of the connection state remain to be designed.

## 1.2 Onboarding — account and profile first

- A new user should create an account and complete their profile before entering the main app experience.
- After Profile Setup, take the user directly to **My Day**; do not add a separate introductory walkthrough or tutorial to the MVP onboarding flow.
- MVP authentication methods: **email and password** or **Google sign-in**. Apple sign-in is not included in the initial MVP authentication scope.
- Use one shared **Welcome / Authentication screen** for both Sign Up and Sign In, allowing users to switch between the two flows rather than navigating to separate screens.
- For email-and-password sign-up, require the user to verify their email address before proceeding to Profile Setup. The first-time flow is **Welcome / Authentication → Email Verification → Profile Setup → My Day**.
- For Google sign-in, a separate email-verification step is not required; after authentication, a new user proceeds to Profile Setup.
- A returning user who signs in and already has a completed profile can go directly to My Day.
- Keep initial Profile Setup minimal: **display name is required**, while **profile photo and short introduction are optional**.
- Partner connection is not required during onboarding; users can enter and use the app in Solo Mode.

## 1.3 Partner connection — MVP invitation method

- The first version will use a **private, shareable invitation link** generated for the intended partner. The link carries the invitation code/token, so the recipient does not need to type it manually.
- The inviter can share the link through external messaging apps such as Telegram or Messenger.
- When the recipient taps the link, In The Circle should open directly to the inviter's normal profile, where the recipient can review the profile and explicitly accept or decline the connection.
- Each invitation is **single-use**: only one account can successfully accept it. Once an invitee accepts and the connection is established, that invitation expires and cannot be used by anyone else.
- Simply opening or viewing the invitation should not consume it; it is used up when someone successfully accepts.
- QR-code scanning is not part of the first version. It can be considered for a later release.

This keeps connection intentional and private while making it easy to invite a long-distance or nearby partner through a messaging app.

### One-sided acceptance — invitee decides

- After the invitee opens the private link, they see the inviter's normal profile and can choose to accept or decline.
- If the invitee accepts, the two accounts become connected immediately; the inviter does not need to approve a second request.
- If the invitee declines, the accounts remain unconnected.
- Each invitation is single-use. Once accepted, the link expires and cannot be used again.

## 2. My Day — Home

**Purpose:** Help the user manage their own day through one simple task list and personal progress. In Connected Mode, My Day may also include a compact overview of the partner's progress.

Initial content:
- One **Today's Tasks** list containing the user's daily tasks.
- The user's personal daily progress.
- In Connected Mode only, a compact overview of the partner's progress. This is not shown in Solo Mode.

The partner overview should provide an at-a-glance completion summary, for example:
- **3 of 5 tasks completed**
- **60% complete**
- A visual progress bar.

Tapping the partner overview should open the Partner page for more detail.

### My Day visual hierarchy — Option C confirmed

Use a **balanced focus**:
- The user's personal progress appears first and remains the primary focus.
- The partner's progress appears immediately below in a compact, easy-to-scan overview.
- The user's daily task list follows.
- In Connected Mode, the Partner overview remains visible near the top without making My Day feel like a shared dashboard.
- In Solo Mode, omit the Partner overview entirely so My Day remains a complete personal experience.

This keeps My Day personal while making the partner's journey visible and reinforcing the idea that both people are growing together.

### Adding tasks — capability confirmed, interface undecided

- Users need a way to add tasks to their lists.
- The visual treatment and interaction pattern for adding a task will be decided after sketching the My Day screen; do not commit to a specific button, sheet, or separate screen yet.

### Daily task organization — one unified list confirmed

- Show all personal daily tasks together in one **Today's Tasks** section.
- Do not create a separate Morning Routine section or divide tasks into Morning, Afternoon, and Evening categories.
- Keep the task list in its existing order; users do not need to drag, rearrange, or prioritize tasks manually.
- Let users tap any task to mark it complete, regardless of its position in the list. For example, Task 2 can be completed while Tasks 1 and 3 remain unfinished.
- When a task is completed, keep it in the same position and show its completed state (for example, a checkmark and subdued or struck-through text). Do not automatically move completed tasks to the bottom.
- Do not impose a fixed completion sequence or time-of-day grouping on daily tasks.

This keeps My Day simple and flexible, with one clear place for all daily tasks.

## 3. Partner

**Purpose:** Help the user understand what their partner is doing and how their day is progressing.

Initial content:
- The partner's daily tasks.
- Completed and unfinished work, with the current progress of tasks.
- A summary of the partner's overall daily progress.
- Relevant activity and journey/arrival updates.
- A **Partner Alarm** area where partners can create and manage personalized alarms for each other.

A user should be able to tap an individual partner task to open its detail view. The exact fields and interactions in that detail view are still to be designed.

### Partner task progress — optional percentage

- Support simple task states such as **Not started** and **Completed** for ordinary tasks.
- Allow a task to show a percentage when progress is meaningful (for example, a longer-running project).
- Percentage progress is optional; do not require every task to have a percentage.
- **Only the task owner can update their own task's progress**, including its optional percentage; the partner can view the shared progress but cannot edit it.
- The Partner page should show each task's appropriate progress representation, while My Day can retain a compact overall completion summary.
- The exact interaction for setting and updating a task's percentage remains to be designed.

### Emotional security principle

The experience should communicate a partner's real activity and progress rather than relying on a separate manual availability label such as “Busy” or “Available”.

For example, seeing that a partner is working on a task, has completed some tasks, or is travelling home can help the other person understand their situation without repeatedly asking.

This should create reassurance and understanding, not surveillance or pressure.

## 4. Our Goals

**Purpose:** Give both partners a dedicated place to work towards a shared future.

Initial content:
- Mutual goals.
- Shared tasks and responsibilities.
- Each partner's contributions.
- Overall progress towards each shared goal.

Examples may include saving for a wedding, planning a trip, or preparing for a future home.

### Goal screen structure — reusable screen confirmed

Use one reusable **Goal Screen** with three modes:
- **Create** — create a personal or shared goal.
- **View** — see the goal's details and progress, including relevant partner contributions and milestones.
- **Edit** — update a goal.

Keep these modes within one screen rather than creating separate Goal Details and Add / Edit Goal screens. The exact goal fields, layout, milestones, and contribution interactions remain to be designed.

## 5. Partner Alarm — included in the MVP

**Purpose:** Let partners create personalized, playful alarms for each other as a way to show care and encourage daily routines.

The Partner screen will include a **Partner Alarm** area. Alarm experiences may include:
- Songs or music selected as the alarm sound.
- A partner's recorded voice, funny voices, or other playful sound effects.
- A math question that the person must solve to dismiss the alarm.
- Fun challenges, such as shaking the phone or doing a small physical activity, before dismissing the alarm.

The alarm should feel personal, playful, and supportive. Challenges are optional ways to make waking up more engaging; they must not become punishment, surveillance, or proof of obedience.

### Rest-day decision — Option C confirmed

- Each person controls their own rest days and can choose when they need time off.
- Partners can also gift each other a rest day as a gesture of care.
- The feature should express gratitude and mutual support, never control or pressure.

Partner Alarm is part of the MVP. The exact alarm setup flow, music and sound selection, recording options, challenge types, dismissal behavior, scheduling, and rest-day interactions remain to be designed.

## 6. Structure at a glance

| Destination | Main responsibility |
|---|---|
| **My Day** | Personal tasks and progress; compact partner-progress overview only when connected |
| **Partner** | Partner's tasks, task progress and details, activities, journey updates, and Partner Alarm |
| **Our Goals** | Mutual goals, shared responsibilities, contributions, and shared progress |

## 7. Confirmed decisions

- [x] For a new user signing up with email and password, complete email verification before Profile Setup; the first-time flow is Welcome / Authentication → Email Verification → Profile Setup → My Day. Google sign-in skips the separate verification step.
- [x] Support email-and-password registration and Google sign-in in the MVP; defer Apple sign-in.
- [x] Require email verification after email-and-password sign-up and before Profile Setup; use a dedicated Email Verification screen. Google sign-in does not need a separate verification step.
- [x] Use one shared Welcome / Authentication screen for both Sign Up and Sign In.
- [x] Allow returning users with completed profiles to go directly to My Day after signing in.
- [x] After first-time Profile Setup, take users directly to My Day without a separate introductory walkthrough.
- [x] Do not require a partner connection during onboarding; users can start in Solo Mode.
- [x] Keep initial Profile Setup minimal: display name is required; profile photo and short introduction are optional.
- [x] Combine profile management and app preferences in one **Profile & Settings** screen for the MVP.
- [x] In Solo Mode, the locked Partner or Our Goals page provides an “Unlock this feature” action that leads to a dedicated invitation page to generate a private partner invitation link.
- [x] Use a private, shareable invitation link carrying an invitation code/token in the first version; defer QR-code scanning to a later release.
- [x] Make each invitation single-use: after one invitee accepts and the connection is established, the invitation expires and cannot be accepted by another account.
- [x] Use one-sided acceptance: the invitee reviews the inviter's normal profile and accepts or declines; acceptance connects the accounts immediately without a second approval from the inviter.
- [x] Use a bottom navigation bar with three primary tabs.
- [x] Make My Day the default home screen.
- [x] Support only one active partner connection per account.
- [x] Give Our Goals its own dedicated page.
- [x] Show a small partner-progress overview on My Day only in Connected Mode; omit it in Solo Mode.
- [x] Use a visual progress bar and a completed/total summary (for example, 3/5 and 60%).
- [x] Open the Partner page when the user wants to see more of the partner's progress.
- [x] Integrate emotional-security information into My Day and Partner instead of creating a separate page.
- [x] Allow a partner's task to be opened for more detail.
- [x] Include Partner Alarm in the MVP as part of the Partner experience, with personalized sounds/music and playful dismissal challenges such as math questions or fun activities.
- [x] Keep all daily tasks together in one Today's Tasks list; do not add a separate Morning Routine section or time-of-day categories.
- [x] Allow users to tap any general daily task to mark it complete, regardless of its position in the list.
- [x] Keep completed tasks in their original position in the list; show completion in place rather than moving the task.
- [x] Make individual task percentages optional; use simple completion states for tasks that do not need percentage tracking.
- [x] Let each task owner update their own task progress; partners can view shared progress but cannot edit the other's tasks.
- [x] Keep tasks in their existing order; do not require drag-and-drop or manual rearrangement.
- [x] Use one reusable Task Screen for creating, viewing, and editing tasks instead of separate Task Details and Add / Edit Task screens. A user's own task can be edited by its owner; a partner's task is view-only.

## 8. Still to design

These details are intentionally not finalised yet:
- Whether additional profile information is needed beyond the confirmed minimal setup.
- The exact sections and layout inside each of the three pages.
- The information and actions shown in a task-detail view.
- The precise task-progress states and how progress is calculated.
- The Partner Alarm setup and management experience, including sound/music selection, partner voice recordings, challenge options (such as math or fun activities), dismissal behavior, scheduling, and rest-day controls.
- How journey and arrival updates are presented and controlled.
- What each partner can choose to share, and the privacy boundaries around shared activity.
- Partner invitation details: profile visibility before connection, invitation-link validity, and what happens when an invitation is declined or revoked.

## 9. Confirmed MVP screen inventory

The MVP screen inventory is confirmed at **11 reusable screens**. Some experiences, such as locked states and invitation actions, are states or contexts within existing screens rather than separate screens.

### Account and onboarding
- **Welcome / Authentication** — one shared screen where users can switch between Sign Up and Sign In using email and password or Google.
- **Email Verification** — a dedicated screen shown after email-and-password sign-up and before Profile Setup. Google sign-in skips this screen.
- **Profile Setup** — add a required display name and optionally add a profile photo and short introduction after first-time account creation.

### Main app
- **My Day** — personal routines, tasks, and progress; compact partner progress appears only in Connected Mode.
- **Partner** — partner activity and task progress; shows the locked state in Solo Mode.
- **Our Goals** — shared goals and responsibilities; shows the locked state in Solo Mode.

### Partner connection
- **Invitation Page** — generate and share a private, single-use invitation link.
- **User Profile Screen** — reusable profile view for another user. When opened through an invitation link, it shows the inviter's normal profile with Accept and Decline actions; invitation context does not require a separate profile screen.

### Task and goal details
- **Task Screen** — one reusable screen with Create, View, and Edit modes. Users can create a task, view its details and progress, or edit their own task. A partner's task is view-only; partners cannot edit another person's task.
- **Goal Screen** — one reusable screen with Create, View, and Edit modes. Goal-specific details such as shared progress, partner contributions, and milestones remain to be designed.

### Account management
- **Profile & Settings** — one combined screen for viewing and managing the user's profile and app preferences; do not split these into separate top-level screens in the MVP.

**Partner Alarm:** The feature is included in the MVP and belongs within the Partner destination. The exact UI and whether alarm creation/management needs a dedicated reusable screen will be decided during UI refinement; do not assume a separate screen before that decision.

The current primary screen inventory remains the starting point. Detailed layouts, content hierarchy, and interactions will be worked out during UI refinement and wireframing.

## 10. Next step

Continue refining the existing UI before proceeding with additional wireframes. Update My Day to use one Today's Tasks list, then refine the Partner page to include Partner Alarm. Decide the alarm entry point and interaction structure before selecting detailed UI components or implementation details.

> This is an initial design structure based on the founder's decisions. It is not yet a final UI specification or a validated set of requirements.
