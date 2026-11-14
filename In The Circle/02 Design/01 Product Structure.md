# Product Structure — In The Circle

> **Phase:** Design / MVP UI refinement  
> **Status:** Core product structure and key dashboard decisions confirmed; remaining screen-level details are being finalized before manual Figma work.  
> **Product philosophy:** Connect → Support → Grow  
> **Working constraint:** Finalize layouts and interactions in conversation first. The founder will recreate the agreed UI manually in Figma; avoid unnecessary Figma AI generations.

## 1. Product and navigation model

In The Circle is a relationship app for committed couples. It helps partners connect through everyday life, support each other's individual progress, and grow towards shared goals.

The application uses a bottom navigation bar with three primary destinations:

1. **My Day** — the user's own daily activities and progress.
2. **Partner** — the partner's daily activities and progress, plus Partner Alarm.
3. **Our Goals** — goals both partners are working towards together.

There is no separate Emotional Security tab. Reassurance and understanding should come naturally through the My Day and Partner experiences.

### 1.1 Solo and connected experiences

- A person can use In The Circle alone without needing a partner connection.
- Each account can have only one active partner connection at a time, reflecting the product's focus on committed, two-person relationships.
- My Day remains fully usable in Solo Mode, including personal tasks and individual progress.
- The three main tabs remain visible in Solo Mode.
- In Solo Mode, opening Partner or Our Goals shows an in-page locked/connection state. Do not interrupt the user with unsolicited pop-ups or repeated connection reminders.
- After a partner connection is established, Partner and Our Goals become available, and the partner-progress card appears on My Day.
- The exact visual treatment of the locked states remains to be finalized.

### 1.2 Onboarding — account and profile first

- New users create an account and complete their profile before entering the main app.
- After Profile Setup, take the user directly to My Day. Do not add a separate introductory walkthrough or tutorial to the MVP.
- MVP authentication methods: email and password, or Google sign-in. Apple sign-in is not included in the initial MVP.
- Use one shared Welcome / Authentication screen for Sign Up and Sign In.
- Email-and-password sign-up requires email verification before Profile Setup.
- Google sign-in does not require a separate email-verification screen.
- A returning user with a completed profile goes directly to My Day after signing in.
- Initial Profile Setup stays minimal: display name is required; profile photo and short introduction are optional.
- Partner connection is not required during onboarding; users can begin in Solo Mode.
- Profile management and app preferences remain combined in one Profile & Settings screen.

### 1.3 Partner connection — MVP invitation method

- Use a private, shareable invitation link generated for the intended partner. The link carries the invitation code/token, so the recipient does not need to type it manually.
- The inviter can share the link through external messaging apps such as Telegram or Messenger.
- When the recipient opens the link, In The Circle opens the inviter's normal profile. The recipient can review the profile and explicitly accept or decline.
- Each invitation is single-use: it is consumed only when an invitee successfully accepts and the connection is established.
- Simply opening or viewing the invitation does not consume it.
- QR-code scanning is not part of the first version.
- If the invitee accepts, the accounts connect immediately; the inviter does not need to approve a second request.
- If the invitee declines, the accounts remain unconnected.

## 2. My Day — home dashboard

**Purpose:** Help users manage their own daily activities while keeping their partner's progress visible in Connected Mode.

### 2.1 Confirmed dashboard layout

In Connected Mode, the layout is:

1. Header with a friendly greeting and date.
2. **Your Progress** and **Partner Progress** cards side by side.
3. **Today's Tasks** as a full-width section underneath.
4. Bottom navigation: My Day, Partner, Our Goals.

In Solo Mode:
- Show the user's own progress card without a partner-progress card.
- Keep Today's Tasks full-width.
- Keep the same bottom navigation.

### 2.2 Progress cards — playful direction confirmed

Both progress cards use a consistent structure and a friendly, playful visual style:

- Small playful illustration.
- Clear title: Your Progress or Partner Progress.
- Completed tasks / total tasks (for example, 3/5).
- Rounded visual progress bar.
- Completion percentage.
- Optional short, encouraging microcopy.

The cards sit side by side in Connected Mode. They should feel warm and motivating, not like a competitive productivity dashboard.

**Navigation rule:** Tapping the Partner Progress card on My Day opens the Partner tab/dashboard. It does not open the partner profile.

### 2.3 Today's Tasks — one unified list confirmed

- Show the user's daily tasks together in one full-width Today's Tasks section.
- Do not create a separate Morning Routine section or divide tasks into Morning, Afternoon, and Evening categories.
- Users can tap a task to mark it complete; tap again to undo completion.
- Completed tasks stay in their original positions and show a checkmark plus subdued or struck-through text.
- Do not automatically move completed tasks to the bottom.
- Do not require drag-and-drop, manual rearrangement, or a fixed completion sequence.
- The task owner is responsible for completing their own tasks.

A reusable Task Screen can support creating, viewing, and editing a task. A user's own task is editable by its owner.

## 3. Partner — partner dashboard

**Purpose:** Help each person understand what their partner is doing, see their progress, and support them through everyday life.

### 3.1 Confirmed dashboard layout

The Partner dashboard contains:

1. Header with the partner's name and a short personal status/message.
2. Partner profile/avatar icon at the top right.
3. **Partner Progress** and **Dynamic Partner Alarm** cards side by side.
4. **Today's Tasks** as a full-width section underneath.
5. Bottom navigation: My Day, Partner, Our Goals.

The visual style should match My Day: friendly, playful, clean, card-based, and easy to scan.

### 3.2 Partner profile navigation

- Tapping the profile/avatar icon in the Partner header opens the Partner Profile / Overview.
- The Partner Progress card is not a shortcut to the partner profile.
- The Partner Progress card on My Day opens the Partner dashboard, not the profile.
- Partner Profile is a separate destination reached through the profile/avatar icon.

### 3.3 Partner Progress

- The Partner Progress card summarizes the partner's daily task progress.
- It uses the same visual language as the progress cards on My Day: playful illustration, completed/total count, progress bar, and percentage.
- Do not use this card as a profile shortcut.

### 3.4 Today's Tasks — shared visibility and individual responsibility

- Show the partner's daily tasks in the Partner dashboard's full-width Today's Tasks section.
- The other partner can view the partner's tasks, completed states, and progress.
- Do not hide ordinary daily tasks behind a separate per-task sharing choice. The shared daily-task view supports the product's purpose of understanding and growing alongside one another.
- **Only the task owner can mark their own tasks complete or undo their own completion.**
- The other partner can view progress but cannot complete or edit tasks on the owner's behalf.
- Keep the task list in the same order as the owner's list.

**Product principle:** We grow together, but each person remains responsible for their own growth.

### 3.5 Partner Profile / Overview

The Partner Profile is opened through the profile/avatar icon at the top of the Partner dashboard. It is separate from the Partner Progress card.

The exact profile fields and overview content still need UI refinement. Do not route the Partner Progress card to this screen.

## 4. Partner Alarm — MVP feature inside Partner

**Purpose:** Let one partner create a thoughtful, playful experience for the other. Partner Alarm is a way to express care, share memories, make each other smile, encourage each other, and build shared rituals — not a general-purpose alarm-clock system.

### 4.1 Entry point and dynamic card

- Partner Alarm belongs inside the Partner UI; it is not a separate bottom-navigation destination.
- The Dynamic Partner Alarm card sits side by side with Partner Progress.
- If a scheduled alarm exists, the card shows the next scheduled alarm's time and type.
- If no alarm exists, the card shows **“+ Create Alarm”**.
- Tapping the card opens Partner Alarm management.

### 4.2 Alarm content types

MVP alarm content may include:

- A meaningful song or music choice.
- A voice message recorded by the partner.
- A funny sound or playful audio.
- A math question.
- A playful challenge.

The experience should remain caring, voluntary, playful, and non-controlling. A recipient must have a clear way to dismiss or skip an interactive challenge; the alarm must not become punishment, surveillance, or proof of obedience.

### 4.3 Basic end-to-end flow

1. The creator opens Partner Alarm from the Partner dashboard.
2. The creator starts creating an alarm.
3. The creator chooses an alarm experience type and supplies its content.
4. The creator chooses when it should happen and may add a personal message.
5. The creator reviews and schedules the alarm.
6. At the scheduled time, the recipient receives the alarm experience.
7. The recipient can listen, interact, or skip/dismiss.
8. After dismissal, show the creator's optional personal message in a small dialog when one exists. If there is no message, do not show an empty dialog.

### 4.4 Alarm screens and states to design

- **Partner Alarm Management** — view and manage upcoming partner alarms; entry point is the dynamic card.
- **Create/Edit Alarm** — choose the experience type, configure its content, set its schedule, add an optional personal message, and preview it.
- **Receiving Alarm Experience** — an adaptable recipient experience for songs, voice/funny audio, math questions, and playful challenges.
- **Post-alarm Message Dialog** — optional message shown after dismissal when the creator supplied one.
- **Permission/unavailable state** — explain clearly when the recipient's device cannot receive the alarm because required notification/alarm permissions are unavailable.

Do not add unrelated clock features such as world clocks, stopwatch, timers, or a generic alarm-clock dashboard.

Scheduling details such as repeat options, time-zone handling, and exact sound/music source are still open and should be finalized only when needed for the UI and technical plan.

## 5. Our Goals — shared goals only

**Purpose:** Give both partners a dedicated place to work towards a shared future.

- Our Goals contains shared goals only.
- Do not add separate My Goals or Partner's Goals sections here; individual daily activities belong in My Day and Partner.
- Our Goals uses the same bottom-navigation destination and visual language as the rest of the app.

### 5.1 Our Goals dashboard — confirmed design direction

The dashboard contains:

1. Header: Our Goals and a short supportive subtitle.
2. An **Our Journey** summary showing active goals and completed milestones.
3. **Our Shared Goals** section with an Add action.
4. Full-width goal cards, one per row.
5. A separate **Completed Together** section for completed goals.
6. Bottom navigation.

Goal cards use small playful illustrations rather than plain icons. Each active goal card can show:
- Goal illustration.
- Goal title and optional short description.
- Overall progress percentage and progress bar.
- Completed milestones / total milestones.
- Next milestone, when applicable.

Completed goals move out of the active list into Completed Together.

### 5.2 Milestone-based progress — confirmed

- Goal progress is calculated from milestones, not entered as a manually adjusted percentage.
- Overall progress = completed milestones ÷ total milestones.
- A milestone counts as completed only after its required completion rule has been satisfied.
- When all milestones are complete, the goal moves into Completed Together.

### 5.3 Two milestone completion rules — confirmed

Each milestone has its own completion rule:

1. **Either partner** — either partner can mark the milestone complete; it becomes complete for both.
2. **Both partners** — each partner must confirm completion individually; the milestone becomes complete only after both have confirmed.

- Default rule: **Either partner**.
- The creator can choose the rule for each milestone.
- For Both partners, one partner's confirmation must never automatically confirm for the other.
- Both partners can see the confirmation status.
- The app records who confirmed and when.
- Goal progress increases only after the milestone is fully completed.

### 5.4 Goal and milestone screens

Use a reusable **Goal Screen** with Create, View, and Edit modes unless a later usability test shows that a separate screen is necessary.

Goal details include:
- Goal title and description.
- Overall milestone-based progress.
- Milestone list and completion states.
- Who confirmed a milestone when Both partners is selected.
- Add Milestone action.

The exact milestone editor and confirmation presentation (inline state, dialog, or sheet) remain to be finalized during UI refinement.

## 6. MVP screen inventory

The following is the working MVP screen/state inventory for manual Figma design. Some items are reusable screens; others are states or dialogs within a screen.

### Account and onboarding
1. **Welcome / Authentication** — shared Sign Up and Sign In screen; email/password or Google.
2. **Email Verification** — shown after email/password registration.
3. **Profile Setup** — required display name; optional profile photo and introduction.
4. **Invitation Page** — generate and share a private, single-use partner invitation link.
5. **Partner Profile / Invitation Review** — inviter's profile with Accept and Decline actions when opened through an invitation.

### Main app
6. **My Day Dashboard** — greeting/date, side-by-side progress cards in Connected Mode, full-width Today's Tasks, and bottom navigation.
7. **Task Screen** — reusable Create, View, and Edit modes; owner can edit their own task.
8. **Partner Dashboard** — partner header/status/avatar, side-by-side Partner Progress and Dynamic Partner Alarm cards, full-width partner Today's Tasks.
9. **Partner Profile / Overview** — opened from the profile/avatar icon in the Partner header.
10. **Profile & Settings** — combined profile management and app preferences.

### Partner Alarm
11. **Partner Alarm Management** — list and manage partner alarms.
12. **Create/Edit Alarm** — select and configure alarm content, schedule, optional personal message, and preview.
13. **Receiving Alarm Experience** — adaptable experience for music, voice/funny audio, math, or playful challenge.
14. **Post-alarm Message Dialog** — shown only when an optional personal message exists.
15. **Alarm permission/unavailable state** — explanatory state when delivery permissions are missing.

### Our Goals
16. **Our Goals Dashboard** — Our Journey summary, active full-width goal cards, Completed Together section.
17. **Goal Screen** — reusable Create, View, and Edit modes.
18. **Milestone completion/confirmation state** — supports Either partner and Both partners rules; can be implemented within Goal Screen rather than as a separate destination.

### Shared app states
- Solo Mode locked state for Partner and Our Goals.
- Empty states for task lists, alarms, and goals.
- Loading and error states for data-dependent screens.
- Invitation expired, already used, or declined states.
- No scheduled Partner Alarm state (“+ Create Alarm”).
- Completed Together empty state.

This inventory is a practical design checklist, not a requirement to create a separate Figma page for every state. Reuse screens and components wherever possible.

## 7. Confirmed product principles and decisions

- [x] Product philosophy: Connect → Support → Grow.
- [x] Focus on committed, two-person relationships.
- [x] One active partner connection per account.
- [x] My Day is the default home screen.
- [x] Bottom navigation has My Day, Partner, and Our Goals.
- [x] Solo Mode is usable; partner-dependent tabs show an in-page locked state.
- [x] Account and profile setup happen before entering the main app.
- [x] Email/password and Google sign-in are in the MVP; Apple sign-in is deferred.
- [x] Email/password sign-up requires email verification; Google sign-in skips the separate verification screen.
- [x] Display name is required; profile photo and introduction are optional.
- [x] Partner connection is not required during onboarding.
- [x] Partner connection uses a private, shareable, single-use invitation link.
- [x] The invitee reviews the inviter's profile and accepts or declines; acceptance connects immediately.
- [x] My Day progress cards are side by side in Connected Mode.
- [x] Progress cards use a playful illustration, completed/total count, progress bar, and percentage.
- [x] Today's Tasks is full-width below the progress cards.
- [x] Daily tasks stay in one unified list; no Morning Routine section or time-of-day categories.
- [x] A user can complete or undo their own task by tapping it; completed tasks remain in place.
- [x] Tapping Partner Progress on My Day opens the Partner tab, not the partner profile.
- [x] Partner dashboard has Partner Progress and Dynamic Partner Alarm cards side by side, with Today's Tasks full-width below.
- [x] Partner header includes partner name, a short status/message, and a profile/avatar icon.
- [x] Tapping the Partner profile/avatar icon opens Partner Profile / Overview.
- [x] Partner Progress is not a shortcut to Partner Profile.
- [x] Partner's daily tasks are visible in the Partner dashboard.
- [x] Only the task owner can mark their own tasks complete or undo completion; the other partner has view-only access.
- [x] Partner Alarm is part of the Partner UI, not a separate bottom-navigation destination.
- [x] Dynamic Partner Alarm card shows the next scheduled alarm's time and type, or “+ Create Alarm” when none exists; tapping it opens management.
- [x] Partner Alarm is for care, memories, encouragement, playful moments, and shared rituals — not a general-purpose alarm clock.
- [x] Alarm content may include meaningful music, partner-recorded voice, funny sound, math question, or playful challenge.
- [x] Alarm experiences must remain voluntary, caring, and non-controlling.
- [x] Our Goals contains shared goals only.
- [x] Goal cards are full-width, one per row, with small playful illustrations.
- [x] Completed goals move to a separate Completed Together section.
- [x] Goal progress is milestone-based.
- [x] Each milestone uses Either partner or Both partners completion; Either partner is the default.
- [x] Both partners must individually confirm a Both partners milestone.
- [x] Progress updates only when the milestone's completion rule is satisfied.
- [x] Profile management and app preferences share one Profile & Settings screen.
- [x] Rest days remain an expression of personal choice and mutual care, never pressure or control.

## 8. Still to finalize

These are open UI/product details, not permission to add unrelated features:

- Exact visual styling, color palette, typography, spacing, and illustration system.
- Exact My Day and Partner header details and empty states.
- Partner Profile / Overview content.
- Whether and how journey/arrival updates fit the MVP UI.
- Exact Partner Alarm management layout and alarm editing/deletion behavior.
- Alarm repeat options, time-zone display, music source, and audio playback constraints.
- Exact math-question and playful-challenge interaction details.
- Alarm permission behavior and delivery limitations across devices.
- Exact Goal Screen layout and fields.
- Milestone add/edit and confirmation presentation.
- Empty, loading, and error-state visuals.

## 9. UI finalization workflow

To respect the project's time and Figma-credit constraints:

1. Finalize screen purpose, layout, and interactions in conversation.
2. Use text wireframes to resolve structure before visual polish.
3. Confirm the screen before moving to the next one.
4. Finalize a shared visual system after the core layouts are agreed.
5. The founder recreates the finalized UI manually in Figma.
6. Move to implementation only after the MVP screens and interactions are sufficiently specified.

Do not spend Figma AI credits on exploratory generations or screens that have not been agreed.

> This document records the current founder-approved product and UI decisions. Open items are explicitly marked as unfinished; do not silently turn proposals into confirmed requirements.
