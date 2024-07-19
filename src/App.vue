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
    <div
      class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4"
    >
      <!-- Image 1 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/400x300"
          alt="Image 1"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 2 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/500x400"
          alt="Image 2"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 3 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/600x400"
          alt="Image 3"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 4 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/300x300"
          alt="Image 4"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 5 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/400x500"
          alt="Image 5"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 6 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/450x350"
          alt="Image 6"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 7 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/500x500"
          alt="Image 7"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 8 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/350x450"
          alt="Image 8"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 9 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/400x400"
          alt="Image 9"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 10 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/450x400"
          alt="Image 10"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 11 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/300x450"
          alt="Image 11"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 12 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/350x350"
          alt="Image 12"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 13 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/450x300"
          alt="Image 13"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 14 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/400x300"
          alt="Image 14"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Image 15 -->
      <div class="relative overflow-hidden rounded-lg shadow-lg">
        <img
          src="https://via.placeholder.com/500x350"
          alt="Image 15"
          class="w-full h-full object-cover"
        />
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

