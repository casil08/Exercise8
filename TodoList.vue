 <template>
    <div>
     <h2>To-Do List</h2>
     <input v-model="newItem" @keyup.enter="addItem" placeholder="Add a
new item" />
      <ul>
        <li v-for="(item, index) in items" :key="index">
          {{ item }} <button @click="removeItem(index)">Remove</button>
        </li>
      </ul>
    </div>
</template>
</script>
    export default {
        data() {
            return {
                newItem: '',
                items: []
            };
        },
        methods: {
            addItem() {
                if (this.newItem !== '') {
                    this.items.push(this.newItem);
                    this.newItem = '';
                }
            },
            removeItem(index) {
                this.items.splice(index, 1);
            }
        }
    };