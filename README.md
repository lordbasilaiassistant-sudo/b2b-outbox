# b2b-outbox

Hand-off: the daily routine (can reach github.com, NOT workers.dev) pushes
`pending/<slug>.mp4` + `pending/<slug>.json` and appends the slug to `manifest.json`;
the yt-relay Worker cron (*/30) uploads each slug exactly once (KV done-set).
PUBLIC by design: contents are public on YouTube minutes later. Nothing sensitive, ever.
