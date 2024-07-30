<script lang="ts">
    import DFTFeature from './IntroDFTFeature.svelte';
    import BackgroundLines from './BackgroundLines.svelte';
    
    
    interface Feature {
      icon: string;
      title: string;
      description: string;
    }
    
    const features: Feature[] = [
      {
        icon: '/src/lib/img/clock.svg',
        title: "Immediacy",
        description: "Transactions with DFTs are processed swiftly, a stark contrast to the often-protracted procedures of conventional financing!",
      },
      {
        icon: '/src/lib/img/searchtick.svg',
        title: "Transparency",
        description: "Each transaction is recorded on a blockchain, offering an undisputable and clear record of transactions, accessible to all relevant parties!",
      },
      {
        icon: '/src/lib/img/securetick.svg',
        title: "Security",
        description: "Leveraging the robustness of blockchain technology, DFTs provide a secure environment for financial transactions, safeguarding against tampering and fraud.",
      },
    ];
    </script>
    
    <section class="flex flex-col justify-center pt-20">
      <section class="flex relative flex-col justify-center items-center px-16 py-20 w-full flex-shrink-0 max-md:px-5 max-md:max-w-full" style="background: linear-gradient(261deg, #05A987 2.74%, #024336 82.42%);">
        <BackgroundLines />
        <div class="relative w-full max-w-screen-xl max-md:max-w-full">
          <div class="flex gap-5 max-md:flex-col">
            <div class="flex flex-col w-[45%] max-md:ml-0 max-md:w-full">
              <div class="relative grow max-md:mt-10 max-md:max-w-full">
                <div class="flex gap-6 max-md:flex-col">
                  <div class="flex flex-col w-6/12 max-md:ml-0 max-md:w-full">
                    <div class="flex relative flex-col grow text-white max-md:mt-5">
                      <DFTFeature feature={features[0]} />
                      <DFTFeature feature={features[1]} />
                    </div>
                  </div>
                  <div class="flex flex-col ml-5 w-6/12 max-md:ml-0 max-md:w-full text-white">
                    <DFTFeature feature={features[2]} />
                  </div>
                </div>
              </div>
            </div>
            <div class="flex flex-col ml-5 w-[50%] max-md:ml-0 max-md:w-full px-20">
              <div class="flex relative flex-col self-stretch my-auto text-white max-md:mt-10 max-md:max-w-full">
                <h2 class="text-6xl font-medium leading-[66px] max-md:max-w-full max-md:text-4xl max-md:leading-[49px]">
                  Introducing DFT <br />Tokens
                </h2>
                <p class="mt-5 text-xl font-light tracking-wide leading-8 max-md:max-w-full">
                  DFTs represent a paradigm shift in supply chain finance, offering a digital, blockchain-based approach to managing and transferring value within the supply chain ecosystem.
                </p>
              </div>
            </div>
          </div>
        </div>
      </section>
    </section>