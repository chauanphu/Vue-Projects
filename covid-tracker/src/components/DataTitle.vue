<template>
    <div class="text-center">
        <div class="text-3xl font-bold">{{text}}</div>
        <div class="text-2xl mt-6 mb-10">{{timestamp}}</div>
    </div>
</template>
<script>
import moment from 'moment';
export default {
    name: "DataTitle",
    props: {
        text: String,
        dataDate: String
    },
    computed: {
        timestamp(){
            return moment(this.dataDate).format('MMMM Do YYYY, h:mm:ss a')
        }
    }
}
</script>