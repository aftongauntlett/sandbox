<template>
  <v-row>
    <v-col></v-col>
    <v-col>
      <v-timeline>
        <v-timeline-item
          right
          small
          class="text-left"
          v-for="(employees, job) in people"
          :key="job"
        >
          <employees-group :job="job" :employees="employees" />
        </v-timeline-item>
      </v-timeline>
    </v-col>
    <v-col></v-col>
  </v-row>
</template>

<script>
import EmployeesGroup from "./employeesGroup.vue";
import profile from "./profile.vue";

export default {
  components: { profile, EmployeesGroup },
  data: () => ({
    people: {
      manager: [
        {
          name: "bob",
          bio: "bio info",
        },
      ],
      lead: [
        {
          name: "sue",
          bio: "info here",
        },
        {
          name: "dave",
          bio: "more info",
        },
      ],
      associate: [
        {
          name: "rando",
          bio: "info here",
        },
        {
          name: "clear",
          bio: "more info",
        },
      ],
    },
  }),
};
</script>

<style></style>
