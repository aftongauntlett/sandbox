<template>
  <v-list-group :value="true" no-action sub-group>
    <template v-slot:activator>
      <v-list-item-content>
        <v-list-item-title>{{ job }}</v-list-item-title>
      </v-list-item-content>
    </template>

    <v-list-item @click="() => {onClick(employee)}" link v-for="employee in employees" :key="employee.name">
      <v-list-item-title v-text="employee.name"></v-list-item-title>
    </v-list-item>
  </v-list-group>
</template>

<script>
export default {
  props: ["job", "employees"],
  methods: {
      onClick(employee){
          this.$emit(
              "clicked",
              {
                  bio: employee.bio,
                  imageURL: employee.img, 
              }
          )
      }
  }
};
</script>

<style></style>
