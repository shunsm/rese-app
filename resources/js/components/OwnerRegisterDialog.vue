<template>
    <div class="modal" :class="fadeAnimation">
        <div class="modal-content" :class="zoomAnimation">
            <div class="modal-content-inner">
                <p>店舗オーナーを新規登録しました</p>
                <button class="back" @click="leaveWithAnimation">戻る</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data: function () {
        return {
            fadeAnimation: "animate__animated animate__fadeIn",
            zoomAnimation: "animate__animated animate__zoomIn",
        };
    },
    methods: {
        leaveWithAnimation() {
            this.fadeAnimation = "animate__animated animate__fadeOut";
            this.zoomAnimation = "animate__animated animate__zoomOut";
            setTimeout(() => {
                this.$router.push("/rese/admin/owner-list");
            }, 300);
        },
    },
};
</script>

<style scoped>
.modal {
    position: fixed;
    left: 0%;
    top: 0%;
    height: 100vh;
    width: 100vw;
    background-color: rgba(0, 0, 0, 0.3);
    animation-duration: 0.3s;
}
.modal-content {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
    animation-duration: 0.2s;
}
.animate__animated.animate__zoomOut {
    animation-duration: 0.5s;
}
.modal-content-inner {
    border: 5px solid #9a2fff;
    border-radius: 10px;
    overflow: hidden;
    background-color: white;
    width: 600px;
    box-shadow: 2px 2px 10px gray;
    height: 200px;
    display: flex;
    flex-flow: column;
    justify-content: center;
    gap: 30px 0;
}
.modal-content-inner > * {
    margin: 0 auto;
}
.modal-content-inner p {
    font-size: 20px;
    font-weight: bold;
}
.back {
    border: none;
    background-color: #9a2fff;
    color: #ffffff;
    padding: 7px 20px;
    border-radius: 5px;
    cursor: pointer;
}
</style>
