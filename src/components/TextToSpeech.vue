<template>
  <q-card class=" bordered q-pa-md bg-grey-3 text-white">
    <q-input class="q-pa-md" outlined v-model="textInput" label="Digite aqui" />
    <div class=" q-pa-md">
      <q-btn
        class="q-px-md"
        dense
        no-caps
        color="indigo"
        id="play"
        @click="speak()"
      >
        Falar
      </q-btn>
    </div>
  </q-card>
</template>

<script>
export default {
  name: "TextToSpeech",
  data() {
    return {
      textInput: ""
    };
  },
  methods: {
    speak() {
      let fala = new SpeechSynthesisUtterance(this.textInput);
      window.speechSynthesis.speak(fala);
    }
  }
};
</script>

<style scoped></style>
