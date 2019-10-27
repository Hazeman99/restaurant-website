<template>
    <div class="navbar">
        <v-toolbar flat>
            <v-toolbar-title class="headline text-uppercase">
                <span>HAZE</span>
                <span class="font-weight-light"> Restaurant</span>
            </v-toolbar-title>
            <div class="flex-grow-1"></div>

            <v-toolbar-items class="hidden-sm-and-down">
                <v-btn to="/" text>Home</v-btn>
                <v-btn to="/about" text>About</v-btn>
                <v-btn to="/contact" text>Contact</v-btn>
            </v-toolbar-items>

            <v-toolbar-items class="hidden-md-and-up">
                <v-btn icon to="/">
                    <v-icon>mdi-home</v-icon>
                </v-btn>
                <v-btn icon to="/about">
                    <v-icon>mdi-information</v-icon>
                </v-btn>
                <v-btn icon to="/contact">
                    <v-icon>mdi-chat</v-icon>
                </v-btn>
            </v-toolbar-items>
        </v-toolbar>
    </div>
</template>