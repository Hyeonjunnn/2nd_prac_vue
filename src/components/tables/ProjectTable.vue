<template>
    <table class="table table-striped table-hover text-center">
        <thead>
            <tr>
                <th>학과 번호</th>
                <th>학과 이름</th>
                <th>계열</th>
                <th>개설 여부</th>
                <th>삭제</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="project in projects" :key="project.no">
                <td>{{ project.postNo }}</td>
                <td>{{ project.title }}</td>
                <td>{{ project.userName }}</td>
                <td>{{ new Date(post.createdAt).toLocaleDateString() }}</td>
                <td>
                    <button type="button" class="btn btn-outline-danger">삭제</button>
                </td>
            </tr>
        </tbody>
    </table>
</template>

<script setup>
    const props = defineProps({
        projects: {
            type: Array,
            required: true
        }
    });
</script>