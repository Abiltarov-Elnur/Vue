<template>
  <div>
    <Employee
      v-for="user in users"
      :key="user.id"
      :id="user.id"
      :name="user.name"
      :surn="user.surn"
      @change="change"
    />
  </div>
</template>

<script>
import Employee from './Employee.vue';

export default {
  components: { Employee },
  data() {
    return {
      users: [
        { id: 1, name: 'Alice', surn: 'Smith' },
        { id: 2, name: 'Bob', surn: 'Johnson' },
      ],
    };
  },
  methods: {
    change(id, name, surn) {
      this.users = this.users.map(user => {
        if (user.id === id) {
          user.name = name;
          user.surn = surn;
        }
        return user;
      });
    },
  },
};
</script>


