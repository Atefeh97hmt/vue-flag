
<template>
<header>
    <nav class="flex flex-wrap items-center justify-between w-full py-4 md:py-0 px-4 text-lg text-gray-700 bg-white h-14 bg-gradient-to-r from-violet-100 to-violet-300">
      <div class="hidden w-full md:flex md:items-center md:w-auto" id="menu">
          <ul
            class="
              text-base text-gray-700
              pt-4
              md:flex
              md:justify-between
              md:pt-0">
            <li>
              <RouterLink to="/" class="md:p-4 py-2 block hover:text-purple-400" >Main page</RouterLink>
            </li>
            <li>
              <RouterLink to="about" class="md:p-4 py-2 block hover:text-purple-400" >About</RouterLink>
            </li>
            <li>
              <RouterLink to="./contact" class="md:p-4 py-2 block hover:text-purple-400">Contact</RouterLink>

            </li>
          </ul>
        </div>
    </nav>
  </header>
  </template>