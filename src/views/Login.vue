<template>
    <div class="center">
        <v-row>
            <v-col cols="10" offset="1" sm="6" offset-sm="3" md="4" offset-md="4">
                <v-avatar color="primary" size="128" rounded="1">
                    <v-img src="@/assets/logo.png"></v-img>
                </v-avatar>
                <div style="margin-top: 20px;"></div>
                <v-text-field v-model="username" filled label="Username" clearable></v-text-field>
                <v-text-field v-model="password" filled label="Password" clearable type="password"></v-text-field>
                <v-btn class="base-inverted" block @click="onLogin()">
                    Login
                </v-btn>
            </v-col>
        </v-row>
    </div>
</template>

<script>
export default {
    data() {
        return {
            username: "",
            password: ""
        }
    },
    methods: {
        onLogin() {
            alert("Clicked")
        }
    }
}
</script>

<style lang="scss" scoped></style>