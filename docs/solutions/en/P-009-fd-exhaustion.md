# P-009. Hermes gateway exhausted its open-file limit

**Status:** recovery verified; the cause of file-descriptor growth remains unknown.

[Русский](../P-009-fd-exhaustion.md) · [Index](../../problem-index.en.md)

## Conditions and symptoms

On 28 May 2026, the Hermes gateway process on a Linux VPS approached its soft limit of 1,024 open file descriptors (FDs). The count had increased over approximately three days. The journal reported `sqlite3.OperationalError: unable to open database file` roughly once a minute: SQLite could not open related WAL/SHM files. Although this looked like a database-path error, measurements showed FD exhaustion. **The record does not establish why FDs accumulated.**

## How to check a similar failure

Identify the correct process PID and compare its open descriptors with its limits. These are read-only examples; substitute your own PID:

```sh
ls /proc/<PID>/fd | wc -l
cat /proc/<PID>/limits
```

For a systemd user service, check the limit actually received by the running process. A setting in a file alone is not proof that it took effect.

## Actions and verification

According to the incident receipt, the operator compared the FD count with the process limit, restarted the gateway, and set `LimitNOFILE=65536` for the systemd user service. The same limit was applied to a second gateway preventively; exhaustion on that second gateway was **not** established by this incident.

After restart the service was active and the FD count fell to about 32. A later check on the same day found 27 FDs and a successful model test. The SQLite error did not recur in the journal window inspected after the repair.

## Limits

Increasing the limit and restarting restored service, but did not fix a potential descriptor leak. If FD use grows monotonically again, identify the files or connections being left open rather than merely raising the limit. The record does not prove long-term stability or a specific code-level root cause.

## Evidence

Operational receipt and lesson dated 28 May 2026, recording FD counts, process limits, and the post-restart state. Private paths, addresses, configuration and full logs are not republished.
