<template>
    <div class="shadow-md p-5 bg-blue-700 text-center">

        <!-- Year -->
        <div class="shadow-md p-2 bg-blue-600">
            <h1 class="font-semibold font-xl shadow-sm text-white hover:text-orange-400 tracking-wider">{{ year }}</h1>
        </div>

        <!-- List for each month -->
        <div class="mt-2">
            <ul>
                <li 
                    v-for="mth in months" 
                    :key="mth" 
                    class="text-lg text-gray-200 hover:text-orange-400"
                    @click="emitMonth(mth, year)"
                >
                    {{ mth }}
                </li>
            </ul>
        </div>

    </div>
</template>

<script>
export default {
    data() {
        return {
            months: ['Jun', 'May', 'Apr', 'Mar']
        }
    },
    props: [
        'year',
        'month'
    ],
    methods: {
        emitMonth: function(mth, yr) {
            this.$emit('filterMonth', mth, yr)
        }
    }
}
</script>

<style scoped>
</style>
