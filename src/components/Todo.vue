<template>
    <div class="jumbotron">
        <h2>List of Todos</h2>
        <hr>
        <div class="row">
            <div class="col-md-6">
                <table  class="table table-striped table-bordered table-responsive">
                    <thead>
                        <tr>
                            <th>ID</th>
                            <th>Todo Title</th>
                            <th>Todo Body</th>
                            <th>Action</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="todo in todos" v-bind:key="todo">
                            <td>{{todo.id}}</td>
                            <td>{{todo.title}}</td>
                            <td>{{todo.body}}</td>
                            <td>
                                <span class="btn btn-primary btn-sm">Edit</span> | 
                                <span class="btn btn-danger btn-sm" v-on:click="deleteTodo">Delete</span>
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <div class="col-md-1"></div>
            <div class="col-md-4">
                <form v-on:submit="addTodo" action="">
                    <div class="form-group">
                        <input id="my-input" class="form-control" v-model="id" type="text" placeholder="Enter ID">
                    </div>
                    <div class="form-group">
                        <input id="my-input" class="form-control" v-model="title" type="text" placeholder="Enter Title">
                    </div>
                    <div class="form-group">
                        <input id="my-input" class="form-control" v-model="body" type="text" placeholder="Enter Todo Message">
                    </div>
                    <button type="submit" class="btn btn-primary btn-block">Add Todo</button>
                </form>

            </div>
        </div>
        
    </div>
    
</template>

<script>
export default {
    data(){
        return{
            id: '',
            title: '',
            body: '',
            todos: [
                {
                    id: 1,
                    title: 'Wake Up',
                    body: 'Wake up by 10am'
                },
                {
                    id: 2,
                    title: 'School Resumption',
                    body: 'We are resuming on 30th of Oct'
                },
                {
                    id: 3,
                    title: 'Food Stuff',
                    body: 'Buy 1 crate of egg and cra-fish'
                }
            ]
        }
    },
    methods: {
        deleteTodo(id){
            if(confirm('Are you sure you want to delete this? ')){
                this.todos = this.todos.filter(todo => todo.id !== id)
                // let id = this.todos.id;
                // console.log('Good');
                // alert("good");
            }else{
                alert('false');
                // console.log("happy");
            }
        },
        addTodo(){
            this.todos.id = this.id;
            this.todos.title = this.title;
            this.todos.body = this.body;
        }
    }
}
</script>


<style scoped>
h2{
    text-align: center;
    padding-top: 5px;
    
}
form{
    padding-top: 20px;
}

</style>