<template>
    <div class="inputBox shadow">
        <input type="text" v-model="newTodoItem" placeholder="Type it">
        <span class="addContainer" v-on:click="addTodo">
            <font-awesome-icon class="addBtn" icon="plus" />
                <!-- <font-awesome-icon icon="user-secret" /> -->
        </span>
    </div>
</template>

<script>
export default {
    data() {
        return {
            newTodoItem: ''
        }
    },
    methods: {
        addTodo() {

            if (this.newTodoItem !== "") {
                const value = this.newTodoItem && this.newTodoItem.trim();
                localStorage.setItem(value, value);
                console.log(`NEW TODO ${this.newTodoItem}, ${value}`);
                this.clearInput();
            }
        },
        clearInput() {
            this.newTodoItem = '';
        }
    }
}
</script>

<style>
    input:focus {
        outline: none;
    }
    .inputBox {
        background: white;
        height: 50px;
        line-height: 50px;
        border-radius: 5px;
    }
    
    .inputBox input {
        border-style: none;
        font-size: 0.9rem;
    }

    .addContainer {
        float: right;
        background: linear-gradient(to right, #6478FB, #8763FB);
        display: block;
        width: 3rem;
        border-radius: 0 5px 5px 0;
    }

    .addBtn {
        color: white;
        vertical-align: middle;
    }
</style>
