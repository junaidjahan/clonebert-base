<template>
    <div class="d-flex justify-center py-7">
        <base-card class="pa-10 px-15 rounded darkgrey" flat max-width="600px">
            <div class="d-flex justify-space-between align-center">
                <div>
                    <h1 class="white--text" style="font-size:2.19rem; font-weight:650">| CLONEBERT</h1>
                    <h4 class="white--text font-weight-medium">follow the experts</h4>
                </div>
                <div class="ml-5 pa-3">
                    <v-img src="images/rocket.png" width="65%" />
                </div>
            </div>
            <br /><br />
            <h3 style="font-size:1.5rem; font-weight:500" class=" white--text text-left mb-3">Sign In</h3>
            <base-form @submit="login">
                <div class="mb-3">
                    <base-text-field label="Username" hide-details :value.sync="loginData.username" />
                </div>
                <div>
                    <base-text-field label="Password" hide-details :value.sync="loginData.password" />
                </div>
                <div class="d-flex justify-space-between align-center mt-3">
                    <div>
                        <base-checkbox class="mt-0" label="">
                            <template #label>
                                <div class="muted--text">
                                    Remember me
                                </div>
                            </template>
                        </base-checkbox>
                    </div>
                    <div>
                        <p @click="$router.push({name: 'Forgot Password'})" class="cursor-pointer btnprimary--text font-weight-medium">
                            Forgot Password
                        </p>
                    </div>
                </div>
                <div class="mt-3">
                    <base-btn class="white black--text" block type="submit">
                        SIGN IN
                    </base-btn>
                </div>
                <div class="mt-3 text-center">
                    <p class="white--text">Don't have an Account?<a @click="$router.push({name: 'Signup'})"> Sign Up</a></p>
                </div>
            </base-form>
        </base-card>
    </div>
</template>

<script lang="ts" src="./login.component.ts" />

<style lang="scss" scoped>
.max-width-500 {
    max-width: 500px;
}
</style>
