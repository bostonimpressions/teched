<script setup lang="ts">
  const footerLinks = [
    {
      title: 'Company',
      links: [
        { label: 'Home', url: '/' },
        { label: 'Programs', url: '/programs' },
        { label: 'Who We Are', url: '/who-we-are' },
        { label: 'Contact Us', url: '/contact' },
      ],
    },
    {
      title: 'Programs',
      links: [
        { label: 'K12 Education', url: '/k12-education' },
        {
          label: 'Career & Technical Education',
          url: '/career-and-technical-education',
        },
        { label: 'Industry Training', url: '/industry-training' },
        {
          label: 'Industry Recognized Certifications',
          url: '/industry-recognized-certifications',
        },
      ],
    },
  ]

  const partners = [
    { label: `Amatrol`, url: `` },
    { label: `APT: Manufacturing Solutons`, url: `` },
    { label: `Atech Automotive training`, url: `` },
    { label: `Bayport Technical`, url: `` },
    { label: `Brainco`, url: `` },
    { label: `Chaney Electronics`, url: `` },
    { label: `CNC Concept`, url: `` },
    { label: `LEVIL Technology`, url: `` },
    { label: `Lincoln Electric`, url: `` },
    { label: `LJ Create`, url: `` },
    { label: `Manufacturing Skills Standards Council`, url: `` },
    { label: `MINDS-i Robotics`, url: `` },
    { label: `OnRobots`, url: `` },
    { label: `Simlog`, url: `` },
    { label: `Smart Automation Certification Allience`, url: `` },
    { label: `Stokes Educational Services`, url: `` },
    { label: `DAC Worldwide`, url: `` },
    { label: `Denford Limited`, url: `` },
    { label: `Dynalogic Concept`, url: `` },
    { label: `Elenco Electronics`, url: `` },
    { label: `FANUC America`, url: `` },
    { label: `Interior Concepts`, url: `` },
    { label: `Tii Technical Educational Systems`, url: `` },
    { label: `VRSim`, url: `` },
  ]
</script>

<template>
  <footer class="base-footer">
    <div class="container">
      <div class="five-col-grid">
        <!-- Company -->
        <div class="grid-item">
          <h3>{{ footerLinks[0].title }}</h3>
          <ul>
            <li v-for="(link, i) in footerLinks[0].links" :key="i">
              <a :href="link.url">{{ link.label }}</a>
            </li>
          </ul>
        </div>

        <!-- Programs -->
        <div class="grid-item">
          <h3>{{ footerLinks[1].title }}</h3>
          <ul>
            <li v-for="(link, i) in footerLinks[1].links" :key="i">
              <a :href="link.url">{{ link.label }}</a>
            </li>
          </ul>
        </div>

        <!-- Partners spanning 3 columns -->
        <div class="grid-item partners">
          <h3>Partners</h3>
          <div class="partners-grid">
            <ul v-for="(_, colIndex) in 3" :key="colIndex">
              <li
                v-for="(link, i) in partners.slice(
                  colIndex * Math.ceil(partners.length / 3),
                  (colIndex + 1) * Math.ceil(partners.length / 3)
                )"
                :key="i"
              >
                <a :href="link.url">{{ link.label }}</a>
              </li>
            </ul>
          </div>
        </div>
      </div>

      <div class="copyright">©2025 - TechEd | All right reserved</div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
  .base-footer {
    background: var(--darkblue);
    color: var(--offwhite);
    padding: 80px 0;

    .copyright {
      padding-top: 40px;
      border-top: 1px solid rgba(255, 255, 255, 0.06);
    }
  }

  .five-col-grid {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 40px;

    .grid-item {
      display: flex;
      flex-direction: column;
      gap: 16px;

      h3 {
        font-weight: 700;
        color: var(--white);
      }

      ul {
        list-style: none;
        padding: 0;
        margin: 0;

        li {
          margin-bottom: 8px;

          a {
            text-decoration: none;
            color: var(--white);

            &:hover {
              text-decoration: underline;
            }
          }
        }
      }
    }

    .partners {
      grid-column: 3 / 6; // spans columns 3,4,5
      display: flex;
      flex-direction: column;

      .partners-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 16px;

        ul {
          margin: 0;
          padding: 0;
          list-style: none;
        }
      }
    }
  }

  @media (max-width: 1024px) {
    .five-col-grid {
      grid-template-columns: 1fr;
      gap: 24px;

      .partners {
        grid-column: auto;
        .partners-grid {
          grid-template-columns: 1fr;
        }
      }
    }
  }
</style>
