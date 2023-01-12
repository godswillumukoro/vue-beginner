# Vue JS

## Benefits
- Create Dynamic Apps
- Tools for Code Organization
- Speed of Development
- Developer Tools
- Helps with scaling

## Features
- Virtual DOM
- Lightweight
- Progressive
- Vue Ecosystem
- Flexible
- Incrementally Adoptable

## Variables & Directives

```
<body>
    <main id="container" v-cloak>
        <h1>{{greet}} Vue</h1>

        <input type="text" name="" id="" v-model="greet">

        <div class="card" v-if="isVisible">
        </div>
        <div class="card2" v-else-if="isVisible2">
        </div>
        <div class="card3" v-else>
        </div>
    </main>

    <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

    <script>
        // 1. Create Vue Instance
        let app = Vue.createApp({
            data: () => {
                return {
                    greet: 'Hello',
                    yell: 'Hmm..',
                    isVisible2: true,
                }
            }
        })

        // 2. Connect Vue Instance to DOM element
        app.mount('#container')
    </script>
</body>
```

## Components
Breaking into sperate pieces.

```
        <h1>{{title}}</h1>
 

 app.component('loginform', {
            data() {
                return {
                    subtitle: 'Login to your dashboard here...'
                }
            },

            template: `
                 <p class="sm-txt">{{subtitle}}</p>
                 <form @submit.prevent="handleSubmission" action="" class="flex mg-block">
                    <input v-model="name" type="text" placeholder="Name">
                    <input v-model="email" type="email" placeholder="Email">
                    <input v-model="password" type="password" placeholder="Password">
                    <input type="submit" value="Login" class="btn">
                </form
            `, //v-model allows me access the inputted data

            methods: {
                handleSubmission() {
                    console.log({
                        name: this.name,
                        email: this.email,
                        password: this.password,
                    })
                }
            }
        })
```

## LifeCycle Hooks
A hook is a function that will be triggered to run at a specific point in the lifecycle of a component.

Used to:
- Check if user is authorized
- Pull data from API
- Initialize and remove events
- Save or Cleanup data from events