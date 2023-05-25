<script>
export default {
   data() {
      return {

      }
   },
   props: {
      num: String,
      title: String,
      description: String,
   }
}
</script>
<template>
   <div class=" flex flex-col tb:flex-row dsk:flex-col items-center gap-6 tb:gap-8 dsk:gap-[57px] mx-4 text-neo-black z-30">
      <h3
         class=" flex justify-center items-center text-[20px] dsk:text-[24px] leading-[36px] dsk:leading-[40px] font-fraunces dsk:font-medium w-12 dsk:w-14 h-12 dsk:h-14 border border-neo-black rounded-full">
         {{ num }}</h3>
      <div class=" flex flex-col gap-4 dsk:gap-[27px] tb:w-[478px] dsk:w-[354px] text-center tb:text-left dsk:text-center">
         <h2 class=" text-[28px] dsk:text-[32px] leading-[36px] dsk:leading-[40px] tracking-tighter font-fraunces font-medium">{{ title }}</h2>
         <p class=" text-txt-base dsk:text-txt-lg">{{ description }}</p>
      </div>
   </div>
</template>