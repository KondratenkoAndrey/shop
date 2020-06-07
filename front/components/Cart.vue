<template>
  <v-dialog v-model="cartDialog" persistent max-width="800">
    <template v-slot:activator="{ on }">
      <v-btn
        icon
        v-on="on"
      >
        <v-badge
          color="green"
          overlap
          :content="cartItemsCount"
          :value="cartItemsCount"
        >
          <v-icon>mdi-cart</v-icon>
        </v-badge>
      </v-btn>
    </template>
    <v-stepper v-model="e6" vertical>
      <v-stepper-step :complete="e6 > 1" step="1">
        Проверьте заказ
        <small>
          Убедитесь в правильности Вашего заказа
        </small>
      </v-stepper-step>
      <v-stepper-content step="1">

      <template>
        <v-container fluid>
            <template>
              <v-card>
                <v-card-title
                  class="subheading font-weight-bold"
                >
                  Заказ
                </v-card-title>
                <v-divider></v-divider>
                <v-list dense>
                  <v-list-item
                    v-for="item in items"
                    :key="item.name"
                  >
                    <v-list-item-content>{{ item.name }}</v-list-item-content>
                    <v-list-item-content class="align-end">{{ item.price }}</v-list-item-content>
                  </v-list-item>
                </v-list>
              </v-card>
            </template>
        </v-container>
      </template>

        <v-btn color="primary" @click="e6 = 2">
          Далее
        </v-btn>
        <v-btn text @click="cartDialog = false">
          Отмена
        </v-btn>
      </v-stepper-content>
      <v-stepper-step :complete="e6 > 2" step="2">
        Параметры доставки
      </v-stepper-step>
      <v-stepper-content step="2">
        <v-card color="grey lighten-1" class="mb-12" height="200px">
          Шаг 2
        </v-card>
        <v-btn color="primary" @click="e6 = 3">
          Далее
        </v-btn>
        <v-btn text @click="cartDialog = false">
          Отмена
        </v-btn>
      </v-stepper-content>
      <v-stepper-step step="3">
        Оплата заказа
      </v-stepper-step>
      <v-stepper-content step="3">
        <v-card color="grey lighten-1" class="mb-12" height="200px">
          Шаг 3
        </v-card>
        <v-btn color="primary" @click="paySucces()">
          Оплатить
        </v-btn>
        <v-btn text @click="cartDialog = false">
          Отмена
        </v-btn>
      </v-stepper-content>
    </v-stepper>
  </v-dialog>
</template>

<script>
export default {
  data () {
    return {
      cartDialog: false,
      cartItemsCount: 4,
      e6: 1,
      itemsPerPage: 4,
      items: [
        {
          name: 'Котята',
          price: 1200
        },
        {
          name: 'Щенята',
          price: 2600
        },
        {
          name: 'Гусята',
          price: 800
        },
        {
          name: 'Лягушата',
          price: 250
        }
      ]
    }
  },
  methods: {
    paySucces () {
      this.cartItemsCount = 0
      this.cartDialog = false
      this.e6 = 1
    }
  }
}
</script>
