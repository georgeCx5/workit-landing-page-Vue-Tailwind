<script>
import BtnApply from './components/BtnApply.vue'
import TextFeatures from './components/TextFeatures.vue'
import BtnNetworks from './components/BtnNetworks.vue'

import LogoLight from '@/assets/images/logo-light.svg?component'
import LogoDark from '@/assets/images/logo-dark.svg?component'
import patternOne from '@/assets/images/bg-pattern-1.svg?component'
import patternTwo from '@/assets/images/bg-pattern-2.svg?component'
import patternThree from '@/assets/images/bg-pattern-3.svg?component'

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
    patternOne,
    patternTwo,
    patternThree,
  }
}
</script>
<template>
  <body class=" relative flex flex-col items-center w-full font-manrope overflow-hidden">
    <patternOne class=" absolute hidden tb:block tb:top-20 dsk:top-28 tb:-left-56 dsk:-left-36 z-40" />
    <patternTwo class=" absolute hidden tb:block tb:top-60 dsk:top-[314px] tb:-right-24 dsk:-right-[70px] z-40" />
    <header class=" relative h-[462px] tb:h-[500px] dsk:h-[660px] w-full z-30">
      <div class=" flex flex-col gap-16 tb:gap-14 dsk:gap-[62px] h-full bg-neo-black">
        <nav class=" flex justify-between items-center px-4 tb:px-10 dsk:px-[165px] pt-8 dsk:pt-[50px]">
          <LogoLight />
          <BtnApply :txt="btnText" txt-color="text-neo-white" txt-hv-color="hover:text-neo-green" :has-border="true" />
        </nav>
        <div class=" flex flex-col items-center gap-10 dsk:gap-9 px-4 tb:px-32 dsk:px-96">
          <h1
            class=" text-neo-white text-center text-[50px] tb:text-[60px] dsk:text-[80px] leading-[50px] tb:leading-[60px] dsk:leading-[80px] tracking-tighter font-fraunces font-normal">
            Data <span class=" border-b-[3px] border-neo-green">tailored</span> to your needs.
          </h1>
          <button
            class=" w-[133px] dsk:w-[161px] h-[55px] dsk:h-[61px] bg-neo-green hover:bg-transparent text-neo-black hover:text-neo-green text-txt-base dsk:text-txt-lg font-extrabold border border-neo-green">Learn
            more</button>
        </div>
      </div>
      <!-- rounded end -->
      <div
        class=" absolute -bottom-4 tb:-bottom-10 dsk:-bottom-20 w-full h-8 tb:h-20 dsk:h-40 bg-neo-black rounded-b-[50%]">
      </div>
    </header>
    <main class=" relative flex flex-col items-center w-full -mt-[72px] tb:-mt-[108px] dsk:-mt-[196px]">
      <div
        class=" relative flex flex-col items-center gap-10 tb:gap-12 dsk:gap-[70px] w-full h-[1060px] tb:h-[900px] dsk:h-[920px] bg-neo-ghost">
        <img class=" w-[320px] tb:w-[514px] dsk:w-[767px] mb-5 tb:mb-[10px] z-50" :src="imgPhone" alt="imgPhone">
        <div class=" flex flex-col dsk:flex-row gap-10 tb:gap-12 dsk:gap-0">
          <TextFeatures :num="datos[0].id" :title="datos[0].title" :description="datos[0].description" />
          <TextFeatures :num="datos[1].id" :title="datos[1].title" :description="datos[1].description" />
          <TextFeatures :num="datos[2].id" :title="datos[2].title" :description="datos[2].description" />
        </div>
        <!-- rounded end -->
        <div
          class=" absolute -bottom-4 tb:-bottom-8 dsk:-bottom-20 w-full h-8 tb:h-16 dsk:h-40 bg-neo-ghost rounded-b-[50%]">
        </div>
      </div>
      <div
        class=" relative flex flex-col items-center w-[343px] tb:w-[689px] dsk:w-[1112px] h-[603px] tb:h-[526px] dsk:h-[648px] mt-28 tb:mt-[132px] dsk:mt-[188px]">
        <img class=" absolute tb:left-0 w-[281px] dsk:w-[477px]" :src="imgFounder" alt="imgFounder">
        <div
          class=" absolute bottom-0 dsk:bottom-[70px] tb:right-0 flex flex-col items-center tb:items-start gap-5 tb:gap-6 dsk:gap-8 tb:w-[514px] dsk:w-[730px] h-[375px] dsk:h-[413px] bg-neo-black px-[32px] tb:px-[58px] dsk:px-[70px] pt-8 tb:pt-12 dsk:pt-16 text-neo-white text-center tb:text-left z-40">
          <patternThree class=" absolute hidden tb:block tb:-bottom-[106px] dsk:-bottom-[62px] tb:right-4 dsk:right-[74px] z-50" />
          <h2
            class=" text-[32px] tb:text-[48px] dsk:text-[56px] leading-[48px] tb:leading-[56px] dsk:leading-[64px] tracking-tighter font-fraunces">
            Be
            the first to test</h2>
          <p class=" text-txt-base dsk:text-txt-lg font-light">
            Hi, I'm Louis Graham, the founder of the company. Book a demo call with me to become a beta tester for our app
            and kickstart your company. Apply for access below and I’ll be in touch to schedule a call.
          </p>
          <BtnApply class=" w-[172px] dsk:w-[190px] h-[55px] dsk:h-[61px] font-extrabold border border-neo-green"
            :txt="btnText" bg-color="bg-neo-green" bg-hv-color="hover:bg-transparent" txt-color="text-neo-black"
            txt-hv-color="hover:text-neo-green" />
        </div>
      </div>
    </main>
    <footer class=" flex flex-col items-center gap-[58px] my-[68px] tb:mt-20 dsk:mt-[50px] tb:mb-28">
      <LogoDark />
      <div class=" flex justify-between items-center w-[116px]">
        <BtnNetworks network="Facebook" />
        <BtnNetworks network="Twitter" />
        <BtnNetworks network="Instagram" />
      </div>
    </footer>
  </body>
</template>