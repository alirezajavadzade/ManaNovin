<template>
    <v-container fluid>
        <v-row>
            <v-col cols="12">
                <div class="about-page">
                    <h1>پروژه شرکت نوین مانا</h1>
                    <div>
                        <p>در این پروژه از فریم ورک vuetify کمک گرفته شد</p>
                        <p>همچنین از typescript برای جلوگیری از خطا ها استفاده شد</p>
                        <p>برای routing نیز از vue-router کمک گرفته شد</p>
                    </div>
                    <a href="">لینک گیت هاب پروژه</a>
                </div>
            </v-col>
        </v-row>
    </v-container>
</template>

<script setup>

</script>

<style scoped>
.about-page {
    direction: rtl;
}

.about-page h1 {
    display: inline-block;
    border-bottom: 1px solid #000;
    padding-bottom: 0.3rem;
}

.about-page div {
    margin: 2rem 0;
}

.about-page p {
    margin: 1rem 0;
}
</style>