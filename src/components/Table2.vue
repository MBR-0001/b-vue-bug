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
          key: "SteamID",
          label: "Steam ID",
        },
        {
          key: "DisplayName",
          label: "Name",
        },
        {
          key: "Ping",
          sortable: true,
        },
        {
          key: "ConnectedSeconds",
          label: "Connected",
          sortable: true,
        },
        {
          key: "Health",
          sortable: true,
        }
      ]
    }
  },
  mounted() {
    for (let i = 0; i < 10; i++) {
      this.tickets.push({
        SteamID: "7656112052525252",
        DisplayName: "name",
        Ping: 52,
        ConnectedSeconds: 12525,
        Health: 99
      });
    }
  }
}
</script>