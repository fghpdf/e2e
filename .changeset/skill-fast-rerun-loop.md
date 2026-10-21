---
"e2e": patch
---

The bundled agent skill now gives a coding agent a fast loop for fixing a test: rerun only that test by `file:line`, keep the replay cache on so goals that passed replay without model calls, add `--retries 0` when the config sets retries, don't rename the test or reword a passing goal mid-loop, and run with `--no-cache` one time once the test passes. The coding agents guide no longer tells agents to add `--no-cache` after every change, and the caching guide has a section on rerunning a test while you fix it.
