<div align="center">
<img src="https://raw.githubusercontent.com/uNetworking/uWebSockets/master/misc/logo.svg" height="180" /><br>

</div>
<br>


We aren't in the NPM registry but you can easily install it with the NPM client:
* `npm install uNetworking/uWebSockets.js#v20.48.0`

### :dart: In essence
```
// npm install uNetworking/uWebSockets.js#latest package.json->type:module
import uWS from 'uWebSockets.js';
```

### The right approach
Don't use require, because you can only use it now. When you cooperate with other libraries, you will lose the Promise and fall into an infinite loop in res.onAbortd res.cork

```
// npm install uNetworking/uWebSockets.js#latest package.json->type:module
import uWS from 'uWebSockets.js';
const port = 9001;

const redis = require('redis');
import { createClient } from 'redis';
const useRedis = createClient();
useRedis.connect(); 
```

![image](https://github.com/user-attachments/assets/0c34f84f-7f04-45b9-a559-a8af2a2e59e2)
