<template>
    <div>
        <v-container>
            <v-card class="ma-5 pa-5" cols="12" md=8>
                <v-form lazy-validation>
                    <v-row justify="center">
                        <v-col cols="12" md="8">
                            <h1 class="display-2 text-center ma-5">Contact Form</h1>
                        </v-col>
                    </v-row>
                    <v-row justify="center">
                        <v-col cols="12" md="8">
                            <v-text-field v-model="name" name="name" :rules="nameRules" label="Name..." required></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row justify="center">
                        <v-col cols="12" md="8">
                            <v-text-field v-model="email" name="email" :rules="emailRules" label="Email..." required></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row justify="center">
                        <v-col cols="12" md="8">
                            <v-textarea v-model="message" name="message" :rules="messageRules" label="Message..."></v-textarea>
                        </v-col>
                    </v-row>                    
                    <v-row justify="center">
                        <v-col class="text-center" cols="12" md="8">
                            <v-btn text>Submit</v-btn>
                        </v-col>
                    </v-row>
                </v-form>
            </v-card>
        </v-container>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: "",
            email: "",
            message: "",
            emailRules: [
                value => !!value || 'Required.',
                value => (value || '').length <= 20 || 'Max 20 characters',
                value => {
                const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
                return pattern.test(value) || 'Invalid e-mail.'
                },
            ],
            nameRules: [
                value => !!value || 'Required.',
                value => (value || '').length <= 20 || 'Max 20 characters'
            ],
            messageRules: [
                value => !!value || 'Required.',
                value => (value || '').length >= 20 || 'Min 20 characters'
            ],
        }
    }
}
</script>