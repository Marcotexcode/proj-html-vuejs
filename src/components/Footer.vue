<template>
  
    <div class="container">

        <ColumnSx/>
        <ColumnCenter/>
        <ColumnDx/>

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
    
    .container {
        display: flex;
    }

</style>
