<script lang="ts" setup></script>

<template>
  <div>
    Page: index
    <p>explain how it works, show your user stats for your visit</p>
    <p>This is a family friendly trivia game for you to play as you explore the visitor center.</p>
    <p>You'll need to read closely and explore all sections of the center to complete your exploration passport.</p>
    <p>We use session storage to keep track of your progress for this game. That means none of your information is saved on our servers and we won't know who you are. That also means if you close this webpage your progress will be lost! When you click the button below to Begin, you'll have an option on the next page to save your progress to the local storage on your phone. We still won't have access to it, but it will survive a refresh or if you decide to leave a come back later.</p>
    <NuxtLink to="/trivia/passport">Begin</NuxtLink>
  </div>
</template>
