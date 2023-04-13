<template>
    <div class="home">
        <HeaderComponent />
        <HeroComponent />
        <ProductComponent />
        <InstaComponent />
        <PartnerComponent />
    </div>
</template>

<script>
// @ is an alias to /src
import HeaderComponent from '@/components/HeaderComponent.vue'
import HeroComponent from '@/components/HeroComponent.vue'
import ProductComponent from '@/components/ProductComponent.vue'
import InstaComponent from '@/components/InstaComponent.vue'
import PartnerComponent from '@/components/PartnerComponent.vue'

export default {
    components: {
        HeaderComponent,
        HeroComponent,
        ProductComponent,
        InstaComponent,
        PartnerComponent,
    },
}
</script>
