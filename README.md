# ProcessVersion-API

## Documentation for the API

## Base URL: https://processversion.herokuapp.com/

**ALL API ENDPOINTS REQUIRE A KEY. There are _2_ ways of doing so**

1. Authorization header
2. Query (?apikey=key)

### /reddit - URL https://processversion.herokuapp.com/reddit

#### Params

| Name     | Type     | Required |
| -------- | -------- | -------- |
| `user`   | `string` | `Yes`    |
| `apikey` | `string` | `No`     |

#### Example response

- 200

```json
{
	"success": true,
	"status": 200,
	"statusMessage": "OK",
	"data": {
		"url": "https://reddit.com/user/Techmxster/",
		"name": "Techmxster",
		"name_prefixed": "u/Techmxster",
		"id": "5866fa74",
		"pfp": "https://styles.redditmedia.com/t5_2ah0o4/styles/profileIcon_uVPfocfhcj-3k.png?width=256&height=256&crop=256:256,smart&s=f86197ae0711f93e1690ab5b92c9a8e5b4e1d16c",
		"verified": true,
		"created": "Sunday, December 15th 2019, 7:56:54 am",
		"total_karma": "309",
		"link_karma": "5",
		"awarder_karma": 6,
		"awardee_karma": 0,
		"mod": false,
		"gold": false,
		"employee": false
	}
}
```

#### Example request

- Javascript / Typescript (axios)

```js
const axios = require('axios');
// TS: import axios from axios;

const res = await axios.get(
	`https://processversion.herokuapp.com/reddit?user=techmxster&apikey=key`
);
const data = res.data;

/*
 With headers
*/

const axios = require('axios');
// TS: import axios from "axios";

const res = await axios.get(
	`https://processversion.herokuapp.com/reddit?user=techmxster`,
	{ headers: { Authorization: 'KEY HERE' } }
);
const data = res.data;
```

- Javascript / Typescript (node-fetch)

```js
const fetch = require('node-fetch');
// TS:  import fetch from fetch;

const res = await fetch(
	`https://processversion.herokuapp.com/reddit?user=techmxster&apikey=key`
);
const data = await res.json();

/*
 With headers
*/

const fetch = require('node-fetch');
// TS: import fetch from fetch;

const res = await fetch(
	`https://processversion.herokuapp.com/reddit?user=techmxster`
);
const data = await res.json();
```
