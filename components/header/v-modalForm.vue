<template>
<div class="v-modalForm">
    <template>
  <v-row justify="center">
    <v-dialog
      v-model="dialog"
      scrollable
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Оставить заявку
        </v-btn>
      </template>
      <v-card>
        <v-card-title>Форма заявки</v-card-title>
        <v-divider></v-divider>
        <v-card-text>

            <vFormItem />

        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn
            color="blue darken-1"
            text
            @click="dialog = false && logout"
          >
            Выйти
          </v-btn>
          <v-btn
            color="blue darken-1"
            text
            @click="dialog = false"
          >
            Сохранить
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row> 
  </template>
  </div>
</template>

<script>
import vFormItem from "./v-form-item"

export default {
    name: "v-modalForm",
    data () {
        return {
            dialog: false,
        }
    },
    components: {
        vFormItem
    },
    methods: {
      async logout() {
        await this.$store.dispatch("logout")
      }
    },
}
</script>

<style lang="scss">
.v-modalForm{
z-index: 5;
position: absolute;
}
.v-dialog.v-dialog--active.v-dialog--scrollable{
    width:500px;
}
.v-application--wrap{
    min-height: 1px;
}
.theme--dark.v-btn.v-btn--has-bg{
    opacity: 90%;
    border-radius: 30px;
    background-color: rgb(170, 170, 170);
}
</style>