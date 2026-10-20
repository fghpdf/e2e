---
"e2e": patch
---

`tap_at` and `hover_at`, in `agent.act` and `e2e mcp`, now act on the bare point when the control under it has its center covered by another node and the engine takes a bare point. Before, a point outside an iOS popover snapped to the popover's full-screen dismiss region and tapped its center, inside the popover, so the popover stayed open.
