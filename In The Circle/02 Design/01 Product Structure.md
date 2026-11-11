# Product Structure — In The Circle

> **Phase:** Design  
> **Status:** Initial structure decisions confirmed; screen-level details remain open.  
> **Product philosophy:** Connect → Support → Grow

## 1. Navigation model

The application will use a **bottom navigation bar** with three primary destinations:

1. **My Day** — the user's home screen.
2. **Partner** — a deeper view of the partner's daily activities and progress.
3. **Our Goals** — a dedicated space for goals and responsibilities shared by both partners.

There will be **no separate Emotional Security tab**. Emotional security should be supported within the My Day and Partner experiences.

## 2. My Day — Home

**Purpose:** Help the user manage their own day while staying aware of their partner's progress.

Initial content:
- The user's daily to-do list.
- The user's personal daily progress.
- A compact overview of the partner's progress.

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
- The Partner overview remains visible near the top without making My Day feel like a shared dashboard.

This keeps My Day personal while making the partner's journey visible and reinforcing the idea that both people are growing together.

### Adding tasks — capability confirmed, interface undecided

- Users need a way to add tasks to their lists.
- The visual treatment and interaction pattern for adding a task will be decided after sketching the My Day screen; do not commit to a specific button, sheet, or separate screen yet.

### Daily task organization — flexible structure confirmed

- Keep a dedicated **Morning Routine** section for tasks that are specifically part of the user's morning routine.
- Keep other tasks together in one **Today's Tasks** list rather than dividing them into Morning, Afternoon, and Evening sections.
- Keep the task list in its existing order; users do not need to drag, rearrange, or prioritize tasks manually.
- Let users tap any task to mark it complete, regardless of its position in the list. For example, Task 2 can be completed while Tasks 1 and 3 remain unfinished.
- When a task is completed, keep it in the same position and show its completed state (for example, a checkmark and subdued or struck-through text). Do not automatically move completed tasks to the bottom.
- Do not impose a fixed completion sequence or time-of-day grouping on general daily tasks.

This gives routine habits a clear home while allowing the rest of the day to remain flexible and low-pressure.

## 3. Partner

**Purpose:** Help the user understand what their partner is doing and how their day is progressing.

Initial content:
- The partner's daily tasks.
- Completed and unfinished work, with the current progress of tasks.
- A summary of the partner's overall daily progress.
- Relevant activity and journey/arrival updates.

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

## 5. Partner Alarm — playful care for daily routines

**Concept:** Partners can create personalized alarms for each other as a fun way to show care and encourage healthy daily routines.

Possible experiences discussed:
- A partner chooses a playful alarm sound, such as duck quacks or a funny voice.
- A partner sets a small wake-up challenge, such as doing 10 squats.
- Partners may use their own recorded voices or other playful sounds.
- The feature should make waking up and building routines feel more fun and supportive.

### Rest-day decision — Option C confirmed

- Each person controls their own rest days and can choose when they need time off.
- Partners can also gift each other a rest day as a gesture of care.
- The feature should express gratitude and mutual support, never control or pressure.
- Challenges are encouragement, not proof of obedience.

The detailed alarm controls, challenge rules, notifications, and dismissal behavior are still to be designed. The concept is mutual: both partners can give and receive these gestures.

## 6. Structure at a glance

| Destination | Main responsibility |
|---|---|
| **My Day** | My tasks and progress, plus a compact partner-progress overview |
| **Partner** | Partner's tasks, task progress and details, activities, and journey updates |
| **Our Goals** | Mutual goals, shared responsibilities, contributions, and shared progress |

## 7. Confirmed decisions

- [x] Use a bottom navigation bar with three primary tabs.
- [x] Make My Day the default home screen.
- [x] Give Our Goals its own dedicated page.
- [x] Show a small partner-progress overview on My Day.
- [x] Use a visual progress bar and a completed/total summary (for example, 3/5 and 60%).
- [x] Open the Partner page when the user wants to see more of the partner's progress.
- [x] Integrate emotional-security information into My Day and Partner instead of creating a separate page.
- [x] Allow a partner's task to be opened for more detail.
- [x] Include the Partner Alarm concept as a playful, mutual way to support daily routines.
- [x] Choose rest-day approach C: each person controls their own rest days, and partners can also gift each other a rest day.
- [x] Keep the feature rooted in gratitude and care, not control.
- [x] Keep a dedicated Morning Routine section, with all other tasks in one flexible Today's Tasks list.
- [x] Allow users to tap any general daily task to mark it complete, regardless of its position in the list.
- [x] Keep completed tasks in their original position in the list; show completion in place rather than moving the task.
- [x] Make individual task percentages optional; use simple completion states for tasks that do not need percentage tracking.
- [x] Let each task owner update their own task progress; partners can view shared progress but cannot edit the other's tasks.
- [x] Keep tasks in their existing order; do not require drag-and-drop or manual rearrangement.

## 8. Still to design

These details are intentionally not finalised yet:
- The exact sections and layout inside each of the three pages.
- The information and actions shown in a task-detail view.
- The precise task-progress states and how progress is calculated.
- How journey and arrival updates are presented and controlled.
- What each partner can choose to share, and the privacy boundaries around shared activity.
- Partner Alarm details: alarm creation, scheduling, sound selection, challenge library/customization, notification behavior, and how a receiver can dismiss or skip an alarm.

## 9. Next step

Define the **screen-level structure** for each destination, starting with My Day: identify its sections, their order, and what the user can do from each section.

> This is an initial design structure based on the founder's decisions. It is not yet a final UI specification or a validated set of requirements.
