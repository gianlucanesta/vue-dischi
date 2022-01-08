<template>
    <header>

        <div class="logo d-flex">
            <img src="../assets/logo.png" alt="logo">
        </div>
        
    </header>
</template>

<script>

    export default {
        name: 'Header',
    };

</script>

<style scoped lang="scss" >
@import '../style/variables.scss';

    header {
        
        background-color: $primary-color;
        
        .logo {
            padding: 10px 10px;
            justify-content: flex-start;
            align-items: center;
            margin-left: 15px;

            img {
                height: 50px;
            }
        }
    }

</style>