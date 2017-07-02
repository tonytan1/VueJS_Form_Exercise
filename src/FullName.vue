<template>
    <div>
        <div class="form-group">
            <label for="firstname">First Name</label>
            <input type="text" id="firstname" class="form-control" v-model="firstName">
        </div>
    
        <div class="form-group">
            <label for="lastname">Last Name</label>
            <input type="text" id="lastname" class="form-control" v-model="lastName">
        </div>
    </div>
</template>

<script>
export default {
    props: ['fullName'],
    data: function() {
        return {
            firstName: '',
            lastName: ''
        }
    },

    methods: {
        showFullName() {
            this.$emit('input', this.firstName + ' ' + this.lastName);
        }
    },

    updated() {
        this.showFullName();
    }
}
</script>

<style>

</style>


