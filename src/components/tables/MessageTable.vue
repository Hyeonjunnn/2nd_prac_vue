<template>
    <table class="table table-striped table-hover text-center">
        <thead>
            <tr>
                <th>쪽지 번호</th>
                <th>보낸 사람</th>
                <th>받는 사람</th>
                <th>보낸 날짜</th>
                <th>내용</th>
                <th>삭제</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="message in messages" :key="message.no">
                <td>{{ message.no }}</td>
                <td>{{ message.senderId }}</td>
                <td>{{ message.reveiverId }}</td>
                <td>{{ message.sentAt }}</td>
                <td>{{ message.content }}</td>
                <td>
                    <button type="button" class="btn btn-outline-danger">삭제</button>
                </td>
            </tr>
        </tbody>
    </table>
</template>

<script setup>
    const props = defineProps({
        messages: {
            type: Array,
            required: true
        }
    });
</script>