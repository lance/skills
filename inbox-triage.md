# Inbox Triage

## Goal

Maintain a low-clutter inbox without pursuing Inbox Zero at all costs.

The primary goal is removing junk. The secondary goal is keeping useful
mail organized and preventing old, non-actionable messages from
accumulating in the Inbox.

Messages may intentionally remain in the Inbox as reminders of things
that require attention.

When classification is uncertain, prefer leaving a message alone.

------------------------------------------------------------------------

## Labels

Triage-specific labels live under the `!!Triage` namespace so they
remain grouped near the top of Gmail's label list and do not conflict
with Gmail's own labels.

### States

-   `!!Triage/Action` --- the message appears to require the user to do
    something.
-   `!!Triage/Keep` --- explicit user override; automated triage must
    leave the message in the Inbox.

### Classifications

-   `!!Triage/Important` --- consequential financial, medical,
    government, insurance, tax, legal, security, billing, or similar
    mail.
-   `!!Triage/Personal` --- correspondence primarily written by a person
    directly to the user.
-   `!!Triage/Promotion` --- potentially useful commercial marketing
    from companies with which the user has an established relationship.
-   `!!Triage/Subscription` --- newsletters and other content the user
    intentionally subscribed to.

State and classification labels are not mutually exclusive. For example,
a message may be both `!!Triage/Important` and `!!Triage/Action`.

More specific nested labels may be introduced later if actual usage
demonstrates a need, for example `!!Triage/Important/Medical`.

### Existing Gmail Labels

Do not repurpose, modify, remove, or otherwise interfere with existing
Gmail system or managed labels.

In particular, do not confuse triage labels with Gmail's existing
`IMPORTANT`, Personal, Promotions, or `unsubscribe` functionality.

Leave the existing `!!TODO` label unchanged.

Do not create new triage labels until the proposed classifications have
been tested against actual mail.

------------------------------------------------------------------------

## Classification and Actions

### Obvious Commercial Junk

Unsolicited commercial or marketing mail with no apparent value should
be moved to Trash.

When practical, unsubscribe from recurring unwanted marketing.

A previous relationship with a company does not automatically make all
of its marketing valuable.

Never permanently delete email. "Trash" means move the message to Gmail
Trash.

### Transactional Mail

Mail generated as the result of an action the user took should be
retained.

Examples include:

-   Receipts
-   Order confirmations
-   Shipping and delivery updates
-   Reservation confirmations
-   Requested reminders
-   Routine account notifications

#### Unread Transactional Mail

**Never archive unread transactional mail.**

Unread transactional messages must remain in the Inbox.

Before performing triage actions, assess how much unread transactional
mail is present. If there appears to be an unusually large backlog, stop
and alert the user before making any changes.

Do not mark transactional messages read merely to make them eligible for
archival.

There is intentionally no fixed numerical definition of "unusually
large" yet. Establish an appropriate threshold based on experience with
actual inbox triage.

#### Read Transactional Mail

Read transactional messages that are no longer current or actionable may
be archived.

If a transactional message still appears to require action, apply
`!!Triage/Action` and leave it in the Inbox.

#### Backlog Recovery

The normal rule is that unread transactional mail must remain in the
Inbox. An exception may be made during an explicitly approved
backlog-recovery operation.

During backlog recovery, old unread transactional messages may be marked
read and archived when the message clearly describes a successfully
completed event and contains no indication of required action, failure,
dispute, security concern, upcoming event, or unresolved state.

Examples of potentially safe completed events include:

-   A package that was successfully delivered in the past
-   A payment that was successfully processed
-   A transfer that completed successfully
-   A paid invoice or receipt for a completed transaction

Do not apply this exception to messages about transactions that are
still pending or in progress.

Do not apply this exception to failed payments, account or security
warnings, upcoming appointments or reservations, disputed transactions,
unusual activity, or any message whose final state is unclear.

For routine bank transfer status notifications, messages older than **14
days** may be treated as stale transactional status mail during backlog
recovery even when no matching "transfer complete" message can be found.
This includes routine recurring-transfer reminders, requested-transfer
notices, in-progress notices, and completion notices.

Do not apply this rule when the message indicates a failed, declined,
canceled, disputed, unauthorized, suspicious, or otherwise exceptional
transfer, or explicitly requires user action. Standard boilerplate
explaining what to do if the user did not authorize an otherwise routine
transfer does not by itself make the message exceptional.

During backlog recovery, unread calendar or event notifications may be
marked read and archived when the event has a specific date that is
clearly in the past.

Do not apply this rule to future events, recurring events whose series
may still be active, cancellations or changes that may still matter, or
messages where the event status or date is unclear.

Backlog recovery must be explicitly approved by the user. Prefer
processing one clearly defined category at a time, beginning with
low-risk categories such as old completed shipping and delivery
notifications.

### Promotions

Marketing from a company with which the user has an established
relationship may be potentially useful even when it does not belong in
the Inbox.

Apply `!!Triage/Promotion` and archive it.

Retain promotional messages for no more than **60 days**.

Retain a maximum of **3 promotional messages per sender**. When more
than three exist, keep the three most recent or relevant and trash the
remainder.

High-volume marketing should not accumulate simply because the sender is
a company the user sometimes does business with.

Consider unsubscribing when a sender's frequency substantially exceeds
its usefulness.

Marketing from a company with no apparent useful relationship to the
user should generally be unsubscribed from when practical and moved to
Trash.

### Subscriptions

Content the user intentionally subscribed to is useful content, not
promotional junk.

Examples include:

-   Community and local organizations
-   Clubs
-   Newsletters
-   Substacks
-   Technical publications
-   Local government information

New subscription messages should remain visible in the Inbox initially.

After **30 days**, archive subscription messages unless they have been
explicitly protected with `!!Triage/Keep` or remain actionable.

Do not automatically unsubscribe from intentional subscriptions.

Local and community content deserves particular protection when
classification is uncertain.

If it is unclear whether something is an intentional subscription or
unwanted marketing, leave it alone.

### Nextdoor

Nextdoor mail is low-priority neighborhood browsing content. Retain all
Nextdoor messages received within the most recent **24 hours**
in their current location and read state.

Move Nextdoor messages older than 24 hours to Trash, whether read or
unread and whether in the Inbox or archived. Identify Nextdoor by the
sender's `nextdoor.com` domain or its subdomains, not by mentions of
Nextdoor in other correspondence.

This sender-specific rule takes precedence over normal classification
and retention rules, including Important, Personal, Subscription, and
transactional-mail rules. `!!Triage/Keep` and `!!Triage/Action` still
protect messages from cleanup.

Do not unsubscribe from Nextdoor; the recent messages remain useful for
occasional neighborhood browsing. Never permanently delete messages.

### Personal Correspondence

Messages primarily written by a person directly to the user should never
be automatically trashed.

Apply `!!Triage/Personal`.

Personal correspondence may remain in the Inbox while current or
potentially actionable.

After **60 days**, personal correspondence that is no longer apparently
active or actionable may be archived while retaining the
`!!Triage/Personal` label.

`!!Triage/Keep` and `!!Triage/Action` override age-based archival.

Mailing lists and group discussions should not automatically be
classified as Personal merely because individual humans wrote the
messages.

### Important Mail

Apply `!!Triage/Important` to consequential messages involving subjects
such as:

-   Financial matters
-   Medical matters
-   Government agencies
-   Insurance
-   Taxes
-   Legal matters
-   Bills
-   Account and security warnings

Important messages must never be automatically trashed or unsubscribed
from.

They may be archived when no longer current or actionable.

If action appears necessary, also apply `!!Triage/Action` and leave the
message in the Inbox.

`!!Triage/Keep` overrides automatic archival.

More specific classifications such as `!!Triage/Important/Medical` or
`!!Triage/Important/Financial` may be introduced later if actual usage
demonstrates that they are useful.

### Two-Factor Authentication

One-time authentication codes and similar 2FA messages have extremely
short-lived value.

2FA messages may always be moved to Trash during inbox triage.

Do not confuse a 2FA code with an account security warning.

Security warnings should be classified as `!!Triage/Important` and must
not be automatically trashed.

------------------------------------------------------------------------

## Overrides

### `!!Triage/Keep`

`!!Triage/Keep` means automated triage should leave the message in the
Inbox regardless of age or normal classification rules.

Never automatically trash or archive a message labeled `!!Triage/Keep`.

### `!!Triage/Action`

`!!Triage/Action` means the message appears to require the user to do
something.

Leave messages labeled `!!Triage/Action` in the Inbox regardless of
normal age-based archival rules.

Once the action has been completed and the `!!Triage/Action` label
removed, the message can be handled according to its normal
classification.

------------------------------------------------------------------------

## Safety Rules

When uncertain, leave the message alone.

Never permanently delete email.

Never automatically trash personal correspondence.

Never automatically trash or unsubscribe from Important messages.

Never automatically unsubscribe from intentional Subscriptions.

Never archive unread transactional mail.

Never mark a message read simply to make it eligible for cleanup.

Respect `!!Triage/Keep` and `!!Triage/Action` before applying any other
cleanup rule.

Do not modify Gmail's existing system or managed labels as part of
triage.

When a new category or recurring ambiguity appears, ask the user rather
than inventing a permanent rule.

------------------------------------------------------------------------

## Operating Procedure

### Before Making Changes

1.  Inspect the current Inbox and assess the overall state.
2.  Check for an unusually large backlog of unread transactional mail.
3.  If such a backlog exists, report it and stop before taking cleanup
    actions.
4.  Respect existing `!!Triage/Keep` and `!!Triage/Action` labels.
5.  Classify messages according to this document.

### Dry Run

When testing new or changed triage rules, perform a read-only dry run
first.

Report how messages would be classified and what actions would be taken
without modifying Gmail.

Use ambiguities discovered during the dry run to refine this document.

### Applying Triage

Only after the rules have been sufficiently validated should triage
modify messages.

Actions may include:

-   Applying `!!Triage/*` labels
-   Archiving messages
-   Moving junk or expired promotional messages to Trash
-   Identifying recurring marketing that may be worth unsubscribing from

Prefer conservative action whenever confidence is low.

------------------------------------------------------------------------

## Evolution

This document is expected to evolve.

When actual inbox triage reveals a recurring situation that is not
adequately covered here, discuss the desired behavior with the user and
update this document.

Prefer adding rules in response to real examples rather than
anticipating every possible email category in advance.

Keep the system simple enough that its behavior remains understandable
and predictable.
