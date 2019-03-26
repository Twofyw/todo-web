<template>
    <section class="main-content">
        <div class="container">
            <div class="row">

                <div class="col-md-12">


                    <h1><strong>Home</strong></h1>

                    <p>Here will be a check to see if you are currently logged in and your user info.</p>

                    <p v-if="user"><i class="fa fa-user fa-fw"></i>  You: {{user}}</p>
                    <p v-else>Hmm, you are not logged in.</p>

                    <p>
                        <a href="https://github.com/Twofyw?tab=followers" target="_blank"><img src="https://img.shields.io/github/followers/Naereen.svg?style=social&label=Follow&maxAge=2592000" alt=""></a>
                    </p>
                </div>

            </div>
        </div>
    </section>
</template>

<script>
import { mapState } from 'vuex'

export default {
    name: 'home',
    computed: {
        ...mapState({
            user: state => state.user.user
        })
    },
    mounted () {
    }
}
</script>

<style lang="scss" scoped>
</style>
