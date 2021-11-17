<template>
  <v-timeline>
    <v-timeline-item right class="text-left">
      <v-list-group :value="true" no-action sub-group>
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title>Manager</v-list-item-title>
          </v-list-item-content>
        </template>

        <v-list-item v-for="([title], i) in manager" :key="i" link>
          <v-list-item-title v-text="title"></v-list-item-title>
        </v-list-item>
      </v-list-group>
    </v-timeline-item>

    <v-timeline-item right class="text-left">
      <v-list-group :value="true" no-action sub-group>
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title>Lead</v-list-item-title>
          </v-list-item-content>
        </template>

        <v-list-item v-for="([title], i) in lead" :key="i" link>
          <v-list-item-title v-text="title"></v-list-item-title>
        </v-list-item>
      </v-list-group>
    </v-timeline-item>

    <v-timeline-item right class="text-left">
      <v-list-group :value="true" no-action sub-group>
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title>Associate</v-list-item-title>
          </v-list-item-content>
        </template>

        <v-list-item v-for="([title], i) in associate" :key="i" link>
          <v-list-item-title v-text="title"></v-list-item-title>
        </v-list-item>
      </v-list-group>
    </v-timeline-item>
  </v-timeline>
</template>

<script>
export default {
  data: () => ({
    manager: [["Name One"], ["Name Two"]],
    lead: [["Name One"], ["Name Two"]],
    associate: [["Name One"], ["Name Two"]],
  }),
};
</script>
