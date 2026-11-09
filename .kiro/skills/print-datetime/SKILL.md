---
name: print-datetime
description: Prints today's date and current time. Use when the user asks for the current date, time, or timestamp.
---

# Print Date and Time

When this skill is activated, report the current local date and time.

## Steps

1. Run the command below with the shell tool. Do not rely on memory or guess the time.

   PowerShell (Windows):
   ```powershell
   Get-Date -Format "dddd, MMMM d, yyyy HH:mm:ss (zzz)"
   ```

   Bash (macOS/Linux):
   ```bash
   date "+%A, %B %-d, %Y %H:%M:%S (%:z)"
   ```

2. Reply with the output in one short line, for example:

   `Today is Monday, November 9, 2026, 14:35:07 (+08:00)`

## Notes

- Use the local time zone unless the user asks for another one (e.g. UTC via `(Get-Date).ToUniversalTime()` or `date -u`).
- If the user asks for a different format, adjust the format string accordingly.
