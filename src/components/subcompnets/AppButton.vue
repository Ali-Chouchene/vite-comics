<script>
export default {
    name: 'AppButton',
}

</script>

<template>
    <div class="btn">
        <button>
            <h3>LOAD MORE</h3>
        </button>
    </div>

</template>

<style lang="scss" scoped>
.btn {
    text-align: center;
    padding: 2rem 0;

    button {
        color: white;
        background-color: dodgerblue;
        padding: 10px 20px;
        border: 1px solid rgba(22, 22, 219, 0.281);
        cursor: pointer;

        &:hover {
            background-color: rgba(57, 86, 248, 0.781);
        }
    }
}
</style>