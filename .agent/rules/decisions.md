Rules enforced:
  1.  Hard-coded values / magic strings → must be constants or enums
  2.  No ternary / inline && conditionals inside JSX return blocks
  3.  No date libs (moment / date-fns) directly in component files
  4.  Type safety – no `any`, `unknown`, `@ts-ignore`, `as any`
  5.  Code complexity – no deeply nested ternaries
  6.  React Context architecture – only { state, data, actions } keys
  7.  Naming conventions – meaningful names, consistent across feature
  8.  useFormContext / react-hook-form must be removed
  9.  Redux-style file splitting (slices/reducers/actions) not allowed
  10. console.log ONLY allowed inside catch blocks; banned everywhere else
  11. Prettier formatting – trailing spaces, mixed quotes, semicolons
  12. Extra blank lines – more than 2 consecutive blank lines (ESLint rule)
  13. Import order – React first, then external, then internal/relative
  14. Reusable code candidates – identical/near-identical blocks across files
  15. Logic that belongs in a utils file, not in a component/context
  16. Repeated hard-coded string values that should be a shared enum/const
  17. Code-pattern inconsistency across the same feature
  18. File & variable naming consistency across a feature
  19. Frontend architecture – `pages` handle routing/data orchestration, `layouts` handle chrome, `components` are presentational, `hooks` and `api` encapsulate logic/IO.
  20. Frontend data fetching – all HTTP / WebSocket calls go through `api` or dedicated hooks; no raw `fetch` / `socket.io-client` or inline URLs in components.
  21. Backend layering – `routes` only parse input and call `services`; business logic lives in `services`; direct DB access only in `db`/repository modules.
  22. Validation at boundaries – all external input (HTTP, WebSocket, CSV, queues) is validated with `zod` (or equivalent) before business logic or DB.
  23. Multi-tenant safety – every tenant/org-scoped query must filter by tenant/org id; no unscoped queries over multi-tenant data.
  24. Configuration & secrets – all env-specific values come from config/env; no inline secrets, keys, connection strings, or hostnames in code.
  25. Background work – heavy/long-running tasks (CSV, emails, sandbox) must use queues/workers, not block HTTP request handlers.
  26. Error handling – errors are caught at the edge and mapped to a consistent response; logs never expose sensitive internals to clients.
  27. Auth & authorization – shared `auth` / `middleware` modules implement checks; no copy-pasted ad-hoc permission logic in routes/services.
  28. Real-time features – `socket.io` events use shared helpers and constants; no ad-hoc event names or payload shapes scattered in code.
  29. Testing expectations – critical business flows (auth, CSV, scoring, tenant boundaries) must have at least basic automated tests before major changes.
