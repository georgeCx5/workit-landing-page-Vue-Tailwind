<script>
export default {
   data() {
      return {
         value: '',
      }
   },
   props: {
      txt: String,
      bgColor: String,
      bgHvColor: String,
      txtColor: String,
      txtHvColor: String,
      hasBorder: {
         Boolean,
         default: false,
      },
   },
   methods: {
      getValue() {
         return this.hasBorder ? this.value = 'border-b-[3px]' : this.value = '';
      }
   },
   mounted() {
      this.getValue();
   }
}
</script>
<template>
   <button class=" text-btn-base dsk:text-btn-lg" :class="`${bgColor} ${bgHvColor} ${txtColor} ${txtHvColor} ${value} border-neo-green`">{{
      txt }}</button>
</template>