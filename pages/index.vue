<template>
  <div>

    <Hero />

    <FirstSection />

    <SecondSection />

    <ThirdSection />

    <SubbeddSection />

    <OurOffersSection :cards="cards"/>
    
    <Footer />

  </div>
</template>

<script>
import Hero from '@/components/hero/Hero';
import FirstSection from '@/components/section/FirstSection';
import SecondSection from '@/components/section/SecondSection';
import ThirdSection from '@/components/section/ThirdSection';
import SubbeddSection from '@/components/section/SubbeddSection';
import OurOffersSection from '@/components/section/OurOffersSection';
import Footer from '@/components/footer/Footer';

export default {
  data() {
    return {
      cards: [
        { title: "Free", price: { monthly: 0, yearly: 0 }, video: 50, languages: 2, other1: false, other2: false, other3: false },
        { title: "Junior", price: { monthly: 30, yearly: 300 }, video: 50, languages: 4, other1: true, other2: true, other3: true },
        { title: "Explorer", price: { monthly: 0, yearly: 500 }, video: 50, languages: 6, other1: true, other2: true, other3: true },
        { title: "Captain", price: { monthly: 0, yearly: 0 }, video: 50, languages: 6, other1: true, other2: true, other3: true }
      ]
    }
  },
  components: {
    Hero,
    FirstSection,
    SecondSection,
    ThirdSection,
    SubbeddSection,
    OurOffersSection,
    Footer,
  },
}
</script>

<style>

</style>
