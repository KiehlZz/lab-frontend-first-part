<script setup lang="ts">
import type { Event } from '@/types';
import { ref } from 'vue';
const event = ref<Event>({
    id: 0,
    category: '',
    title: '',
    description: '',
    location: '',
    date: '',
    time: '',
    petsAllowed: false,
    organizer: ''
})
</script>

<template>
    <div class="form-container">
        <h1>Create an Event</h1>
        <form class="event-form">
            <div class="form-group">
                <label>Category</label>
                <input v-model="event.category" type="text" placeholder="Category" class="field" />
            </div>

            <h3>Name & Describe Your Event</h3>
            <div class="form-group">
                <label>Title</label>
                <input v-model="event.title" type="text" placeholder="Title" class="field" />
            </div>

            <div class="form-group">
                <label>Description</label>
                <textarea v-model="event.description" placeholder="Description" class="field"></textarea>
            </div>

            <h3>Where is Your Event?</h3>
            <div class="form-group">
                <label>Location</label>
                <input v-model="event.location" type="text" placeholder="Location" class="field" />
            </div>

            <button class="button" type="submit">Submit</button>
        </form>

        <pre>{{ event }}</pre>
    </div>
</template>