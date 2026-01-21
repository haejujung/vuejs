<script>
    export default {
        props: {
            name: {
                type: String,
                required: true,
                validator: function (value){
                    return value.length > 1;
                },
            },
            age: {
                type: Number,
                default: function(){
                    return 10;
                },
            },
        },
    }
</script>