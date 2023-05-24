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
   <div class=" flex flex-col items-center gap-6 px-4 text-neo-black">
      <div class=" flex flex-col justify-center items-center w-12 h-12 border border-neo-black rounded-full">
         <h3 class=" text-[20px] leading-[36px] font-fraunces">{{ num }}</h3>
      </div>
      <div class=" flex flex-col gap-4 text-center">
         <h2 class=" text-[28px] leading-[36px] tracking-tighter font-fraunces font-medium">{{ title }}</h2>
         <p class=" text-[16px] leading-[28px]">{{ description }}</p>
      </div>
   </div>
</template>