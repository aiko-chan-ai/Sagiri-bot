# API Endpoint
- Base URL: <strong>https://sagiri-fansub.tk/api/v1</strong>
## Girl Image
- Endpoint: <strong>/girl</strong>
- Method: <strong>GET</strong>
- Authorization: <strong>False</strong>
- Param: <strong>No</strong>
- Description: Lấy ảnh gái random từ Database
<details>
<summary><strong>Axios NodeJS Demo</strong></summary>

Code:
```js
const axios = require('axios');
const res = axios
	.get('https://sagiri-fansub.tk/api/v1/girl')
	.then((res) => console.log(res.data))
	.catch((e) => console.log(e));
```
Response
```js
{
  msg: 'API by Shiraori#1782',
  code: 200,
  data: {
    authorName: 'test-v2',
    authorId: '895296229821542451',
    messageId: '915913485785915402',
    messageUrl: 'https://discord.com/channels/820557032016969748/915903029276971008/915913485785915402',
    proxyUrl: 'https://media.discordapp.net/attachments/915903029276971008/915913485580386314/201.jpg'
  }
}
```

<strong>Image Demo</strong>

<img src='https://media.discordapp.net/attachments/915903029276971008/915913485580386314/201.jpg'>
</details>

## Discord User Info
- Endpoint: <strong>/userinfo</strong>
- Method: <strong>GET</strong>
- Authorization: <strong>True</strong>
- Param: <strong>UserID</strong>
- Description: Lấy thông tin người dùng Discord khá đầy đủ (Nitro, Connected Accounts, Bio, ...)
- Note: DMs tôi trên Discord [Shiraori#1782] để lấy token
<details>
<summary><strong>Axios NodeJS Demo</strong></summary>

Code:
```js
const axios = require('axios');
axios
    .get(
        'https://sagiri-fansub.tk/api/v1/userinfo/721746046543331449', {
            headers: {
                Authorization: 'Token',
            },
    })
	.then((res) => console.log(res.data))
	.catch((e) => console.log(e));
```
Response
```js
{
  msg: 'Success',
  code: 200,
  data: {
    id: '721746046543331449',
    bot: false,
    system: false,
    flags: [ 'HOUSE_BALANCE' ],
    username: 'Shiraori',
    discriminator: '1782',
    avatar: 'f9ba7fb35b223e5f1a12eb910faa40c2',
    banner: null,
    accentColor: null,
    bio: '**Owner bot Sagiri#3948**\n' +
      '<a:counting:857071204330635265><t:1653757200:R> 🎂\n' +
      '<:bot:943941834365890690> https://sagiri-fansub.tk\n' +
      '<a:kanna_hamom:912296822939193374>`aiko.dev@mail.nezukobot.vn`',
    connected_accounts: [ [Object], [Object], [Object] ],
    premium_since: 1623357181151,
    premium_guild_since: null,
    createdTimestamp: 1592148066889,
    defaultAvatarURL: 'https://cdn.discordapp.com/embed/avatars/2.png',
    hexAccentColor: null,
    tag: 'Shiraori#1782',
    avatarURL: 'https://cdn.discordapp.com/avatars/721746046543331449/f9ba7fb35b223e5f1a12eb910faa40c2.webp',
    displayAvatarURL: 'https://cdn.discordapp.com/avatars/721746046543331449/f9ba7fb35b223e5f1a12eb910faa40c2.webp',
    bannerURL: null
  },
  metadata: true
}
```
</details>

## Discord.js Documentation
- Endpoint: <strong>/djsdoc</strong>
- Method: <strong>GET</strong>
- Authorization: <strong>False</strong>
- Param: <strong>No</strong>
- Query1: <strong>type</strong> | Not required
- Query2: <strong>keyword</strong> | Required
- Description: Lấy 1 Embed về Discord.js Doc [Đã format để gửi trực tiếp]
<details>
<summary><strong>Axios NodeJS Demo</strong></summary>

Code:
```js
const axios = require('axios');
// Type: stable | main
axios
    .get('https://sagiri-fansub.tk/api/v1/djsdoc?type=stable&keyword=error')
	.then((res) => console.log(res.data))
	.catch((e) => console.log(e));
```
Response
```js
{
  msg: 'Success',
  code: 200,
  data: {
    title: 'Search results:',
    type: 'rich',
    description: ':regional_indicator_e: **[Client#error](https://discord.js.org/#/docs/discord.js/stable/class/Client?scrollTo=e-error)**\n' +
      ':regional_indicator_t: **[APIError](https://discord.js.org/#/docs/discord.js/stable/typedef/APIError)**\n' +
      ':regional_indicator_c: **[HTTPError](https://discord.js.org/#/docs/discord.js/stable/class/HTTPError)**\n' +
      ':regional_indicator_t: **[HTTPErrorData](https://discord.js.org/#/docs/discord.js/stable/typedef/HTTPErrorData)**\n' +
      ':regional_indicator_t: **[MakeErrorOptions](https://discord.js.org/#/docs/discord.js/stable/typedef/MakeErrorOptions)**\n' +
      ':regional_indicator_m: **[WebSocketShard#onError()](https://discord.js.org/#/docs/discord.js/stable/class/WebSocketShard?scrollTo=onError)**\n' +
      ':regional_indicator_m: **[Util.makeError()](https://discord.js.org/#/docs/discord.js/stable/class/Util?scrollTo=s-makeError)**\n' +
      ':regional_indicator_e: **[Client#shardError](https://discord.js.org/#/docs/discord.js/stable/class/Client?scrollTo=e-shardError)**\n' +
      ':regional_indicator_m: **[DiscordAPIError.flattenErrors()](https://discord.js.org/#/docs/discord.js/stable/class/DiscordAPIError?scrollTo=s-flattenErrors)**\n' +
      ':regional_indicator_c: **[RateLimitError](https://discord.js.org/#/docs/discord.js/stable/class/RateLimitError)**',
    url: null,
    timestamp: '2022-03-20T18:21:20.702Z',
    color: 2266867,
    fields: [],
    thumbnail: null,
    image: null,
    author: {
      name: 'Discord.js Docs',
      url: 'https://discord.js.org/#/docs/discord.js/stable/general/welcome',
      icon_url: 'https://discord.js.org/favicon.ico'
    },
    footer: {
      text: 'API by Shiraori#1782',
      icon_url: 'https://cdn.discordapp.com/avatars/817229550684471297/9a1e752bcd271e333d09c6235713a9bf.webp'
    }
  }
}
```

<strong>Demo</strong>

<img src='https://cdn.discordapp.com/attachments/820557032016969751/955169519905701918/unknown.png'>
</details>

