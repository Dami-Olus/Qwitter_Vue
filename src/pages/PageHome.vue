<template>
  <q-page>
    <div class="q-py-lg q-px-md row items-end q-col-gutter-md">
      <div class="col">
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
        </q-input>
      </div>
      <div class="col col-shrink q-mb-lg">
        <q-btn
          :disable="!newQweetContent"
          unelevated
          rounded
          color="primary"
          label="Qweet"
          no-caps
        />
      </div>
    </div>
    <q-separator class="divider" size="10px" color="grey-2" />

    <q-list>
      <q-item class="q-py-md">
        <q-item-section avatar top>
          <q-avatar size="xl">
            <img src="https://bit.ly/3EBR5Qp" />
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-subtitle1">
            <strong>Damola</strong>
            <span class="text-grey-7">@Damioguns</span>
          </q-item-label>
          <q-item-label class="qweet-content text-body1">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incidid unt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation.
            <br /><br />
            Ullamco laboris nisi ut aliquip ex ea comm odo consequat. Duis aute
            irure dolor in reprehenderit in voluptate velit esse cillum dolore
            eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
            proident, sunt in culpa qui officia deserunt mollit anim id est
            laborum.
          </q-item-label>
          <div class="qweet-icons row justify-between q-mt-sm">
            <q-btn
              flat
              round
              color="grey"
              size="sm"
              icon="fa-regular fa-comment"
            />
            <q-btn
              flat
              round
              color="grey"
              size="sm"
              icon="fas fa-retweet"
            />
            <q-btn
              flat
              round
              color="grey"
              size="sm"
              icon="fa-regular fa-heart"
            />
            <q-btn
              flat
              round
              color="grey"
              size="sm"
              icon="fas fa-trash"
            />
          </div>
        </q-item-section>

        <q-item-section side top> 1 min ago </q-item-section>
      </q-item>
    </q-list>
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
.divider
  border-top: 1px solid
  border-bottom: 1px solid
  border-color: $grey-4
.qweet-content
  white-space: pre-line
.qweet-icons
  margin-left: -5px
</style>
