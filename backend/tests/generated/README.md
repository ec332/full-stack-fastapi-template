# Generated tests (test platform run r-0001)

Generated from approved test cases and checked against commit `6838b40`:
each was run several times, in shuffled order, and against planted code changes.

## Run them

```bash
docker compose up -d db   # the same database the repo's own tests use
cd backend && pytest tests/generated
```

Each test runs inside a database transaction that is rolled back afterwards.
`_support/` holds the runtime the tests use (`platform_rt`, the data factories).

## Expected to fail until a defect is fixed

- `test_tc_o5_1.py` (O-5): TC-O5-1

## Tests

| File | Priority | Requirement | Purpose |
|---|---|---|---|
| `test_tc_o1_2.py` | P1 | O-1 | Create item and check final_price is the exact discounted value |
| `test_tc_o5_1.py` | P1 | O-5 | Discount 99 accepted and final_price is exact |
| `test_tc_o5_2.py` | P1 | O-5 | discount_percent at the 0 limit |
| `test_tc_o5_3.py` | P1 | O-5 | Discount 100 refused with 422 and no item created |
| `test_tc_o5_4.py` | P1 | O-5 | Negative discount refused with 422 |
