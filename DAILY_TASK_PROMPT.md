# The daily scheduled task

Paste the text between the lines as the prompt of the scheduled task in Claude Code
on the web. Set it to run every day at 7:00 AM, Central time.

---

Read CLAUDE.md first, then everything in companion/, then the last five files in
letters/. You are writing today's letter for Vienna, a six-year-old, following
CLAUDE.md exactly.

1. Find today's date: `TZ=America/Chicago date +%F`.
2. If `letters/<today>.json` already exists on `main`, stop. Today's letter is there.
3. Write today's letter following "How to write" in CLAUDE.md: three to five
   sentences at a second-grade reading level, cheerful, praising effort, different
   from the last five.
4. Check every line against the "Always" and "Never" lists in CLAUDE.md. Rewrite any
   line that fails.
5. Create `letters/<today>.json` in the format shown in CLAUDE.md, with `"time"` set
   to `"07:00"` and `"from"` set to `"Claude"`.
6. Add `"<today>"` to the list in `letters/index.json`.
7. Commit on a branch named `letter/<today>` with the message `a letter for <today>`,
   push it, open a pull request to `main`, and merge it. If merging is not possible,
   push directly to `main`.
8. If the push is refused, write what happened to `letters/notes.md` and stop. Don't
   retry more than twice.

Nobody is reading this conversation. Don't ask questions. Just leave the letter.

---

If the push is refused (403): in Claude Code on the web, Settings → Environments →
your environment → repositories, and make sure `love-letters` is listed under its
exact name.
