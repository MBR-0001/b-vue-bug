<template>
  <b-table responsive hover striped :items="tickets" :fields="fields">
  </b-table>
</template>

<script>
export default {
  data: () => {
    return {
      tickets: [],
      fields: [
        {
          key: "id",
          label: "#",
          sortable: true
        },
        {
          key: "creator",
          label: "Creator"
        },
        {
          key: "created_at",
          label: "Created",
          sortable: true
        },
        {
          key: "reported",
          label: "Reported",
        }
      ]
    }
  },
  mounted() {
    for (let i = 0; i < 10; i++) {
      this.tickets.push({
        id: 5,
        creator: "test",
        created_at: "saturday",
        reported: "someone"
      });
    }
  }
}
</script>