---

title: "Wishing and Musing: Web Sites"
description: ""
image:
video:
date: 2022-03-28

---

TODO: this needs to be updated to my current views which are much less graphQL-ish (?)

```
server
├── schemas
│   ├── Company.gql
│   ├── Employee.gql
│   └── Time.gql
├── resolvers
│   ├── Company.js
│   ├── Employee.js
│   └── Time.js
├── store
│   ├── company.js
│   ├── employee.js
│   └── time.js
└── package.json
```

```
client
├── queries
│   ├── Company.gql
│   ├── Employee.js
│   └── Time.js
├── views
│   ├── Company
│   │   ├── list.js
│   │   └── detail.js
│   ├── Employee
│   │   └── detail.js
│   └── Time
│       └── detail.js
├── public
│   ├── index.html
│   └── manifest.json
├── layout.json
├── theme.json
└── package.json
```

This seems pretty minimal compared to what I have seen so far.

Still, it seems redundant across server/client.  Even then, it's redundant within both of these.  But maybe this is not without call.

### reference
- [ascii tree generator](https://tree.nathanfriend.io/)
