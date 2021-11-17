<template>
  <v-row>
    <v-col>
        {{ imageURL }}
    </v-col>
    <v-col>
      <v-timeline>
        <v-timeline-item
          right
          small
          class="text-left"
          v-for="(employees, job) in people"
          :key="job"
        >
          <employees-group :job="job" :employees="employees" @clicked="bio=$event.bio; imageURL=$event.imageURL" />
        </v-timeline-item>
      </v-timeline>
    </v-col>
    <v-col>
        <div>
            {{ bio }}
        </div>
    </v-col>
  </v-row>
</template>

<script>
import EmployeesGroup from "./employeesGroup.vue";

export default {
  components: { EmployeesGroup },
  data: () => ({
    bio: "",
    imageURL: "",
    people: {
      manager: [
        {
          name: "bob",
          bio: "bio info",
          img: "randjomhge"
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
