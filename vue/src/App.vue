<template>
  <div class="container">
    <!-- Меню заметок -->
    <div class="sidebar">
      <button
        v-for="(note, index) in notes"
        :key="index"
        @click="selectNote(index)"
        :class="{ active: index === selectedNoteIndex }"
      >
        Note {{ index + 1 }}
      </button>
      <button @click="addNote">+ Add Note</button>
    </div>

    <!-- Редактор -->
    <div class="editor" v-if="selectedNoteIndex !== null">
      <textarea v-model="notes[selectedNoteIndex]" />
    </div>

    <div class="editor" v-else>
      <p>Select a note to edit</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      notes: ['First note', 'Second note'],
      selectedNoteIndex: null,
    };
  },
  methods: {
    selectNote(index) {
      this.selectedNoteIndex = index;
    },
    addNote() {
      this.notes.push('New note');
      this.selectedNoteIndex = this.notes.length - 1;
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
  max-width: 800px;
  margin: 2rem auto;
  border: 1px solid #ccc;
  border-radius: 8px;
  overflow: hidden;
}

.sidebar {
  width: 200px;
  background: #f4f4f4;
  padding: 1rem;
  border-right: 1px solid #ccc;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.sidebar button {
  padding: 0.5rem;
  text-align: left;
  border: none;
  background: #fff;
  cursor: pointer;
  border-radius: 4px;
  transition: 0.2s;
}

.sidebar button.active,
.sidebar button:hover {
  background: #dceeff;
}

.editor {
  flex: 1;
  padding: 1rem;
}

textarea {
  width: 100%;
  height: 300px;
  font-size: 1rem;
  padding: 0.5rem;
  resize: none;
}
</style>
