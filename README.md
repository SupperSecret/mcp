# SupperSecret for Claude Code

Plan your household's dinners from Claude Code: the week, recipes, pantry,
shopping list, leftovers and dinner guests, in your
[SupperSecret](https://suppersecret.com) household.

## Install

```bash
claude plugin marketplace add suppersecret/mcp
claude plugin install suppersecret@suppersecret
```

Then, in a Claude Code session, run `/mcp`, pick **suppersecret**, and choose
**Authenticate**. Your browser opens SupperSecret: sign in, choose which
household Claude may use, and tap **Allow**.

You need a SupperSecret account in a household. During the beta, households
join by invitation.

## What it can do

The same things as the assistant in the SupperSecret app, in the one household
you approved: read and change the week's dinners, import recipes, keep the
pantry and shopping list, record leftovers, and invite someone to dinner.
It can't delete dishes or people, reset anything, or reach any other
household.

Disconnect any time from **Connected AI apps** in SupperSecret's menu, or with
`claude plugin uninstall suppersecret`.

## What's in here

- `.claude-plugin/marketplace.json`: the marketplace, listing one plugin.
- `plugins/suppersecret/.mcp.json`: the connector, pointing at
  `https://suppersecret.app/mcp`.
- `plugins/suppersecret/skills/suppersecret/`: notes that help Claude use the
  planner well.

No credentials live here: signing in happens in your browser, against
SupperSecret, when you authenticate.

## License

MIT. See [LICENSE](LICENSE).
