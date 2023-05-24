<script>
import BtnApply from './components/BtnApply.vue'
import TextFeatures from './components/TextFeatures.vue'
import BtnNetworks from './components/BtnNetworks.vue'

import LogoLight from '@/assets/images/logo-light.svg?component'
import LogoDark from '@/assets/images/logo-dark.svg?component'

// images
import imgFounder from '@/assets/images/image-founder.webp'
import imgPhone from '@/assets/images/image-hero.webp'

export default {
  data() {
    return {
      imgFounder,
      imgPhone,
      btnText: 'Apply for access',
      datos: [
        {
          id: '1',
          title: 'Actionable insights',
          description: 'Optimize your products, improve customer satisfaction and stay ahead of the competition with our product data analytics.',
        },
        {
          id: '2',
          title: 'Data-driven decisions',
          description: 'Make data-driven decisions with our product data analytics. Our AI-generated reports help you unlock insights hidden in your product data.',
        },
        {
          id: '3',
          title: 'Always affordable',
          description: 'Always affordable pricing that scales with your business. Get top-quality product data analytics services without hidden costs or unexpected fees.',
        }
      ]
    }
  },
  components: {
    // components
    BtnApply,
    TextFeatures,
    BtnNetworks,
    // SVG's
    LogoLight,
    LogoDark,
  }
}
</script>
<template>
  <body class=" flex flex-col items-center w-full font-manrope">
    <header class=" relative h-[462px] w-full z-30">
      <div class=" flex flex-col gap-16 h-full bg-neo-black">
        <nav class=" flex justify-between items-center px-4 pt-8">
          <LogoLight />
          <BtnApply :txt="btnText" txt-color="text-neo-white" txt-hv-color="hover:text-neo-green" :has-border="true" />
        </nav>
        <div class=" flex flex-col items-center gap-10 px-4">
          <h1 class=" text-neo-white text-center text-[50px] leading-[50px] font-fraunces font-normal tracking-tighter">
            Data <span class=" border-b-[3px] border-neo-green">tailored</span> to your needs.
          </h1>
          <button
            class=" w-[133px] h-[55px] bg-neo-green hover:bg-transparent text-neo-black hover:text-neo-green text-btn-base font-extrabold border border-neo-green">Learn
            more</button>
        </div>
      </div>
      <!-- rounded end -->
      <div class=" absolute -bottom-4 w-full h-8 bg-neo-black rounded-b-[50%]">
      </div>
    </header>
    <main class=" flex flex-col items-center  w-full -mt-[72px]">
      <div class=" relative flex flex-col items-center gap-10 w-full h-[1060px] bg-neo-ghost">
        <img class=" w-[320px] z-50 mb-5" :src="imgPhone" alt="imgPhone">
        <TextFeatures :num="datos[0].id" :title="datos[0].title" :description="datos[0].description" />
        <TextFeatures :num="datos[1].id" :title="datos[1].title" :description="datos[1].description" />
        <TextFeatures :num="datos[2].id" :title="datos[2].title" :description="datos[2].description" />
        <div class=" absolute -bottom-4 w-full h-8 bg-neo-ghost rounded-b-[50%]"></div>
      </div>
      <div class=" relative flex flex-col items-center w-full h-[603px] mt-28">
        <img class=" w-[281px]" :src="imgFounder" alt="imgFounder">
        <div
          class=" absolute bottom-0 flex flex-col items-center gap-5 h-[375px] bg-neo-black mx-4 px-[32px] pt-8 text-neo-white text-center z-50">
          <h2 class=" text-[32px] leading-[48px] tracking-tighter font-fraunces fontl">Be the first to test</h2>
          <p class=" text-txt-base font-light">
            Hi, I'm Louis Graham, the founder of the company. Book a demo call with me to become a beta tester for our app
            and kickstart your company. Apply for access below and I’ll be in touch to schedule a call.
          </p>
          <BtnApply class=" w-[172px] h-[55px] font-extrabold border border-neo-green" :txt="btnText"
            bg-color="bg-neo-green" bg-hv-color="hover:bg-transparent" txt-color="text-neo-black"
            txt-hv-color="hover:text-neo-green" />
        </div>
      </div>
    </main>
    <footer class=" flex flex-col items-center gap-[58px] my-[68px]">
      <LogoDark />
      <div class=" flex justify-between w-[116px]">
        <BtnNetworks network="Facebook" />
        <BtnNetworks network="Instagram" />
        <BtnNetworks network="Twitter" />
      </div>
    </footer>
  </body>
</template>