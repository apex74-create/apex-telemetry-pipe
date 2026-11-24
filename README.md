# Apex Telemetry Pipe

The public pipe for the **Apex Widget Window**.

`telemetry.json` in this repo is the live factory tachometer record
(schema `apex-telemetry/1`): factory rpm, open/red PR counts, the sample
timestamp, and the main thread's weight gauges with their ledger date.

**Feed URL** (unauthenticated, poll-friendly):

    https://raw.githubusercontent.com/apex74-create/apex-telemetry-pipe/main/telemetry.json

The record is composed from the factory's own instruments — the Merge
Spindle's tach samples and the thread-weight ledger — and republished when
it changes (checked every 5 minutes; the tach itself samples every 10).
The same record is held privately in the house provenance repo; this repo
is its public pipe, and nothing else.

**Privacy posture:** operational telemetry only. No names, no locations,
no message content, no health data, no credentials — the pipe carries the
factory's gauges, nothing about any person.
