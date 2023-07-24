<template lang="pug">
.about
  Navbar(:breadcrumbs="breadcrumbs")

  v-content
    v-container
      .team-member
        span.display-4.text-yellow.font-weight-medium सदस्य
        .team-member-profiles
          .team-member-profile(v-for="item in items", :key="item.id")
            v-avatar(size="128")
              v-img(:src="item.url", aspect-ratio="0.9")
            .team-member-profile-info
              span.username.font-weight-light {{ item.name }}
              span.department.font-weight-medium.pt-1 {{ item.department }}
              span.department.font-weight-medium.pt-1 {{ item.department2 }}
              v-row.pt-2(justify="space-around")
                a(:href="item.email", target="_blank")
                  v-icon.mr-2 mdi-email
                a(:href="item.phone", target="_blank")
                  v-icon.mr-2 mdi-phone
</template>

<script>
import Navbar from '@/components/Navbar.vue';

export default {
  name: 'home',
  components: {
    Navbar,
  },
  data() {
    return {
      items: [
        {
          name: 'डॉ. ओमप्रकाश र. बंसल',
          department: 'निदेशक, रा. प्रो. सं. गोवा ',
          department2: 'अध्यक्ष, राजभाषा समिति',
          url: require('@/assets/director2023.jpeg'),
          email: 'mailto:patodirector@nitgoa.ac.in',
          phone: 'tel:+918322404200',
        },
        {
          name: 'डॉ. लोकेश कुमार ब्रम्हने',
          department: 'सहायक प्राध्यापक (सदस्य)',
          url: require('@/assets/lokesh kumar brahmane.jpeg'),
          email: 'mailto:lokes.brahmane@nitgoa.ac.in ',
          phone: 'tel:',
        },
        {
          name: 'डॉ. प्रवति स्वान ',
          department: 'सहायक प्राध्यापक (सदस्य)',
          url: require('@/assets/pravati swain.png'),
          email: 'mailto:pragati@nitgoa.ac.in',
          phone: 'tel:+91-832-2404204',
        },
        {
          name: 'श्री मनमोहन सखूजा ',
          department: 'सहायक सचिव (सदस्य)',
          url: require('@/assets/manmohan sakhuja.jpg'),
          email: 'mailto:ar_af@nitgoa.ac.in',
          phone: 'tel:+91-7607005575',
        },
        {
          name: 'डॉ. प्रसंजित डे',
          department: 'सहायक प्राध्यापक (सदस्य)',
          url: require('@/assets/pransenjit dey.png'),
          email: 'mailto:prasenjit.dey@nitgoa.ac.in',
          phone: 'tel:+91-9774735514',
        },
        {
          name: 'श्री एस सुदर्सन',
          department: 'संगणक विज्ञान अभियांत्रिकी',
          url: require('@/assets/Sudharsan Sridharan.jpg'),
          email: 'mailto:sudharsan@nitgoa.ac.in',
          phone: 'tel:+91-9405153443',
        },
        {
          name: 'श्रीमती सुविधा नाइक',
          department: 'इलेक्ट्रिकल एवं इलेक्ट्रॉनिक्स अभियांत्रिकी',
          url: require('@/assets/Suvida Madkaiker.jpg'),
          email: 'mailto:suvidanaik@nitgoa.ac.in',
          phone: 'tel:',
        },
        {
          name: 'श्री निखिल उदय नाइक',
          department: 'इलेक्ट्रॉनिक्स एवं संचार  अभियांत्रिकी',
          url: require('@/assets/nikhil.jpg'),
          email: 'mailto:nikhilnaik@nitgoa.ac.in',
          phone: 'tel:+91-9588604598',
        },
        {
          name: 'श्री राजकुमार',
          department: 'मानविकी एवं सामाजिक विज्ञान',
          url: require('@/assets/Kanneboina RajKumar.jpg'),
          email: 'mailto:rajkumar@nitgoa.ac.in',
          phone: 'tel:',
        },
        {
          name: 'श्री संदीप जैसवार',
          department: 'प्रशासनिक विभाग / स्थापना विभाग ',
          url: require('@/assets/Sandeep Jaishwar.jpg'),
          email: 'mailto:sandeep8025@nitgoa.ac.in',
          phone: 'tel:',
        },
        {
          name: 'श्री विजईश वी पी',
          department: 'यांत्रिक अभियांत्रिकी ',
          url: require('@/assets/vijeesh.jpg'),
          email: 'mailto:vijeesh@nitgoa.ac.in',
          phone: 'tel:+91-9048134023',
        },

        {
          name: 'श्रीमती नम्रता ए. गिरपी',
          department: 'असैनिक अभियांत्रिकी',
          url: require('@/assets/namrata.jpg'),
          email: 'mailto:namrata@nitgoa.ac.in',
          phone: 'tel:+91-7887346493',
        },
        {
          name: 'सुश्री प्रियंका परब ',
          department: 'अनुप्रयुक्त विज्ञान',
          url: require('@/assets/priyanka parab.png'),
          email: 'mailto:priyankaparab@nitgoa.ac.in',
          phone: 'tel:',
        },
        {
          name: 'श्री प्रीतम नागेश्कर',
          department: 'प्रशासनिक विभाग',
          url: require('@/assets/pritam Nageshkar.jpg'),
          email: 'mailto:pritamnageshkar@nitgoa.ac.in',
          phone: 'tel:7507836161',
        },
        {
          name: 'श्रीमती मीनाक्षी ',
          department: 'प्रशासनिक विभाग',
          url: require('@/assets/MeenakshiMaam.png'),
          email: 'mailto:meenakshi@nitgoa.ac.in',
          phone: 'tel:8595881062',
        }, // Add new members here
        //Add a comma here before adding another member
      ],
      breadcrumbs: [
        {
          text: 'होम',
          disabled: false,
          href: '/',
        },
        {
          text: 'सदस्य',
          disabled: true,
          href: '/members',
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.about {
  padding-bottom: 128px;
}

.team-member {
  padding-top: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  .display-4 {
    text-align: center;
  }

  &-profiles {
    :first-child {
      grid-column: 1 / span 3;
      @media (max-width: 1264px) {
        grid-column: 1 / span 1;
      }
    }

    @media (max-width: 1264px) {
      grid-template-columns: 1fr;
    }
    padding-top: 2rem;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-row-gap: 3rem;
  }

  &-profile {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    &-info {
      display: flex;
      padding-top: 0.5rem;
      flex-direction: column;
      align-items: center;
      .username {
        font-size: 1.6rem;
      }
      .department {
        font-size: 1.2rem;
        margin-top: -0.3rem;
      }
    }
  }
}
</style>
