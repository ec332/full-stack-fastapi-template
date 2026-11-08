# Generated tests (test platform run r-0037)

Generated from approved test cases and checked against commit `d53d779`:
each was run several times, in shuffled order, and against planted code changes.

## Run them

```bash
docker compose up -d db   # the same database the repo's own tests use
cd backend && pytest tests/generated
```

Each test runs inside a database transaction that is rolled back afterwards.
`_support/` holds the runtime the tests use (`platform_rt`, the data factories).

## Expected to fail until a defect is fixed

- `test_tc_o5_1.py` (O-5): TC-O5-1.3
- `test_tc_o5_2.py` (O-5): TC-O5-2
- `test_tc_o5_3.py` (O-5): TC-O5-3
- `test_tc_o5_4.py` (O-5): TC-O5-4

## Tests

| File | Priority | Requirement | Purpose |
|---|---|---|---|
| `test_tc_o5_1.py` | P0 | O-5 | caller × action |
| `test_tc_o5_2.py` | P0 | O-5 | A non-owner ordinary user cannot update another user's item |
| `test_tc_o5_3.py` | P0 | O-5 | A non-owner PUT is refused with 403, not hidden as 404 |
| `test_tc_o5_4.py` | P0 | O-5 | A refused non-owner PUT leaves the item unchanged |
