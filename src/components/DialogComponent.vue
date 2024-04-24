<template>
    <div>
        <v-dialog max-width="500">
            <template v-slot:activator="{ props: activatorProps }">
                <v-btn v-bind="activatorProps" size="x-large" block class="modal-btn">
                    <p>{{ user.login }}</p>
                </v-btn>
            </template>

            <v-card title="User Info">
                <v-card-text>
                    {{ user.login }}`s id is {{ user.id }}
                </v-card-text>
            </v-card>

        </v-dialog>
    </div>
</template>

<script setup>
defineProps({ user: Object })
</script>

<style scoped></style>