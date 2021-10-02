<template>
  <q-page class="bg-grey-5 flex flex-center">
    <TextToSpeech />
  </q-page>
</template>

<script>
import TextToSpeech from "../components/TextToSpeech";

export default {
  name: "PageIndex",
  components: {
    TextToSpeech
  },
  created() {
    console.log("PATH_TESTE", process.env.PATH_ROUTE);
    console.log("URL_BASE", process.env.URL_BASE);
  }
};
</script>
