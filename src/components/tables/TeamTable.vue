<template>
    <table class="table table-striped table-hover text-center">
        <thead>
            <tr>
                <th>팀 번호</th>
                <th>제목</th>
                <th>설명</th>
                <th>상태</th>
                <th>삭제</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="team in teams" :key="team.no">
                <td>{{ team.no }}</td>
                <td>{{ team.teamNam }}</td>
                <td>{{ team.teamIntroduce }}</td>
                <td>{{ team.projectStatus }}</td>
                <td>
                    <button type="button" class="btn btn-outline-danger">삭제</button>
                </td>
            </tr>
        </tbody>
    </table>
</template>

<script setup>
    const props = defineProps({
        teams: {
            type: Array,
            required: true
        }
    });
</script>