<template>
    <select @change="onChanged" v-model="selected" class="form-select mt-10 p-3 block w-full border rounded">
        <option value="0">Select Country</option>
        <option v-for="country in countries" :key="country.ID" :value="country.ID">
            {{country.Country}}
        </option>
    </select>
</template>
<script>
export default {
    name: 'CountrySelect',
    props: ['countries'],
    data() {
        return {
            selected: 0
        }
    },
    methods: {
        onChanged() {
            const country = this.countries.find( item => item.ID === this.selected)
            this.$emit('get-country', country)
        }
    }
}
</script>