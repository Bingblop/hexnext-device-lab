# Hex Next device lab

Test jobs for the phone and the results it sends back. Private.

- `jobs/<id>.json`: a job. The phone runner (`tools/device/autotest.sh` in Hex-Next) runs each job once.
- `results/<id>/`: what the phone sent back: `status.json`, `shots/` (real screens and the app's preview of the same screens, `dark-real-qs.jpg` beside `dark-preview-qs.jpg`), `ui/` (view trees), `hook.jsonl`, and the `collect.sh` files.

Job fields: `id`, `ref` (Hex-Next branch for collect.sh), `run_id` + `artifact_sha256` (owner build to install), `steps` (install, theme, scan, apply, remove, capture, collect), `captures` (settings, qs, shade, power, myfiles, dialer), `modes` (dark, light), `theme` (a theme.json object), `confirm`.
