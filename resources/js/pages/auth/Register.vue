<template>
    <fwb-card class="p-4">
        <fwb-heading class="text-center" tag="h3"> Register Form </fwb-heading>
        <form @submit.prevent="submit">
            <fwb-input
                v-model="form.name"
                label="Name"
                placeholder="enter your first name"
                size="sm"
            />
            <fwb-input
                v-model="form.email"
                label="Email"
                placeholder="enter your email"
                size="sm"
            />
            <fwb-input
                v-model="form.password"
                label="Password"
                placeholder="enter your password"
                size="sm"
            />
            <fwb-input
                v-model="form.password_confirmation"
                label="Confirm Password"
                placeholder="enter your password again"
                size="sm"
            />
            <div class="p-2 text-sm flex gap-1">
                <p class="">Already have an account?</p>
                <Link class="text-blue-600">Login</Link>
            </div>
            <fwb-button type="submit">
            Register
            </fwb-button>
        </form>
    </fwb-card>
</template>

<script setup>
import { reactive } from "vue";
import Layout from "../../layouts/GuestLayout.vue";
import { FwbCard, FwbInput, FwbHeading, FwbButton } from "flowbite-vue";

const form = reactive({
    name: "",
    email:"",
    password:"",
    password_confirmation:""
})

function submit(){
    console.log(form)
}

defineOptions({
    layout: Layout,
});
</script>
