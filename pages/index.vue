<template>
  <div>
    <Hero />

    <FirstSection />

    <SecondSection />

    <ThirdSection />

    <SubbeddSection />
    
  </div>
</template>

<script>
import Hero from '@/components/hero/Hero';
import FirstSection from '@/components/section/FirstSection';
import SecondSection from '@/components/section/SecondSection';
import ThirdSection from '@/components/section/ThirdSection';
import SubbeddSection from '@/components/section/SubbeddSection';

export default {
  components: {
    Hero,
    FirstSection,
    SecondSection,
    ThirdSection,
    SubbeddSection,
  },
}
</script>

<style>

</style>
