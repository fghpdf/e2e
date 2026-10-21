---
"e2e": patch
---

The bundled agent skill now keeps an `e2e mcp` session open between test runs while the agent writes or fixes a test on the web, so a live look after a failed run is one `observe` instead of a walk through the flow from the start. It says when a run can share the app with the session: no `app.command`, a port-0 URL, or `reuseExisting: true` on a fixed port. A fixed port without `reuseExisting` makes a run beside the session fail with `APP_ALREADY_RUNNING`, so the agent offers `reuseExisting: true` to the user instead of adding it, and closes the session before each run until then. With `CI` set, it unsets `CI` for the run or closes the session. On mobile it still closes the session before a run, or opens it on a target with a device of its own. The MCP server page shows the same cases as a table.
