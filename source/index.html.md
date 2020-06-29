---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - accounts
  - libraries
  - folders_and_collections
  - assets
  - uploading
  - errors

search: true
---

# Introduction

Welcome to the ChilliPharm API. You can use our API to access ChilliPharm API endpoints, which can get information on Accounts, Libraries and Assets and can also be used to create Assets.

You can view CURL examples in the dark area to the right.

# Authentication

> To authenticate, use the login endpoint:

```shell
curl -X POST "https://chillipharm.com/api/v1/login" -d '{"auth": {"email": "user@test.com", "password": "pa$$word"}}' -H "Content-Type: application/json"
```

> The above command returns JSON structured like this:

```json
  {
    "id": 1,
    "name": "Jane Doe",
    "email": "user@test.com",
    "token": "tNKJN8khgvscm86Zy5FPTAyBZqptD4WM-bGU5K9L8ZA"
  }
```

ChilliPharm uses short-term session tokens whose usage extends their expiry.

ChilliPharm expects for the session token to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
  You must replace <code>meowmeowmeow</code> with the session token.
</aside>

<aside class="notice">
  The token will expire after 1 hour of inactivity.
</aside>

A `401` error code will be returned in all of the following cases:
<ul>
  <li>email or password is incorrect</li>
  <li>email does not exist</li>
  <li>user is not activated</li>
  <li>user has been suspended</li>
  <li>email is temporarily <strong>locked out</strong></li>
</ul>

If authentication fails five consecutive times with the same email address within the space of two minutes, that email address will be temporarily <strong>locked out</strong> of the system (three minutes).

# Permissions & Authorisation

Before every API request the User is checked to see if they have access to the resource being requested and to see if they have the required permissions to carry out that action.

A `401` error code will be returned if this check fails.

All following actions will detail the required permissions.