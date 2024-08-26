<template>
    <section>
        <base-card>
            <div>
                <h2>Register as Coach now!</h2>
                <coach-form @save-data="saveData"></coach-form>
            </div>
        </base-card>
    </section>
</template>



<script>
import CoachForm from '../../components/coaches/CoachForm.vue';
export default {
    components: { CoachForm },
    methods: {
        saveData(data) {
            this.$store.dispatch('coaches/registerCoach', data)
            this.$router.replace('/coaches');
        }
    }
}
</script>

<style scoped>
/* Aggiungi stili specifici qui */
</style>
