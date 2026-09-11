# Linux — DevOps Interview Coding Practice

## Q1 — File + Directory + Permissions

Write Linux commands to create a directory `/app/logs`, create a file
`app.log` inside it, set permissions so the owner has read/write/execute,
the group has read/execute, and others have no access.

Change ownership to user `appuser` and group `appteam`.

---

## Q2 — Process Management

Write Linux commands to find a process running on port `8080`, check its PID,
view its resource usage, and kill it gracefully.

If it does not stop, force kill it.

---

## Q3 — Disk + Memory + CPU Monitoring

Write Linux commands to:

- Check disk usage of all mounted filesystems.
- Check memory usage.
- Check CPU load average.
- Find the top 5 processes consuming the most CPU.
- Find the top 5 processes consuming the most memory.

---

## Q4 — Log Investigation + grep + awk

Write Linux commands to:

- Search for all `ERROR` lines in `/var/log/app.log`.
- Count how many errors occurred.
- Extract only the timestamp and error message from each line using `awk`.
- Save the output to a new file.

---

## Q5 — User + Group Management

Write Linux commands to:

- Create a user `devops` with a home directory.
- Add the user to the `sudo` and `docker` groups.
- Set a password.
- Lock the account temporarily.
- Unlock the account again.

---

## Q6 — Networking + Troubleshooting

Write Linux commands to:

- Check all open ports.
- Check if port `443` is listening.
- Trace the network route to `google.com`.
- Check DNS resolution.
- View active network connections.

---

## Q7 — Cron Job + Scheduling

Write cron jobs that:

- Run `/usr/local/bin/backup.sh` every day at 2 AM.
- Run a log cleanup script every Sunday at midnight.
- Run a health check every 5 minutes.

Also show how to:

- View the crontab.
- Edit the crontab.

---

## Q8 — Systemd + Service Management

Write Linux commands to create a systemd service file for a Node.js
application.

The service should:

- Start automatically on boot.
- Start the application.
- Allow checking its status.
- Allow viewing logs using `journalctl`.
- Restart automatically if the application crashes.

---

## Q9 — Linux Architecture

Explain how the following Linux components work together:

```text
                 Linux Server
                      │
        ┌─────────────┼─────────────┐
        │             │             │
   Files & Dirs   Processes      Services
        │             │             │
   chmod/chown    ps/top/kill    systemctl
        │             │             │
        └─────────────┼─────────────┘
                      │
                 Log Files
                      │
                grep / awk / find
                      │
                 Cron Jobs
                  (Automation)
                      │
             Network Troubleshooting