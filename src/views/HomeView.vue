<script setup>
import { supabase } from "../supabase";
import router from "../router/index";

async function signOut() {
  const { error } = await supabase.auth.signOut();
  router.push("/sign-in");
}
</script>

<template>
  <div class="text-center m-20">
    <p class="text-6xl font-bold">Hello Supabase ❤️❤️</p>
    <button
      @click="signOut"
      class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mt-10 rounded focus:outline-none focus:shadow-outline"
      type="submit"
    >
      Logout Here !
    </button>
  </div>
</template>
