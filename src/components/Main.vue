<template>
    <main class="main">
        <SecurityInfo />
        <Services />
        <Productive />
        <Testimonials />
        <Form />
    </main>
</template>

<script>
    import SecurityInfo from './SecurityInfo.vue'
    import Services from './Services.vue'
    import Productive from './Productive.vue'
    import Testimonials from './Testimonials.vue'
    import Form from './Form.vue'

    export default {
    name: "Main",
    components: {
        SecurityInfo,
        Services,
        Productive,
        Testimonials,
        Form
    }
}
</script>