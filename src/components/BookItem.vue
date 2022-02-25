<template>
    <div >
        <div>
            <div class="float-right book">
                <div>
                    {{book.title}}
                </div>
                <div class="icons">
                    <i class="glyphicon glyphicon-pencil" @click="$emit('edit-book-item', book.id)"></i>
                    <i class="glyphicon glyphicon-trash" @click="$emit('del-book-item', book.id)"></i>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "BookItem",
        props: ["book"]
    }
</script>

<style >
    .book{
        -webkit-box-shadow: 2px 0px 20px -4px rgba(0,0,0,0.59); 
        box-shadow: 2px 0px 20px -4px rgba(0,0,0,0.59);
        padding:30px;
        margin-right: 20px;
        border-radius:10px;
        font-size: 30px;
        width:300px;
    }
    .icons{
        display: flex;
        justify-content: space-between;
        margin-top: 20px;
        cursor:pointer;
    }
    
</style>
