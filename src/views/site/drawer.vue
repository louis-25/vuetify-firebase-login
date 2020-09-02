<template>
    <div>
        <site-menutitle></site-menutitle>
        <v-divider></v-divider>
        <site-menu></site-menu>
    </div>
</template>
<script>
import SiteMenu from '@/views/site/menu'
import SiteMenutitle from '@/views/site/menutitle'

export default {
  components: {
    SiteMenu,
    SiteMenutitle
  }
}
</script>
