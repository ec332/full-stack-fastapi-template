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

- `test_tc_o7_1.py` (O-7): TC-O7-1
- `test_tc_o7_2.py` (O-7): TC-O7-2
- `test_tc_o7_3.py` (O-7): TC-O7-3

## Tests

| File | Priority | Requirement | Purpose |
|---|---|---|---|
| `test_tc_o7_1.py` | P0 | O-7 | PUT with a null title is refused with 422 |
| `test_tc_o7_2.py` | P0 | O-7 | A null title does not cause a server error |
| `test_tc_o7_3.py` | P0 | O-7 | A rejected null-title PUT leaves the item unchanged |
