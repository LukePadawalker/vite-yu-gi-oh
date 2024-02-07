<script>
export default {
    name: 'TypeSelect',
    data: () => ({
        selectedOption: '',
    }),
    props: {
        defaultLabel: String,
        defaultValue: String,
        options: Array
    },
    emits: ['option-change']
}
</script>

<template>
    <select v-model="selectedOption" @change="$emit('option-change', selectedOption)">
        <option :value="defaultValue || ''">{{ defaultLabel }}</option>
        <option v-for="option in options">{{ option }}</option>

    </select>
</template>

<style lang="scss" scoped></style>
