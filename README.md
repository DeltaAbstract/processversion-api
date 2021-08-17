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
| `user`   | `String` | `Yes`    |
| `apikey` | `String` | `No`     |

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

### /roblox

#### Params

| Name       | Type     | Required |
| ---------- | -------- | -------- |
| `username` | `String` | `Yes`    |
| `key`      | `String` | `No`     |

#### Example response

- 200

```json
{
	"success": true,
	"status": 200,
	"statusMessage": "OK",
	"data": {
		"isBanned": false,
		"username": "ProcessVersion",
		"pastNames": ["Techmaster10050", "Techmxster"],
		"bio": "If I'm playing there's a 100% chance I'm mining cryptocurrency and looking for something fun that doesn't require my attention (like simulators and tycoons). I'm usually listening to music or watching a video while doing so. Feel free to join if you want.\n\n\n If you need to contact me for whatever reason, tag is ProcessVersion # 4 4 7 2",
		"age": "1,898",
		"joinDate": "2016-05-12T20:44:51.263Z",
		"friends": 49,
		"following": "33",
		"followers": "1,460",
		"profile_url": "https://roblox.com/users/126486392/profile",
		"thumbnail": "https://www.roblox.com/bust-thumbnail/image?userId=126486392&width=420&height=420&format=png"
	}
}
```

#### Example request

- Node JS (Javascript/Typescript) - AXIOS

```js
// WITH AXIOS
const axios = require('axios');
// TS: import axios from "axios";

const res = await axios.get(
	`https://processversion.herokuapp.com/reddit?user=techmxster&key=KEY_HERE`
);
const data = res.data;

/*
WITH HEADERS
*/

const res = await axios.get(
	`https://processversion.herokuapp.com/roblox?username=processversion`,
	{ headers: { Authorization: 'KEY HERE' } }
);
const data = res.data;
```

### /subreddit

### /user
