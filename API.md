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
- Param: <strong>Keyword</strong>
- Description: Lấy 1 Embed về Discord.js Doc [Đã format để gửi trực tiếp]
<details>
<summary><strong>Axios NodeJS Demo</strong></summary>

Code:
```js
const axios = require('axios');
axios
    .get('https://sagiri-fansub.tk/api/v1/djsdoc/error')
	.then((res) => console.log(res.data))
	.catch((e) => console.log(e));
```
Response
```js
{
  msg: 'Lấy data thành công',
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

## Discord Video Embed
- Endpoint: <strong>/embed</strong>
- Method: <strong>POST</strong>
- Authorization: <strong>False</strong>
- Param: <strong>No</strong>
- Description: Tạo 1 URL Embed chứa Video gửi trên Discord
<details>
<summary><strong>Axios NodeJS Demo</strong></summary>

Code:
```js
// Youtube URL
const axios = require('axios');
axios
	.post('https://sagiri-fansub.tk/api/v1/embed', {
		provider: 'Created by Shiraori#1782', // Gần giống Author nhưng nhỏ hơn
		hexColor: '#00ff60', // Màu của Embed, sử dụng Hex
		url: 'https://sagiri-fansub.tk/', // URL ở Title 
		description: 'Mô tả cho embed. Thế thôi :))', // Mô tả cho embed nhưng sẽ bị ẩn do có Video
		title: 'Embed Video demo 🆘', // Embed.title
		thumbnail: undefined, // Embed.thumbnail | Thumbnail Video (Youtube Video không dùng Thumbnail tùy chỉnh)
		video: 'DKnPz7hI25A', // Youtube Video ID
		youtube: true, // True nếu là video Youtube
		redirect: 'https://www.youtube.com/watch?v=dQw4w9WgXcQ', // URL chuyển hướng [Tức là ấn vào link sẽ chuyển sang URL đó]
	})
	.then((res) => console.log(res.data))
	.catch((e) => console.log(e));
// Video URL
const axios = require('axios');
axios
	.post('https://sagiri-fansub.tk/api/v1/embed', {
		provider: 'Created by Shiraori#1782', // Gần giống Author nhưng nhỏ hơn
		hexColor: '#00ff60', // Màu của Embed, sử dụng Hex
		url: 'https://sagiri-fansub.tk/', // URL ở Title 
		description: 'Mô tả cho embed. Thế thôi :))', // Mô tả cho embed nhưng sẽ bị ẩn do có Video
		title: 'Embed Video demo 🆘', // Embed.title
		thumbnail: 'https://media.discordapp.net/attachments/820557032016969751/952602124942991400/17dc8587e135073e0.png', // Embed.thumbnail | Thumbnail Video
		video: 'https://cdn.discordapp.com/attachments/877060758092021801/955153180075913276/demo.mp4', // Video URL
		youtube: false, // True nếu là video Youtube
		redirect: 'https://www.youtube.com/watch?v=dQw4w9WgXcQ', // URL chuyển hướng [Tức là ấn vào link sẽ chuyển sang URL đó]
	})
	.then((res) => console.log(res.data))
	.catch((e) => console.log(e));
/**
 * Note: Cái nào không dùng thì bỏ đi hoặc đặt value là undefined
 * Nếu Video trên Discord phải dùng cdn.discordapp.com, không dùng proxyURL
 * Dùng tới khi bot bị reset nhé
*/
```
Response
```js
{
	msg: `URL của bạn được tạo thành công
Cách dùng: {baseURL}/api/v1/embed/JfJ1kUG7
Dùng tới khi bot bị reset nhé`,
	path: 'JfJ1kUG7',
	code: 200,
}
```
Using
```js
https://sagiri-fansub.tk/api/v1/embed/JfJ1kUG7
```
<strong>Demo</strong>
<details>
<summary>Video URL Thumbnail</summary>
<img src='https://cdn.discordapp.com/attachments/820557032016969751/955173877158383727/unknown.png'>
</details>
<details>
<summary>Video URL Playing</summary>
<img src='https://cdn.discordapp.com/attachments/820557032016969751/955174021236944926/unknown.png'>
</details>
<details>
<summary>Youtube Video Thumbnail</summary>
<img src='https://cdn.discordapp.com/attachments/820557032016969751/955175251053015070/unknown.png'>
</details>
<details>
<summary>Youtube Video Playing</summary>
<img src='https://cdn.discordapp.com/attachments/820557032016969751/955175375896461402/unknown.png'>
</details>
</details>

