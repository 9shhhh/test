<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Example Component</div>

                    <div class="card-body">
                        I'm an example component.
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        computed: {
            hasResult: function () {
                return this.posts.length > 0
            }
        },
        mounted() {
            console.log('ddd');
            this.$http.get('/user')
                .then( response => { console.log(response); } ) // SUCCESS
                .catch( response => { console.log(response); } ); // ERROR
            console.log('Component mounted.')
        }
    }
</script>
