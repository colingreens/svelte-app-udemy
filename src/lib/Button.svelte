<script>
    export let bgColor = 'red'
    export let textColor = 'white'
    export let size = 'small';
    export let shadow = false;
    
</script>

<button 
        style:background-color={bgColor}
        style:color={textColor}
        class:size-lg={size === 'large'}
        class:size-sm={size === 'small'}
        class:shadow><slot /></button>

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
            background-image: linear-gradient(rgba(0,0,0, 0.4) 0 0);
        }
        &:active{
            background-image: linear-gradient(rgba(255, 255, 255, 0.4) 0 0);
        }
        &.size-sm {
            padding: 15px 20px;
        }
        &.size-lg {
            padding: 20px 25px;
            font-size: 20px;
        }
        &.shadow{
            box-shadow: 0 0 10px rgba(255, 255, 255, 0.3);
        }
    }
</style>