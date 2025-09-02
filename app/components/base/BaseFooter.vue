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
      <nav class="footer-top">
        <div class="branding">
          <img
            src="/icons/light-bug.png"
            alt="TEP logo"
            class="branding-logo"
          />
          <div class="social">
            <a
              href="https://www.linkedin.com/company/techedproducts"
              target="_blank"
              rel="noopener"
            >
              <img src="/icons/social-li.svg" alt="LinkedIn" />
            </a>
            <a
              href="https://www.facebook.com/TechEdProducts"
              target="_blank"
              rel="noopener"
            >
              <img src="/icons/social-fb.svg" alt="Facebook" />
            </a>
            <a
              href="https://www.youtube.com/channel/UCQlhFSd02QE4pKwGRSjW3Vw"
              target="_blank"
              rel="noopener"
            >
              <img src="/icons/social-yt.svg" alt="YouTube" />
            </a>
            <a
              href="https://x.com/TechEdProducts"
              target="_blank"
              rel="noopener"
            >
              <img src="/icons/social-tw.svg" alt="Twitter" />
            </a>
          </div>
        </div>

        <div class="contact">
          <h3>Contact</h3>
          <div class="contact-item">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 20 20"
              fill="none"
            >
              <g clip-path="url(#clip0_5_1197)">
                <path
                  d="M3.53931 2.94092H6.31274C6.48603 2.94092 6.63013 3.08501 6.63013 3.2583C6.63017 4.29735 6.79523 5.29656 7.10278 6.22998H7.10376C7.14019 6.34588 7.11387 6.46889 7.02271 6.56006L5.0354 8.54736L5.19165 8.85498C6.37901 11.1885 8.29128 13.0923 10.6223 14.2866L10.9299 14.4438L11.175 14.1997L12.9192 12.4556C13.0051 12.3698 13.1316 12.3426 13.2366 12.3784L13.2415 12.3804C14.1772 12.6895 15.1873 12.856 16.2209 12.856C16.3941 12.8562 16.5373 13.0002 16.5374 13.1733V15.9399C16.5371 16.1129 16.3939 16.2561 16.2209 16.2563C9.04118 16.2563 3.22212 10.438 3.22192 3.2583C3.22192 3.08501 3.36602 2.94092 3.53931 2.94092Z"
                  fill="white"
                  stroke="white"
                  stroke-width="0.951123"
                />
              </g>
              <defs>
                <clipPath id="clip0_5_1197">
                  <rect
                    width="19.0225"
                    height="19.0225"
                    fill="white"
                    transform="translate(0.180908 -0.00244141)"
                  />
                </clipPath>
              </defs>
            </svg>
            <span>(978) 963-8949</span>
          </div>
          <div class="contact-item">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 20 20"
              fill="none"
            >
              <path
                d="M3.54346 4.10596H16.2251C17.097 4.10596 17.8103 4.8193 17.8103 5.69116V15.2024C17.8103 16.0743 17.097 16.7876 16.2251 16.7876H3.54346C2.67159 16.7876 1.95825 16.0743 1.95825 15.2024V5.69116C1.95825 4.8193 2.67159 4.10596 3.54346 4.10596Z"
                stroke="white"
                stroke-width="1.90225"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                d="M17.8103 5.69287L9.88428 11.2411L1.95825 5.69287"
                stroke="white"
                stroke-width="1.90225"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
            <span>
              <a href="mailto:info@techedproducts.com?subject=Website Inquiry">
                info@techedproducts.com
              </a>
            </span>
          </div>
        </div>
      </nav>
      <nav class="five-col-grid">
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
      </nav>

      <div class="footer-bottom">©2025 - TechEd | All right reserved</div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
  .base-footer {
    background: var(--darkblue);
    color: var(--offwhite);
    padding: 50px 0;
    text-align: center;
  }

  .branding {
    align-self: center;
  }

  .branding-logo {
    margin: 0 auto;
    width: 69px;
    height: 69px;
    aspect-ratio: 1/1;
  }

  .social {
    display: flex;
    gap: 15px;
    padding: 24px 0 0;

    > a {
      width: 33.289px;
      height: 33.289px;
      padding: 7px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 50px;
      border: 2px solid rgba(255, 255, 255, 0.2);
      transition:
        border-color 0.3s ease,
        transform 0.3s ease;

      img {
        transition: transform 0.3s ease;
      }

      &:hover {
        border-color: var(--white);
        transform: scale(1.1);

        img {
          transform: scale(1.1);
        }
      }
    }
  }

  .contact {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    padding: 20px 0 0;

    .contact-item {
      display: flex;
      align-items: center;
      gap: 5px;
    }

    svg {
      width: 20px;
      height: 20px;
      flex-shrink: 0;
    }
  }

  nav {
    margin: 0 auto 40px;
  }

  .footer-top {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 100%;
    padding: 0 0 40px;
    border-bottom: 1px solid var(--white);
  }

  .footer-bottom {
    padding-top: 40px;
    border-top: 1px solid rgba(255, 255, 255, 0.06);
  }

  .five-col-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 24px;

    .grid-item {
      display: flex;
      flex-direction: column;
      gap: 16px;

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
      grid-column: auto;

      display: flex;
      flex-direction: column;

      .partners-grid {
        display: grid;
        grid-template-columns: 1fr;
        gap: 16px;

        ul {
          margin: 0;
          padding: 0;
          list-style: none;
        }
      }
    }
  }

  @media (min-width: 1024px) {
    .base-footer {
      padding: 80px 0;
      text-align: left;
    }
    .footer-top {
      flex-direction: row;
    }
    .branding-logo {
      margin: 0;
    }
    .contact {
      padding: 0;
      align-items: flex-start;
      gap: 23px;
    }

    .five-col-grid {
      grid-template-columns: repeat(5, 1fr);
      gap: 40px;

      .partners {
        grid-column: 3 / 6; // spans columns 3,4,5

        .partners-grid {
          grid-template-columns: repeat(3, 1fr);
        }
      }
    }
  }
</style>
