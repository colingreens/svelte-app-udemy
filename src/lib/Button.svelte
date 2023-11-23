<script>
    
</script>

<button><slot /></button>

<style lang="scss">
    button{
        border: none;
        background-color: var.$color;
        color: #ffffff;
        padding: 15px 20px;
        font-weight: bold;
        border-radius: 5px;
        cursor: pointer;
        &:hover{
            background-color: #ffffff;
        }
    }
</style>