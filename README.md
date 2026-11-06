# Cancel Culture

You signed up for a free trial for one assignment, then forgot about it. Cancel Culture is a [Cubbie](https://cubbie.ai) skill that helps you keep track of trial deadlines, subscription renewals, and expiring student discounts before the next charge.

Tell it “I only need this until my presentation,” and it saves that reason alongside the deadline. It helps with reminders and cancellation instructions; you make the account changes yourself.

Built at DevHacks S3 by **Charith Kutikuppala and Richitha Rekula**, Team Southside, for Cubbie Hackathon Track 1.

## Try it

Text the original team repository link to Cubbie and confirm installation:

```text
https://github.com/itsmeck24/cancel-culture
```

Then forward a trial email, paste its contents, or send a screenshot. For example:

- “Remind me before this trial charges.”
- “My student discount is ending. How do I renew it?”
- “Check my email for upcoming renewals.”

Connecting Google is optional and only needed for email search. Forwarded messages work without it.

## What happens behind the scenes

Cubbie reads the message. A Python script saves the details, calculates reminder times, and updates the record when a newer email changes a deadline. Reading the same message twice does not create a duplicate record.

The trial end, charge date, and cancellation cutoff are stored separately. Instructions point to the actual billing provider, such as Apple, Google Play, or the service itself. Missing prices stay unknown.

Saying “done” records that you reported cancelling. A confirmation email is separate evidence that the cancellation went through. The skill does not track usage, sign in, cancel, or pay for you.

## Files

- `SKILL.md`: the workflow Cubbie follows.
- `scripts/trials.py`: the saved list and date calculations; Python 3, with no third-party packages.
- `references/billing-routes.md`: cancellation and student-discount links.

[Full behavior and examples](GUIDE.md)
