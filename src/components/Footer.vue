<template>
  
    <div class="container">
        <div class="container--box">
            <ColumnSx/>
            <ColumnCenter/>
            <ColumnDx/>
        </div>
        <div class="conpyright">
            <p>© Copyright 2012 - 2021 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</p>
        </div>
    </div>

</template>


<script>               

    import ColumnSx from '@/components/ColumnSx.vue';
    import ColumnCenter from '@/components/ColumnCenter.vue';
    import ColumnDx from '@/components/ColumnDx.vue';




    export default {
        
        name: 'Footer',

        components: {

            ColumnSx,
            ColumnCenter,
            ColumnDx

        }

    }

</script>


<style scoped lang="scss">

    @import '@/style/variabili.scss';
    @import '@/style/mixins.scss';
    
    .container--box {
        display: flex;
    }

    .conpyright {
        padding: 30px;
        background-color: rgb(228, 228, 228);
        color: $Raven;
    }

</style>
