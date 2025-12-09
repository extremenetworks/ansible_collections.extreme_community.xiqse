# Integration Tests

These smoke tests exercise the collection against a live XIQ-SE instance.

Set the following environment variables before running:

- `XIQSE_HOST`
- `XIQSE_CLIENT_ID`
- `XIQSE_CLIENT_SECRET`

Run:

```bash
ansible-playbook tests/integration/test_query.yml
```

If the environment variables are not set, tests will be skipped gracefully.
