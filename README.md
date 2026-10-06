# Trello REST API Testing with Postman

A Postman collection that tests the Trello REST API across the full lifecycle of boards, lists, cards and checklists. I built it as a hands-on API testing project to practice request chaining, variables, test scripts and verifying API state after every change.

## What it covers

| Resource | Operations tested |
|---|---|
| Board | Create, get, update, delete |
| List | Create, get, update, archive, unarchive |
| Card | Create, get, update, delete |
| Checklist | Create, get, update, delete |

- **26 requests** in total, in a logical order that follows a real user flow.
- **A follow-up GET request** after each create, update, archive and delete, to confirm the API state actually changed.
- **Variables (DRY principle)** for the base URL, board ID, API key and token, so each value is defined once and reused in every request.
- **Test scripts** that check the status code and the response body.

## Files

| File | Description |
|---|---|
| [trello-collection.json](trello-collection.json) | Postman collection (v2.1) |

## How to run

1. Create your own Trello API key and token at the Trello developer portal.
2. Open Postman and click **Import**, then select `trello-collection.json`.
3. Set the `key` and `token` variables to your own values.
4. Run the requests in order, or use the Collection Runner.

The key and token in this repository are placeholders. Never commit real credentials.

## What I learned

- Reusing IDs between requests by saving them in variables.
- Verifying changes with a GET request, and not trusting the response of the change request alone.
- Writing assertions for the status code and response body.
-----------------------------------
## Second project: ReqRes API Testing

A Postman collection with 15 requests for the ReqRes practice API, covering GET, POST, PUT, PATCH and DELETE.

- **Positive cases:** list users, single user, create, update, delayed response, register and login success.
- **Negative cases:** user not found, resource not found, register without a password, login without a password.
- **Variables and test scripts** for the status code and response body.

## Tools

Postman, Trello REST API
