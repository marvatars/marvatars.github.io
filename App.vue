<template>
  <div class="bg-black">
    <div class="intro-bg">
      <section class="w-full">
        <div
          class="py-8 container flex flex-col flex-wrap items-center justify-between mx-auto md:flex-row max-w-8xl"
        >
          <div class="relative flex flex-col md:flex-row">
            <a
              href="https://marvatars.com"
              aria-current="page"
              class="flex items-center mb-5 font-medium lg:w-auto lg:items-center lg:justify-center md:mb-0 router-link-exact-active router-link-active"
              ><h2
                class="mx-auto text-7xl leading-none select-none mb-4 font-bold py-4 text-red-400"
              >
                Marvatars
              </h2></a
            >
          </div>
          <div class="inline-flex pb-8 md:pb-0">
            <nav
              class="flex flex-wrap items-center text-white text-2xl justify-center"
            >
              <a
                href="#mint"
                class="uppercase leading-6 hover:text-red-300 text-center px-4"
              >
                Mint
                <img class="w-20  m-auto" src="./images/fireline.png" />
              </a>
              <a
                href="#faqs"
                class="uppercase leading-6 hover:text-red-300 text-center px-4"
              >
                FAQs
                <img class="w-20  m-auto" src="./images/fireline.png" />
              </a>
              <a
                href="#charity"
                class="uppercase leading-6 hover:text-red-300 text-center px-4"
              >
                Charity
                <img class="w-20  m-auto" src="./images/fireline.png" />
              </a>
              <a
                href="#lotteries"
                class="uppercase leading-6 hover:text-red-300 text-center px-4"
              >
                Lotteries
                <img class="w-20  m-auto" src="./images/fireline.png" />
              </a>
            </nav>
          </div>
          <div class="inline-flex items-center lg:justify-end">
            <nav
              class="flex flex-wrap items-center text-base pb-4 justify-center"
            >
             <a
                href="http://t.me/marvatars"
                class="uppercase leading-6 hover:text-red-900"
                ><img
                  class="object-contain w-16 h-16"
                  src="./images/tg.png"
              /></a>
              <a
                href="https://twitter.com/marvatars"
                class="uppercase leading-6 hover:text-red-900"
                ><img
                  class="object-contain w-16 h-16"
                  src="./images/twitter.png"
              /></a>
              <a
                href="https://discord.gg/469FPhxKHQ"
                class="uppercase leading-6 hover:text-red-900"
                ><img
                  class="object-contain w-16 h-16"
                  src="./images/discord.png"
              /></a>
              <a
                href="https://etherscan.io/token/0x66769ffa5193e405f77fbb4b5ea1e807cfe4eaa5"
                class="uppercase leading-6 hover:text-red-900"
                ><img
                  class="object-contain w-16 h-16"
                  src="./images/etherscan.png"
              /></a>
              <a
                href="mailto:mail@marvatars.com"
                class="uppercase leading-6 hover:text-red-900"
                ><img class="object-contain w-16 h-16" src="./images/mail.png"
              /></a>
            </nav>
          </div>
        </div>
      </section>
      <section class="py-20 px-2 md:px-16 mx-auto max-w-7xl ">
        <div
          class="grid grid-cols-1 gap-0 text-gray-400 md:grid-cols-2 md:gap-16 text-xl"
        >
          <div class="my-16 intro-text">
            <p class="py-2 text-4xl">
              As the multiverse descends into chaos, the choice is yours! Are
              you the Harbinger of Doom or the Herald of Light?
            </p>

            <p class="py-8 intro-text text-4xl">Pick your side!</p>
            <a href="#">
              <button class="table-text classic-button">
                What's your Marvatar?
              </button>
            </a>
          </div>

          <div
            class="container max-w-4xl mx-auto flex px-5 py-5 items-center justify-center"
          >
            <video width="100%" height="100%" autoplay muted playsinline loop>
              <source src="./images/intro.mp4" type="video/mp4" />
              Your browser does not support the video tag.
            </video>
          </div>
        </div>
      </section>
    </div>
    <section class="px-2 md:px-16 py-20 mx-auto max-w-7xl">
      <h2 class="mb-4 text-5xl md:text-7xl font-bold py-10 text-red-400">
        Marvatars Roadmap
      </h2>

      <div class="grid grid-cols-1 gap-0 text-gray-400 ">
        <div class="text-xl my-8">
          <p class="text-center table-text text-white text-3xl">
            Marvatars - Coming To You In 3 Phases
          </p>
          <img
            class="object-contain w-auto m-auto"
            src="./images/roadmap.png"
          />
        </div>
      </div>
    </section>

    <section id="mint" class="px-2 md:px-16 py-20 mx-auto max-w-7xl">
      <h2 class="mb-4 text-5xl md:text-7xl font-bold py-10 text-red-400">
        Mint your Marvatars
      </h2>

      <div
        class="grid grid-cols-1 gap-0 text-gray-400 md:grid-cols-2 md:gap-16 "
      >
        <div class="text-xl my-8">
          <h3 class="text-2xl lg:text-3xl text-white font-bold p-4 table-text">
            Minting Details
            <img class="w-60 md:w-80" src="./images/fireline.png" />
          </h3>
          <ul class="px-8 ">
            <li>0.08 Eth per mint and a maximum of 5 mints per transaction</li>
            <li>
              Marvatars are revealed 3 days after the start of the sale, or as
              soon as all the Marvatars are sold out
            </li>
            <li>
              Unsold Marvatars can be minted until 7 days from the start of the
              sale
            </li>
            <li>All unsold Marvatars are burnt 7 days after the sale</li>
          </ul>
        </div>

        <div>
          <img
            class="object-contain w-3/4 p-4 m-auto"
            src="./images/card.png"
          />
          <div class="">
            <div
              class="relative flex flex-col sm:flex-row sm:space-x-4"
              v-if="saleopen"
            >
              <a @click="fund">
                <button class="table-text classic-button text-xl">
                  MINT @ {{ nft_price }} ETH
                </button>
              </a>
            </div>

            <h1
              class="text-center table-text text-5xl font-extrabold tracking-tight text-gray-900 py-16"
            >
              <span class="block xl:inline text-red-900">Sold : </span>
              <span class="block text-red-600 xl:inline"
                >{{ totalSupply }} / 2520</span
              >
            </h1>
          </div>
        </div>

        <div class="text-xl my-8">
          <h3 class="text-2xl md:text-3xl text-white font-bold p-4 table-text">
            Minting Rewards
            <img class="w-60 md:w-80" src="./images/fireline.png" />
          </h3>

          <ul class="px-8 ">
            <li>
              Mythic card holders from Phase 1 are airdropped random unrevealed
              Marvheros NFTs (Phase 2)!
            </li>
            <li>
              Mythic card holders from Phase 2 are airdropped random unrevealed
              Marvellous NFTs (Phase 3)!
            </li>
            <li>
              Minting 5 in a single transaction rewards you a 6th Marvatar for
              free!
            </li>
          </ul>
        </div>
        <div>
          <img
            class="object-contain w-auto p-8 m-auto mt-32"
            src="./images/cards.png"
          />
        </div>
      </div>
    </section>

    <section class="px-0 md:px-2 md:px-16 py-20 mx-auto max-w-7xl">
      <h2 class="mb-4 text-5xl md:text-7xl font-bold py-10 text-red-400">
        Mint Breakdown
      </h2>

      <div class="grid grid-cols-1 gap-0 text-gray-400">
        <div>
          <table
            class="table-auto text-center table-text text-sm md:text-xl m-auto"
          >
            <thead>
              <tr class="h-16">
                <th class="w-32 md:w-64">
                  Rarity
                  <img
                    class=" w-20 md:w-32 m-auto"
                    src="./images/fireline.png"
                  />
                </th>
                <th class="w-32 md:w-64">
                  Badges
                  <img
                    class=" w-20 md:w-32 m-auto"
                    src="./images/fireline.png"
                  />
                </th>
                <th class="w-32 md:w-64">
                  Mints
                  <img
                    class=" w-20 md:w-32 m-auto"
                    src="./images/fireline.png"
                  />
                </th>
              </tr>
            </thead>
            <tbody>
              <tr class="h-16">
                <td>Mythic</td>
                <td>
                  <img
                    class="object-contain w-12 md:w-24 m-auto"
                    src="./images/mythic.png"
                  />
                </td>
                <td>120</td>
              </tr>

              <tr class="h-16">
                <td>Legendary</td>
                <td>
                  <img
                    class="object-contain w-12 md:w-24 m-auto"
                    src="./images/legendary.png"
                  />
                </td>
                <td>240</td>
              </tr>

              <tr class="h-16">
                <td>Epic</td>
                <td>
                  <img
                    class="object-contain w-12 md:w-24 m-auto"
                    src="./images/epic.png"
                  />
                </td>
                <td>360</td>
              </tr>

              <tr class="h-16">
                <td>Rare</td>
                <td>
                  <img
                    class="object-contain w-12 md:w-24 m-auto"
                    src="./images/rare.png"
                  />
                </td>
                <td>480</td>
              </tr>

              <tr class="h-16">
                <td>Uncommon</td>
                <td>
                  <img
                    class="object-contain w-12 md:w-24 m-auto"
                    src="./images/uncommon.png"
                  />
                </td>
                <td>600</td>
              </tr>

              <tr class="h-16">
                <td>Common</td>
                <td>
                  <img
                    class="object-contain w-12 md:w-24 m-auto"
                    src="./images/common.png"
                  />
                </td>
                <td>720</td>
              </tr>
            </tbody>
          </table>

          <h2
            class="mb-4 text-2xl md:text-5xl font-bold py-10 text-red-400 text-center"
          >
            Total Marvillians: 2520
          </h2>
        </div>
      </div>
    </section>

    <section id="charity" class="px-2 md:px-16 py-20 mx-auto max-w-7xl">
      <h2 class="mb-4 text-5xl md:text-7xl font-bold py-10 text-red-400">
        Charity & Donations
      </h2>

      <div class="grid grid-cols-1 gap-0 text-gray-400 text-sm md:text-xl">
        <div>
          <p class="py-3">
            As per our belief system, everything has to be for a cause. The same
            applies to our NFTs as well!
          </p>
          <p class="py-3">
            The end game for out team is to establish a foundation for children
            off the street; to provide them with the care and support that every
            child needs to live the life of their dreams! But that is our end
            game, there are so many such organisations already striving hard to
            achieve the exact same goal! And our intention is to help them in
            the meanwhile as at the end we are all on the same team!
          </p>

          <table
            class="table-fixed text-center table-text text-sm md:text-xl mx-auto my-8"
          >
            <tbody>
              <tr class="h-16">
                <td class="md:px-8">
                  <img class="w-16 md:w-32 pb-8" src="./images/20pb.png" />
                </td>
                <td class="p-2">
                  20%
                </td>
                <td class="p-2">1 ETH donation!</td>
              </tr>

              <tr class="h-16">
                <td class="md:px-8">
                  <img class="w-16 md:w-32 pb-8" src="./images/40pb.png" />
                </td>
                <td class="md:px-8">
                  40%
                </td>
                <td class="md:px-8">2 ETH donation!</td>
              </tr>
              <tr class="h-16">
                <td class="md:px-8">
                  <img class="w-16 md:w-32 pb-8" src="./images/60pb.png" />
                </td>
                <td class="md:px-8">
                  60%
                </td>
                <td class="md:px-8">3 ETH donation!</td>
              </tr>
              <tr class="h-16">
                <td class="md:px-8">
                  <img class="w-16 md:w-32 pb-8" src="./images/80pb.png" />
                </td>
                <td class="md:px-8">
                  80%
                </td>
                <td class="md:px-8">4 ETH donation!</td>
              </tr>
              <tr class="h-16">
                <td class="md:px-8">
                  <img class="w-16 md:w-32 pb-8" src="./images/100pb.png" />
                </td>
                <td class="md:px-8">
                  100%
                </td>
                <td class="md:px-8">5 ETH donation!</td>
              </tr>
            </tbody>
          </table>

          <p class="py-3">
            If you own a charity or wish to nominate a charity that needs
            support, please drop our team an email on
            <a href="mailto:mail@marvatars.commail@marvatars.com"
              >mail@marvatars.com</a
            >. Holding a Marvatar would be mandatory to be eligible to nominate,
            hence you will need to provide proof of ownership.
          </p>
          <p class="py-3">
            At the end of the sale, a consolidated list of charities will be
            published based on the community nominations including some of the
            charities that we have considered. There will be 5 rounds of voting,
            based on the progress of the mint sale (20%, 40%, 60%, 90% & 100%).
            The charity with the maximum number of votes at the end of the
            voting period for each of the rounds will receive the respective
            donations at the end of the sale period.
          </p>
        </div>
      </div>
    </section>

    <section id="lotteries" class="px-2 md:px-16 py-20 mx-auto max-w-7xl">
      <h2 class="mb-4 text-5xl md:text-7xl font-bold py-10 text-red-400">
        Lotteries!!!
      </h2>

      <div class="grid grid-cols-1 gap-0 text-gray-400 text-sm md:text-xl">
        <div>
          <p class="py-3">
            With Marvatars, EVERYONE WINS!!
          </p>
          <p class="py-3">
            Every Marvatar holder is eligible for a lottery based on the
            progress of the sale as listed below
          </p>
          <ul class="list-disc px-8">
            <li>20% Minted – 1 winner selected for 1000 USDT</li>
            <li>40% Minted – 2 winners selected for 1000 USDT each</li>
            <li>60% Minted – 3 winners selected for 1000 USDT each</li>
            <li>80% Minted – 4 winners selected for 1000 USDT each</li>
            <li>100% Minted – 5 winners selected for 1000 USDT each</li>
          </ul>
          <p class="py-3">
            But being able to do that needs your support, hence we have broken
            down our milestones based on the mint progression as below:
          </p>

          <p class="py-3">
            There will be 5 snapshots taken of the wallet addresses holding at
            least 1 Marvatar at 20%, 40%, 60%, 80% and 100% of the mint
            progress. The winning addresses will be announced on our Twitter
            page at the end of the sale. So please make sure you like and follow
            our Twitter:
            <a class="break-words" href="https://twitter.com/marvatars"
              >https://twitter.com/marvatars</a
            >
          </p>
          <p class="py-3">
            The funds will be distributed to the winning ERC20 addresses at the
            end of the sale.
          </p>
        </div>
      </div>
    </section>

    <section id="faqs" class="px-2 md:px-16 py-20 mx-auto max-w-7xl">
      <h2 class="mb-4 text-5xl md:text-7xl font-bold py-10 text-red-400">
        FAQs
      </h2>

      <div class="grid grid-cols-1 gap-0 text-gray-400 text-md md:text-xl">
        <div>
          <div class="tabs">
            <div class="tab">
              <input type="checkbox" id="chck1" />
              <label class="tab-label" for="chck1"
                >What is the cost to mint a Marvatar</label
              >
              <div class="tab-content">
                0.08 ETH per Mint
              </div>
            </div>
            <div class="tab">
              <input type="checkbox" id="chck2" />
              <label class="tab-label" for="chck2"
                >When is the date of the sale? When will the Marvatars be
                revealed?</label
              >
              <div class="tab-content">
                The sale for the first Edition of Marvatars – Marvillains, will
                happen in the first week of October • The Marvatars will be
                revealed 3 days after the start of the sale, or as soon as all
                the Marvatars in the edition are sold • The sale for the second
                Edition of Marvatars – Marveroes, will happen in the third week
                of October • The sale for the third Edition of Marvatars –
                Marvellous, will happen in early November, dates to be announced
                soon!
              </div>
            </div>

            <div class="tab">
              <input type="checkbox" id="chck3" />
              <label class="tab-label" for="chck3">
                When are the next phases expected?</label
              >
              <div class="tab-content">
                The sale for phase 2 (Marveroes Edition) will be 2 weeks from
                the sale date for Phase 1 (Marvillains Edition) • The sale for
                phase 3 (Marvellous Edition) will be 2 weeks from the sale date
                for Phase 2 (Marveroes Edition)
              </div>
            </div>

            <div class="tab">
              <input type="checkbox" id="chck4" />
              <label class="tab-label" for="chck4"
                >Which charities would be considered for the donations?</label
              >
              <div class="tab-content">
                The end game for our team is to build a residential school to
                provide a foundation and launch pad for children off the street
                with no support system. But in the meanwhile, as the mint
                progresses, the focus will be to help existing charities that
                support children
              </div>
            </div>

            <div class="tab">
              <input type="checkbox" id="chck5" />
              <label class="tab-label" for="chck5"
                >Can I nominate my own charity?</label
              >
              <div class="tab-content">
                Absolutely!! Anyone who owns a Marvatar is eligible to nominate
                a charity for the donations !
              </div>
            </div>

            <div class="tab">
              <input type="checkbox" id="chck6" />
              <label class="tab-label" for="chck6"
                >When will the lottery rewards be distributed? Do I have to do
                anything?</label
              >
              <div class="tab-content">
                Lottery rewards will be automatically distributed to the winning
                lottery addresses at the end of the sale. The winning addresses
                will be published on our Twitter feed. And, Nope! You don’t need
                to do anything! Congratulations!
              </div>
            </div>

            <div class="tab">
              <input type="checkbox" id="chck7" />
              <label class="tab-label" for="chck7"
                >How do you select the charity?</label
              >
              <div class="tab-content">
                A consolidated list of charities will be published based on the
                community nominations including some of the charities that we
                have considered. There will be multiple rounds of votes, based
                on the progress of the mint sale (10%, 25%, 50%, 100%). The
                charity with the maximum number of votes at the end of the
                voting period will receive the respective donations.
              </div>
            </div>

            <div class="tab">
              <input type="checkbox" id="chck8" />
              <label class="tab-label" for="chck8"
                >How do I nominate a charity of my choice for
                consideration?</label
              >
              <div class="tab-content">
                If you own a charity or wish to nominate a charity that needs
                support, please drop our team an email on mail@marvatars.com.
                Holding a Marvatar would be mandatory to be eligible to
                nominate, hence you will need to provide proof of ownership.
              </div>
            </div>

            <div class="tab">
              <input type="checkbox" id="chck9" />
              <label class="tab-label" for="chck9">
                When will the donations be distributed to the charities?</label
              >
              <div class="tab-content">
                Till what date can the Marvatars be minted? What happens to the
                unsold Marvatars?
              </div>
            </div>

            <div class="tab">
              <input type="checkbox" id="chck10" />
              <label class="tab-label" for="chck10">
                The donations will be distributed after the sales of each
                edition</label
              >
              <div class="tab-content">
                Marvatars can be minted till 7 days from the start of the sale •
                After the 7 days, all unsold Marvatars will be burnt, hence
                increasing the rarity of the Marvatars already sold
              </div>
            </div>

            <div class="tab">
              <input type="checkbox" id="chck11" />
              <label class="tab-label" for="chck11">
                How many Marvatars are available? How many can I hold? How many
                can I mint per transaction?</label
              >
              <div class="tab-content">
                2520 Marvatars are available in Phase 1, of which 120 would be
                used for marketing and giveaways. • There is no limit to how
                many Marvatars you can hold! • You can mint up to 5 Marvatars
                per transaction. Minting 5 in a transaction gives you a 6th for
                FREE!!
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="team" class="px-2 md:px-16 py-20 mx-auto max-w-7xl">
      <h2 class="mb-4 text-5xl md:text-7xl font-bold py-10 text-red-400">
        The Team
      </h2>
      <div
        class="grid w-full grid-cols-1 sm:grid-cols-3 text-red-400 text-xl table-text"
      >
        <div class="flex flex-col items-center justify-center col-span-1 ">
          <div class="relative">
            <img
              class="relative z-20 w-full rounded-full avatar"
              src="./images/Beardo.png"
            />
          </div>
          <div class="mt-3 space-y-2 text-center">
            <div class="space-y-1 text-lg font-medium leading-6">
              <h2 class="text-red-100 text-5xl">Beardo</h2>
            </div>
          </div>
        </div>

        <div class="flex flex-col items-center justify-center col-span-1">
          <div class="relative">
            <img
              class="relative z-20 w-full rounded-full"
              src="./images/Titan.png"
            />
          </div>
          <div class="mt-3 space-y-2 text-center">
            <div class="space-y-1 text-lg font-medium leading-6">
              <h2 class="text-red-100 text-5xl">Titan</h2>
            </div>
          </div>
        </div>

        <div class="flex flex-col items-center justify-center col-span-1">
          <div class="relative">
            <img
              class="relative z-20 w-full rounded-full"
              src="./images/Oracle.png"
            />
          </div>
          <div class="mt-3 space-y-2 text-center">
            <div class="space-y-1 text-lg font-medium leading-6">
              <h2 class="text-red-100 text-5xl">Oracle</h2>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class=" py-16 footer">
      <div
        class="flex flex-col flex-wrap items-center justify-between mx-auto md:flex-row md:mx-16"
      >
        <div class="relative flex flex-col md:flex-row">
          <a
            href="https://marvatars.com"
            aria-current="page"
            class="flex items-center mb-5 font-medium lg:w-auto lg:items-center lg:justify-center md:mb-0 router-link-exact-active router-link-active"
            ><h2
              class="mx-auto text-5xl leading-none select-none mb-4 font-bold py-10 text-red-400"
            >
              Marvatars
            </h2></a
          >
        </div>
        <div class="inline-flex items-center">
          <nav class="flex flex-wrap items-center">
           <a
              href="http://t.me/marvatars"
              class="uppercase leading-6 hover:text-red-900"
              ><img class="object-contain w-16 h-16" src="./images/tg.png"
            /></a>
            <a
              href="https://twitter.com/marvatars"
              class="uppercase leading-6 hover:text-red-900"
              ><img class="object-contain w-16 h-16" src="./images/twitter.png"
            /></a>
            <a
              href="https://discord.gg/469FPhxKHQ"
              class="uppercase leading-6 hover:text-red-900"
              ><img class="object-contain w-16 h-16" src="./images/discord.png"
            /></a>
            <a
              href="https://etherscan.io/token/0x66769ffa5193e405f77fbb4b5ea1e807cfe4eaa5"
              class="uppercase leading-6 hover:text-red-900"
              ><img
                class="object-contain w-16 h-16"
                src="./images/etherscan.png"
            /></a>
            <a
              href="mailto:mail@marvatars.com"
              class="uppercase leading-6 hover:text-red-900"
              ><img class="object-contain w-16 h-16" src="./images/mail.png"
            /></a>
          </nav>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import { ethers } from "ethers";
import { formatEther } from "ethers/lib/utils";

import ABI from "./abi.json";

export default {
  data() {
    return {
      nft_price: 0,
      totalSupply: 0,
      ethw: false,
      saleopen: false,
    };
  },
  methods: {
    async fund() {
      const amountOfNFT = prompt(
        "How much NFTs you want to mint ? (5 Maximum)",
        5
      );

      const accounts = await window.ethereum.request({
        method: "eth_requestAccounts",
      });
      console.log("User : " + accounts[0]);

      var provider = await new ethers.providers.Web3Provider(window.ethereum);
      var signer = await provider.getSigner();

      const runx = new ethers.Contract(
        "0x66769ffa5193e405f77fbb4b5ea1e807cfe4eaa5",
        ABI,
        signer
      );
      const nft_price = (await runx.NFT_PRICE()) * amountOfNFT;
      console.log(nft_price.toString());

      const done = await runx.mint(amountOfNFT, {
        value: nft_price.toString(),
        gasLimit: 388475,
      });

      console.log(done);
    },

    async fetchdata() {
      var provider = await new ethers.providers.getDefaultProvider();

      const gamex = await new ethers.Contract(
        "0x66769ffa5193e405f77fbb4b5ea1e807cfe4eaa5",
        ABI,
        provider
      );

      const nft_price = await gamex.NFT_PRICE();

      this.totalSupply = await gamex.totalSupply();
      this.saleopen = await gamex.saleIsActive();
      this.nft_price = parseFloat(formatEther(nft_price));
    },
  },
  async mounted() {
    this.ethw = window.ethereum;

    this.fetchdata();

    window.setInterval(() => {
      this.fetchdata();
    }, 19000);
  },
};
</script>

<style>
@font-face {
  font-family: "Harlow";
  src: local("Harlow"), url(./fonts/Harlow-Solid-Italic.ttf) format("truetype");
}

@font-face {
  font-family: "Squartiqa4F";
  src: local("Squartiqa4F"), url(./fonts/Squartiqa4F.ttf) format("truetype");
}

@font-face {
  font-family: "SirinStencil";
  src: local("SirinStencil"),
    url(./fonts/SirinStencil-Regular.ttf) format("truetype");
}

html {
  scroll-behavior: smooth;
  background: black;
  font-family: "Squartiqa4F", "Open Sans", sans-serif;
}
h2 {
  font-family: Harlow, sans-serif;
  text-shadow: 1px 1px 2px black, 0 0 1em #ff7979, 0 0 0.2em #ff7979;
  color: #b33939;
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: #ffb142;
  -webkit-text-fill-color: #b33939;
}

.table-text {
  font-family: Squartiqa4F, sans-serif;
}

.intro-text {
  font-family: SirinStencil, sans-serif;
}

/* Accordion styles */
input {
  position: absolute;
  opacity: 0;
  z-index: -1;
}
.tabs {
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 4px 4px -2px rgba(0, 0, 0, 0.5);
}
.tab {
  width: 100%;
  color: white;
  overflow: hidden;
}
.tab-label {
  display: flex;
  justify-content: space-between;
  padding: 1em;
  background: #191919;
  font-weight: bold;
  cursor: pointer;
  position: relative;
  padding-right: 36px;
  /* Icon */
}
.tab-label:hover {
  background: #191919;
}
.tab-label::after {
  content: "";
  transition: all 0.35s;
  height: 40px;
  width: 40px;
  top: 16px;
  right: 0;
  position: absolute;
  background-image: url("./images/faqicon.png");
}
.tab-content {
  max-height: 0;
  padding: 0 1em;
  color: #f9f9f9;
  background: black;
  transition: all 0.35s;
}
.tab-close {
  display: flex;
  justify-content: flex-end;
  padding: 1em;
  font-size: 0.75em;
  background: #2c3e50;
  cursor: pointer;
}
.tab-close:hover {
  background: #1a252f;
}
input:checked + .tab-label {
  background: #1a252f;
}
input:checked + .tab-label::after {
  transform: rotate(90deg);
}
input:checked ~ .tab-content {
  max-height: 100vh;
  padding: 1em;
}

li {
  position: relative;
  list-style-type: none;
  padding-left: 16px;
  padding-bottom: 8px;
}

li:before {
  content: "";
  position: absolute;
  top: -4px;
  left: -24px;
  width: 36px;
  height: 36px;
  background-image: url("./images/fist.png");
}

.footer {
  background: url("./images/footer-line.png") repeat-x bottom center;
  background-size: contain;
}

.intro-bg {
  background: url("./images/bg.jpg") repeat-x bottom center;
  background-size: cover;
}

.classic-button {
  width: 280px;
  height: 160px;
  padding: 16px 32px;
  text-align: left;
  color: #fff;
  background: url("./images/button.png") center center;
  background-size: cover;
}

@media only screen and (device-width: 390px) and (device-height: 844px) and (-webkit-device-pixel-ratio: 3) {
  .classic-button {
    width: 80px;
  }
}
</style>
