# Vue.js JWT Authentication with Vuex and Vue Router

For more detail, please visit:
> [Vue.js JWT Authentication with Vuex and Vue Router](https://bezkoder.com/jwt-vue-vuex-authentication/)

Fullstack with Spring Boot Back-end:
> [Spring Boot + Vue.js: Authentication with JWT & Spring Security Example](https://bezkoder.com/spring-boot-vue-js-authentication-jwt-spring-security/)

Fullstack with Node.js Express Back-end:
> [Node.js Express + Vue.js: JWT Authentication & Authorization example](https://bezkoder.com/node-express-vue-jwt-auth/)

## Note:
Open `src/services/auth-header.js` and modify `return` statement for appropriate back-end.

```js
export default function authHeader() {
  let user = JSON.parse(localStorage.getItem('user'));

  if (user && user.accessToken) {
    return { Authorization: 'Bearer ' + user.accessToken }; // for Spring Boot back-end
    // return { 'x-access-token': user.accessToken };       // for Node.js Express back-end
  } else {
    return {};
  }
}
```

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
