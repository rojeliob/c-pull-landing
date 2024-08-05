<script setup>
import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <nav class="bg-gray-800">
    <div class="max-w-8xl px-2 sm:px-6 lg:px-8">
      <div class="relative flex h-16 items-center justify-between">
        <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
          <!-- Mobile menu button-->
          <button
            type="button"
            class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
            aria-controls="mobile-menu"
            aria-expanded="false"
          >
            <span class="absolute -inset-0.5"></span>
            <span class="sr-only">Open main menu</span>
            <!--
            Icon when menu is closed.

            Menu open: "hidden", Menu closed: "block"
          -->
            <svg
              class="block h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
              />
            </svg>
            <!--
            Icon when menu is open.

            Menu open: "block", Menu closed: "hidden"
          -->
            <svg
              class="hidden h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
        <div
          class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start"
        >
          <div class="flex flex-shrink-0 items-center text-white">
            C-PULL
            <!-- <img
              class="h-8 w-auto"
              src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=500"
              alt="Your Company"
            /> -->
          </div>
          <div class="hidden sm:ml-6 sm:block">
            <div class="flex space-x-4">
              <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
              <a
                href="#"
                class="rounded-md bg-gray-900 px-3 py-2 text-sm font-medium text-white"
                aria-current="page"
                >Home</a
              >
              <a
                href="#"
                class="rounded-md px-3 py-2 text-sm font-medium text-gray-300 hover:bg-gray-700 hover:text-white"
                >Business</a
              >
              <a
                href="#"
                class="rounded-md px-3 py-2 text-sm font-medium text-gray-300 hover:bg-gray-700 hover:text-white"
                >Contact</a
              >
              <a
                href="#"
                class="rounded-md px-3 py-2 text-sm font-medium text-gray-300 hover:bg-gray-700 hover:text-white"
                >About us</a
              >
            </div>
          </div>
        </div>
        <div
          class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0"
        >
          <button
            type="button"
            class="relative rounded-full bg-gray-800 p-1 text-gray-400 hover:text-white focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800"
          >
            <span class="absolute -inset-1.5"></span>
            <span class="sr-only">View notifications</span>
            <svg
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0"
              />
            </svg>
          </button>

          <!-- Profile dropdown -->
          <div class="relative ml-3">
            <div>
              <button
                type="button"
                class="relative flex rounded-full bg-gray-800 text-sm focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800"
                id="user-menu-button"
                aria-expanded="false"
                aria-haspopup="true"
              >
                <span class="absolute -inset-1.5"></span>
                <span class="sr-only">Open user menu</span>
                <img
                  class="h-8 w-8 rounded-full"
                  src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                  alt=""
                />
              </button>
            </div>

            <!--
            Dropdown menu, show/hide based on menu state.

            Entering: "transition ease-out duration-100"
              From: "transform opacity-0 scale-95"
              To: "transform opacity-100 scale-100"
            Leaving: "transition ease-in duration-75"
              From: "transform opacity-100 scale-100"
              To: "transform opacity-0 scale-95"
          -->
            <!-- Active: "bg-gray-100", Not Active: "" -->

            <!-- <div
              class="absolute right-0 z-10 mt-2 w-48 origin-top-right rounded-md bg-white py-1 shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
              role="menu"
              aria-orientation="vertical"
              aria-labelledby="user-menu-button"
              tabindex="-1"
              disabled
            >
              <a
                href="#"
                class="block px-4 py-2 text-sm text-gray-700"
                role="menuitem"
                tabindex="-1"
                id="user-menu-item-0"
                >Your Profile</a
              >
              <a
                href="#"
                class="block px-4 py-2 text-sm text-gray-700"
                role="menuitem"
                tabindex="-1"
                id="user-menu-item-1"
                >Settings</a
              >
              <a
                href="#"
                class="block px-4 py-2 text-sm text-gray-700"
                role="menuitem"
                tabindex="-1"
                id="user-menu-item-2"
                >Sign out</a
              >
            </div> -->
          </div>
        </div>
      </div>
    </div>

    <!-- Mobile menu, show/hide based on menu state. -->
    <div class="sm:hidden" id="mobile-menu">
      <div class="space-y-1 px-2 pb-3 pt-2">
        <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
        <a
          href="#"
          class="block rounded-md bg-gray-900 px-3 py-2 text-base font-medium text-white"
          aria-current="page"
          >Dashboard</a
        >
        <a
          href="#"
          class="block rounded-md px-3 py-2 text-base font-medium text-gray-300 hover:bg-gray-700 hover:text-white"
          >Team</a
        >
        <a
          href="#"
          class="block rounded-md px-3 py-2 text-base font-medium text-gray-300 hover:bg-gray-700 hover:text-white"
          >Projects</a
        >
        <a
          href="#"
          class="block rounded-md px-3 py-2 text-base font-medium text-gray-300 hover:bg-gray-700 hover:text-white"
          >Calendar</a
        >
      </div>
    </div>
  </nav>
  <!-- Home Section -->
  <section class="container mx-auto p-8 flex flex-wrap lg:flex-nowrap">
    <!-- Left Column -->
    <div
      class="flex flex-col justify-center items-center lg:items-start lg:w-1/2 p-4 space-y-4"
    >
      <h1 class="text-4xl font-bold text-teal-400">Liquidez rápida</h1>
      <h2 class="text-2xl font-semibold text-white">Sin complicaciones</h2>
      <p class="text-white text-center lg:text-left">
        Facilitamos el acceso a fondos y simplificamos la administración
        financiera de tu empresa.
      </p>
      <a
        href="#"
        class="px-6 py-2 bg-white text-gray-600 font-semibold rounded hover:bg-blue-600"
        >Regístrate</a
      >
    </div>

    <!-- Right Column -->
    <div class="lg:w-1/2 p-4">
      <img
        src="/images/home-cpull.png"
        alt="Example Image"
        class="w-full h-auto object-cover rounded-lg shadow-lg"
      />
    </div>
  </section>

  <section class="container mx-auto p-8">
    <h2 class="text-3xl font-bold text-white text-center mb-8">
      Cómo funciona
    </h2>
    <div class="relative">
      <div class="flex items-center justify-between relative">
        <!-- Step 1 -->
        <div class="flex flex-col items-center w-1/5">
          <div
            class="w-12 h-12 flex items-center justify-center bg-white text-black font-bold rounded-full"
          >
            1
          </div>
          <h3 class="mt-4 text-xl font-semibold text-white">Registrate</h3>
          <p class="text-white">Completa los datos de tu empresa</p>
        </div>
        <!-- Connector Line -->
        <div class="flex-1 border-t-2 border-gray-300 relative">
          <div
            class="absolute inset-y-1/2 w-full border-t-2 border-gray-300"
          ></div>
        </div>
        <!-- Step 2 -->
        <div class="flex flex-col items-center w-1/5">
          <div
            class="w-12 h-12 flex items-center justify-center bg-white text-black font-bold rounded-full"
          >
            2
          </div>
          <h3 class="mt-4 text-xl font-semibold text-white">
            Sube tus documentos
          </h3>
          <p class="text-white">¡Solo debes hacerlo una vez!</p>
        </div>
        <!-- Connector Line -->
        <div class="flex-1 border-t-2 border-gray-300 relative">
          <div
            class="absolute inset-y-1/2 w-full border-t-2 border-gray-300"
          ></div>
        </div>
        <!-- Step 3 -->
        <div class="flex flex-col items-center w-1/5">
          <div
            class="w-12 h-12 flex items-center justify-center bg-white text-black font-bold rounded-full"
          >
            3
          </div>
          <h3 class="mt-4 text-xl font-semibold text-white">
            Solicita tu préstamo
          </h3>
          <p class="text-white">
            Descubre las condiciones que te ofrece cada entidad bancaria
          </p>
        </div>
      </div>
    </div>
  </section>

  <section class="container mx-auto p-8 mt-10">
    <h2 class="text-4xl font-bold text-white text-center mb-8">
      ¡Encuentra la financiación perfecta! Accede a múltiples bancos, compara y
      elige la mejor opción.
    </h2>

    <div className="grid grid-cols-5 grid-rows-6 gap-4">
      <div className="col-span-2 row-span-2 bg-black">
        <img
          class="w-full h-full"
          src="https://s3-alpha-sig.figma.com/img/34f8/65ac/1bd136173da00b5ff18ee5c38b53b2a9?Expires=1722211200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=Dc~OPJJKtnRlJpSKwX7RNlmDzD2AVTf07dikFBGmX0sVBHTT0GvaOICNKFxmoV3o1NluRA1kW1k0aptxzMZjC7vllcDN8aaWikVccgCmuNGg3PGGZSeTNIXnk63CR2MeeFi4CwVqotIZ9BpkcDWBxJ5ZwiLRHslUEQTmNJZfYabUPjX2epM7f6ii93cdVyCVFzB-0C~PxnrUpBSh4lThV9jUQi100CRfo5clrxBiTvJ4Es3pHj8f2-Z~A3-CvmYdQokq7z7tKg1jvVlrotjMwDv1cZ1zFuhNHv0t5nQdqYtGR7tKbDZNXTPb8gwsjVljz2i6sQez~4XvDiXoRmiA1w__"
          alt="Sunset in the mountains"
        />
      </div>
      <div className="col-start-3 bg-white">
        <div class="max-w-sm rounded overflow-hidden shadow-lg">
          <!-- <img
            class="w-full"
            src="/img/card-top.jpg"
            alt="Sunset in the mountains"
          /> -->
          <div class="px-6 py-4">
            <div class="font-bold text-xl mb-2">The Coldest Sunset</div>
            <p class="text-gray-700 text-base">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Voluptatibus quia, nulla! Maiores et perferendis eaque,
              exercitationem praesentium nihil.
            </p>
          </div>
        </div>
      </div>
      <div className="col-start-4 bg-white">
        <div class="max-w-sm rounded overflow-hidden shadow-lg">
          <!-- <img
            class="w-full"
            src="/img/card-top.jpg"
            alt="Sunset in the mountains"
          /> -->
          <div class="px-6 py-4">
            <div class="font-bold text-xl mb-2">The Coldest Sunset</div>
            <p class="text-gray-700 text-base">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Voluptatibus quia, nulla! Maiores et perferendis eaque,
              exercitationem praesentium nihil.
            </p>
          </div>
        </div>
      </div>
      <div className="col-start-5 bg-white">
        <div class="max-w-sm rounded overflow-hidden shadow-lg">
          <!-- <img
            class="w-full"
            src="/img/card-top.jpg"
            alt="Sunset in the mountains"
          /> -->
          <div class="px-6 py-4">
            <div class="font-bold text-xl mb-2">The Coldest Sunset</div>
            <p class="text-gray-700 text-base">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Voluptatibus quia, nulla! Maiores et perferendis eaque,
              exercitationem praesentium nihil.
            </p>
          </div>
        </div>
      </div>
      <div className="col-span-3 row-span-3 col-start-3 row-start-2 bg-white">
        <div class="max-w-sm rounded overflow-hidden shadow-lg">
          <!-- <img
            class="w-full"
            src="/img/card-top.jpg"
            alt="Sunset in the mountains"
          /> -->
          <div class="px-6 py-4">
            <div class="font-bold text-xl mb-2">The Coldest Sunset</div>
            <p class="text-gray-700 text-base">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Voluptatibus quia, nulla! Maiores et perferendis eaque,
              exercitationem praesentium nihil.
            </p>
          </div>
        </div>
      </div>
      <div className="col-span-2 row-span-2 row-start-3 bg-white">
        <div class="max-w-sm rounded overflow-hidden shadow-lg">
          <!-- <img
            class="w-full"
            src="/img/card-top.jpg"
            alt="Sunset in the mountains"
          /> -->
          <div class="px-6 py-4">
            <div class="font-bold text-xl mb-2">The Coldest Sunset</div>
            <p class="text-gray-700 text-base">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Voluptatibus quia, nulla! Maiores et perferendis eaque,
              exercitationem praesentium nihil.
            </p>
          </div>
        </div>
      </div>
      <div className="col-span-3 col-start-1 row-start-6 bg-white">
        <div class="max-w-sm rounded overflow-hidden shadow-lg">
          <!-- <img
            class="w-full"
            src="/img/card-top.jpg"
            alt="Sunset in the mountains"
          /> -->
          <div class="px-6 py-4">
            <div class="font-bold text-xl mb-2">The Coldest Sunset</div>
            <p class="text-gray-700 text-base">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Voluptatibus quia, nulla! Maiores et perferendis eaque,
              exercitationem praesentium nihil.
            </p>
          </div>
        </div>
      </div>
      <div className="col-span-2 col-start-1 row-start-5 bg-white">
        <div class="max-w-sm rounded overflow-hidden shadow-lg">
          <!-- <img
            class="w-full"
            src="/img/card-top.jpg"
            alt="Sunset in the mountains"
          /> -->
          <div class="px-6 py-4">
            <div class="font-bold text-xl mb-2">The Coldest Sunset</div>
            <p class="text-gray-700 text-base">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Voluptatibus quia, nulla! Maiores et perferendis eaque,
              exercitationem praesentium nihil.
            </p>
          </div>
        </div>
      </div>
      <div className="col-span-2 row-span-2 col-start-4 row-start-5 bg-white">
        <div class="max-w-sm rounded overflow-hidden shadow-lg max-h-20">
          <!-- <img
            class="w-full"
            src="/img/card-top.jpg"
            alt="Sunset in the mountains"
          /> -->
          <div class="px-6 py-4">
            <div class="font-bold text-xl mb-2 text-white">
              The Coldest Sunset
            </div>
            <p class="text-gray-700 text-base">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Voluptatibus quia, nulla! Maiores et perferendis eaque,
              exercitationem praesentium nihil.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="container mx-auto p-8">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <!-- Column 1: Two Cards -->
      <div class="flex flex-col gap-8">
        <!-- Card 1 -->
        <div
          class="bg-gray-600 shadow-lg rounded-lg overflow-hidden flex-1 flex flex-col p-2"
        >
          <div class="p-6 flex-1">
            <h3 class="text-xl font-bold mb-2 text-white">
              Solicita financiamiento bancario
            </h3>
            <p class="text-white">
              Gestiónalo todo en un solo sitio, presenta toda tu documentación
              de manera simple y rápida
            </p>
            <a
              href="#"
              className="hover:underline text-cyan-200 
                   hover:text-cyan-300 
                   visited:text-cyan-500"
            >
              Ver más
            </a>
          </div>
        </div>
        <!-- Card 2 -->
        <div
          class="bg-gray-600 shadow-lg rounded-lg overflow-hidden flex-1 flex flex-col p-2"
        >
          <div class="p-6 flex-1">
            <h3 class="text-xl font-bold mb-2 text-white">
              Compara las propuestas que recibes
            </h3>
            <p class="text-white">
              Obtendrás respuesta a tus solicitudes y podrás comparar
              condiciones para aceptar la propuesta que más se ajuste a tus
              necesidades.
            </p>
            <a
              href="#"
              className="hover:underline text-cyan-200 
                   hover:text-cyan-300  
                   visited:text-cyan-500"
            >
              Ver más
            </a>
          </div>
        </div>
      </div>
      <!-- Column 2: Title and Subtitle -->
      <div class="flex items-center justify-center p-8">
        <div class="text-center">
          <h2 class="text-3xl font-bold mb-2 text-white">
            Escala e invierte en tu negocio
          </h2>
          <p class="text-lg text-white">
            Todas tus operaciones en un solo lugar te permitirán tomar
            decisiones inteligentes para tu negocio.
          </p>
        </div>
      </div>
    </div>
  </section>
  <section class="container mx-auto p-8">
    <div class="flex justify-center items-center mt-10">
      <h2 class="text-2xl font-bold text-teal-400">
        Únete a las 1000+ empresas que ya confían en nosotros para solicitar sus
        préstamos
      </h2>
    </div>
  </section>
  <!-- component -->
  <footer class="bg-blue-100/80 font-sans dark:bg-gray-900">
    <div class="container px-6 py-12 mx-auto">
      <div
        class="grid grid-cols-1 gap-6 sm:grid-cols-2 sm:gap-y-10 lg:grid-cols-4"
      >
        <div class="sm:col-span-2">
          <h1
            class="max-w-lg text-xl font-semibold tracking-tight text-gray-800 xl:text-2xl dark:text-white"
          >
            Subscribe our newsletter to get an update.
          </h1>

          <div
            class="flex flex-col mx-auto mt-6 space-y-3 md:space-y-0 md:flex-row"
          >
            <input
              id="email"
              type="text"
              class="px-4 py-2 text-gray-700 bg-white border rounded-md dark:bg-gray-900 dark:text-gray-300 dark:border-gray-600 focus:border-blue-400 dark:focus:border-blue-300 focus:outline-none focus:ring focus:ring-opacity-40 focus:ring-blue-300"
              placeholder="Email Address"
            />

            <button
              class="w-full px-6 py-2.5 text-sm font-medium tracking-wider text-white transition-colors duration-300 transform md:w-auto md:mx-4 focus:outline-none bg-gray-800 rounded-lg hover:bg-gray-700 focus:ring focus:ring-gray-300 focus:ring-opacity-80"
            >
              Subscribe
            </button>
          </div>
        </div>

        <div>
          <p class="font-semibold text-gray-800 dark:text-white">Quick Link</p>

          <div class="flex flex-col items-start mt-5 space-y-2">
            <p
              class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:cursor-pointer hover:text-blue-500"
            >
              Home
            </p>
            <p
              class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:cursor-pointer hover:text-blue-500"
            >
              Who We Are
            </p>
            <p
              class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:cursor-pointer hover:text-blue-500"
            >
              Our Philosophy
            </p>
          </div>
        </div>

        <div>
          <p class="font-semibold text-gray-800 dark:text-white">Industries</p>

          <div class="flex flex-col items-start mt-5 space-y-2">
            <p
              class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:cursor-pointer hover:text-blue-500"
            >
              Retail & E-Commerce
            </p>
            <p
              class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:cursor-pointer hover:text-blue-500"
            >
              Information Technology
            </p>
            <p
              class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:cursor-pointer hover:text-blue-500"
            >
              Finance & Insurance
            </p>
          </div>
        </div>
      </div>

      <hr class="my-6 border-gray-200 md:my-8 dark:border-gray-700 h-2" />

      <div class="sm:flex sm:items-center sm:justify-between">
        <div class="flex flex-1 gap-4 hover:cursor-pointer">
          <img
            src="https://www.svgrepo.com/show/303139/google-play-badge-logo.svg"
            width="130"
            height="110"
            alt=""
          />
          <img
            src="https://www.svgrepo.com/show/303128/download-on-the-app-store-apple-logo.svg"
            width="130"
            height="110"
            alt=""
          />
        </div>

        <div class="flex gap-4 hover:cursor-pointer">
          <img
            src="https://www.svgrepo.com/show/303114/facebook-3-logo.svg"
            width="30"
            height="30"
            alt="fb"
          />
          <img
            src="https://www.svgrepo.com/show/303115/twitter-3-logo.svg"
            width="30"
            height="30"
            alt="tw"
          />
          <img
            src="https://www.svgrepo.com/show/303145/instagram-2-1-logo.svg"
            width="30"
            height="30"
            alt="inst"
          />
          <img
            src="https://www.svgrepo.com/show/94698/github.svg"
            class=""
            width="30"
            height="30"
            alt="gt"
          />
          <img
            src="https://www.svgrepo.com/show/22037/path.svg"
            width="30"
            height="30"
            alt="pn"
          />
          <img
            src="https://www.svgrepo.com/show/28145/linkedin.svg"
            width="30"
            height="30"
            alt="in"
          />
          <img
            src="https://www.svgrepo.com/show/22048/dribbble.svg"
            class=""
            width="30"
            height="30"
            alt="db"
          />
        </div>
      </div>
      <p class="font-sans p-8 text-start md:text-center md:text-lg md:p-4">
        © 2023 You Company Inc. All rights reserved.
      </p>
    </div>
  </footer>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>

