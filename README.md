# ionic-messages

It includes a message interface compatible with Ionic.

![Logo](https://i.ibb.co/RgKfkYT/Simulator-Screenshot-i-Phone-14-Plus-2023-08-17-at-14-01-41.png)


## Installation

Install ion-messages with npm

```bash
  npm install @vatanay/ion-messages
```
    
## Usage/Examples

```html
<IonMessages :messages="messages"/>
```

```javascript
import IonMessages from "@/components/IonMessages.vue";

const messages = [{
  text: "Hello there!",
  sender: "me",
  avatar: "http://via.placeholder.com/360x360"
},{
  text: "Hi.",
  sender: "them",
  avatar: "http://via.placeholder.com/360x360"
}];
```


## Tech Stack

**Client:** Vue, Ionic


## Support

For support, email vatanayozbeyli@gmail.com or join our Slack channel.


## License

[MIT](https://choosealicense.com/licenses/mit/)


## Badges

Add badges from somewhere like: [shields.io](https://shields.io/)

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)