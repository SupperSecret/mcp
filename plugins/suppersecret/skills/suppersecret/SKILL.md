---
name: suppersecret
description: Use when the user asks about their household's dinners, meal plan, recipes, pantry, shopping list, leftovers, who is eating when, or inviting someone to dinner, and the SupperSecret tools are connected.
---

# Planning dinner with SupperSecret

The SupperSecret tools act on one household: the one the user chose when they
connected. Every tool call reads or changes that household's real plan, which
other people in the family see on their phones. The server sends fuller
instructions when it connects; these are the points that matter most.

## Before changing anything

- Read first. `today`, `week`, `dishes`, `staples`, `list`, `leftovers` and
  `people` change nothing, so look before you act.
- Names are enough: a tool that takes a dish, person, staple or leftover
  accepts its name, its id, or a unique part of its name.
- Days are an ISO date, "today", or a weekday (this week). Tools that work on
  any night also take a date in any week.

## Things that are easy to get wrong

- **Allergies rule a dish out; dislikes are picked around.** Never treat them
  as the same thing.
- **A shelf or freezer photo is a count of what is there, not a delivery.**
  Read `staples` and set each item to what is shown.
- **"Low" is not a number** for a counted item. Ask how many.
- **Import recipes with `add_dish` and the recipe's text.** Check `dishes`,
  `staples` and `jobs` first so nothing is duplicated.
- **Use `fill`, not `regenerate`.** Regenerating throws away swaps people
  made; ask before doing it.
- **Lasting household facts go in `remember`** ("we buy carrots loose"), not
  in a single night's note.

## Inviting a dinner guest

`invite_guest` makes a link for one night, with an optional note. Give the
user the link to send; the guest sees the menu and replies with whether they
are coming and what they can't eat, and a yes puts them on that night. Use
`guest_replies` to see who answered.

## What you can't do

Deleting dishes or people, resetting data and backups are done by people in
the app. Retiring a dish (`set_dish` with `retired`) is usually what was
wanted.
