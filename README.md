# scoreboard

The lab's beacon collector.

Every beacon from the workshop org lands here as a GitHub
`repository_dispatch` event with `event_type: beacon` and a `client_payload`
carrying `team`, `kind`, `secret`, `workflow`, and sometimes `detail`.

The workflow in `.github/workflows/scoreboard.yml` appends one row to
`HITS.md` and commits it. Watch the file, or its commit history, to see hits
accumulate in near real time:

- File: <https://github.com/devcon-dutralab/scoreboard/blob/main/HITS.md>
- History: <https://github.com/devcon-dutralab/scoreboard/commits/main/HITS.md>

The repo is private; only the org's own workflows write to it. Every secret
that reaches it is fake by design.
