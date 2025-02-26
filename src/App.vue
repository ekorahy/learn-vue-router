<template>
  <header>
    <nav>
      <ul>
        <li>
          <router-link to="/">Home</router-link>
        </li>
        <li>
          <router-link to="/about">About</router-link>
        </li>
        <li>
          <router-link to="/brazil">Brazil</router-link>
        </li>
        <li>
          <router-link to="/hawaii">Hawaii</router-link>
        </li>
        <li>
          <router-link to="/jamaica">Jamaica</router-link>
        </li>
        <li>
          <router-link to="/panama">Panama</router-link>
        </li>
      </ul>
    </nav>
  </header>
  <main><router-view></router-view></main>
</template>
