<template>
  <q-page>
    <div class="q-py-lg q-px-md">
      <q-input
        bottom-slots
        v-model="newQweetContent"
        class="new-qweet"
        placeholder="What's happening"
        counter
        maxlength="280"
        autogrow
      >
        <template v-slot:before>
          <q-avatar size="xl">
            <img src="https://bit.ly/3EBR5Qp" />
          </q-avatar>
        </template>

        <template v-slot:after>
          <q-btn
            :disable="!newQweetContent"
            unelevated
            rounded
            color="primary"
            label="Qweet"
            no-caps
          />
        </template>
      </q-input>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageHome",
  data() {
    return {
      newQweetContent: "",
    };
  },
});
</script>

<style lang="sass">
.new-qweet
  textarea
    font-size: 19px
    line-height: 1.4 !important
</style>
