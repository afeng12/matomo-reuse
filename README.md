## Matomo Plugin for UniApp

This [Matomo](https://www.matomo.org) plugin is designed for [UniApp](https://uniapp.dcloud.io).

### Installation

```bash
npm install matomo-reuse
```

### Usage

```javascript
import { createApp } from 'vue'
import VueMatomo from 'matomo-reuse'
import App from './App.vue'

createApp(App)
    .use(VueMatomo, {
        // Configure your matomo server and site by providing
        host: '{YOUR_MATOMO_INSTANCE_URL}',
        siteId: {YOUR_SITE_ID},
    })
    .mount('#app')

//type:event type, action:event behavior, name:event name
VueMatomo.trackEvent(type,aciton,name);
//When the user logs in, set the user ID.
VueMatomo.setUserId('example-user-id');
```

### API

#### `new Matomo(options)`

- `options` (Object):
  - `url` (String): The URL of your Matomo instance.
  - `siteId` (Number): The ID of the site you want to track.

#### `matomo.setUserId(userId)`
- `userId` (String): Defines the User ID for this request. The User ID is any non-empty unique string identifying the user (such as an email address or a username).

### License

[MIT License](https://opensource.org/licenses/MIT)

### Keywords

[matomo](https://www.npmjs.com/search?q=matomo), [uniapp](https://www.npmjs.com/search?q=uniapp)
