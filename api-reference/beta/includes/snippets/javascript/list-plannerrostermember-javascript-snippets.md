---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let res = await client.api('/planner/rosters/6519868f-868f-6519-8f86-19658f861965/members')
	.version('beta')
	.get();

```