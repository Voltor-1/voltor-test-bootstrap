## [Issue title]

**Agent:** builder
**Priority:** [P1 / P2 / P3]
**Depends on:** [issue number or "none"]

### Context
[2-5 sentences: what this issue implements, why it exists, how it fits the design.
Must be specific enough that a developer with no codebase context understands the purpose.]

### Stack Context
[Technology decisions this issue must conform to: library versions, framework patterns,
naming conventions, existing interfaces to extend or depend on.
Example: hono@4, @supabase/supabase-js@2, Zod validation on all inputs,
getAnonClient() from src/lib/supabase.ts, ok()/err() response helpers from src/lib/response.ts]

### Local Path
[Exact absolute path — no ~ expansion]
/home/scott/.openclaw/workspaces/builder_engineer/[product]

### Session Orientation
```bash
cd /home/scott/.openclaw/workspaces/builder_engineer/[product]
git checkout main && git pull origin main
git checkout -b feature/[issue-number]-[short-description]
```

### Files
- path: [relative path from repo root]
  action: create | modify | delete
  purpose: [one sentence]
  content_notes: [what must be in this file — types, functions, exports]

- path: [relative path]
  action: create | modify | delete
  purpose: [one sentence]
  content_notes: [what must be in this file]

### Interfaces
[Complete TypeScript types, SQL schemas, Zod schemas, or API contracts
for every new interface introduced. In the target language of the implementation.]

```typescript
// Example:
export interface ExampleRequest {
  field: string;
  amountCents: number;
}

export interface ExampleResponse {
  id: string;
  field: string;
}
```

### Implementation Notes
[Non-obvious logic, algorithm descriptions, worked examples, library usage patterns.
If logic is straightforward, write: "Implementation is straightforward — no non-obvious logic."
Never leave empty. Address: monetary rounding, error handling, RLS constraints, reusable patterns.]

### Commands
```bash
# All implementation commands in one block
# File writes, git operations, test runs, curl validations

cat > src/routes/[file].ts << 'TSEOF'
[file content]
TSEOF

cd /home/scott/.openclaw/workspaces/builder_engineer/[product]
git add src/routes/[file].ts
git commit -m "[#issue-number] short description"
git push origin feature/[issue-number]-[short-description]
```

### Success Checks
```bash
# Commands that must all exit 0 for the issue to be complete
curl -s https://[worker-url]/[endpoint] | grep -q "expected_value"
npm test -- --testPathPattern=[test-file]
```

### Acceptance Criteria
1. [Explicit, testable condition — e.g. GET /endpoint returns HTTP 200]
2. [Explicit, testable condition]
3. [Explicit, testable condition — minimum 3 required]

### Exec Call Count
[Positive integer — count of shell exec calls in Commands block]
