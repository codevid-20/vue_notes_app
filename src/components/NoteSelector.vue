<template>
  <div class="note-selector" v-bind:class="{active: note.id === selectedNoteId}" v-on:click="changeSelectedNote(note)">
    <p class="note-selector-title">{{note.body}}</p>
    <p class="note-selector-timestamp">{{note.timestamp}}</p>
  </div>
</template>

<script>
export default {
  name: 'note-selector',
  props: ["note", "selectedNoteId"],
  methods: {
    changeSelectedNote: function(note) {      
      this.$emit("changeSelectedNote", note)
    }
  }
}
</script>