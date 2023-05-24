<script>
import IconFacebook from '@/assets/images/icon-facebook.svg?component'
import IconInstagram from '@/assets/images/icon-instagram.svg?component'
import IconTwitter from '@/assets/images/icon-twitter.svg?component'

export default {
   props: {
      network: String,
   },
   components: {
      IconFacebook,
      IconInstagram,
      IconTwitter,
   }
}
</script>
<template>
   <button class=" hover:brightness-[.25]">
      <component :is="`Icon${network}`" />
   </button>
</template>