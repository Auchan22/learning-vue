<template>
    <div>
        <h1>Hola, {{ user.name }}</h1>
        <ul>
            <li>Correo: {{ user.mail }}</li>
            <li>Edad: {{ user.age }}</li>
            <li>Estas Logeado?: {{ user.isLoggedIn }}</li>
        </ul>
    </div>
</template>

<script lang="ts">
import { User } from '@/interfaces/User';
import { defineComponent, PropType } from 'vue';

export default  defineComponent({
    name: "CustomComponent",
    props: {
        user: {type: Object as PropType<User>, required: true}
    },

})
</script>