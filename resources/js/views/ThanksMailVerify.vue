<template>
    <div class="thanks-content">
        <form class="thanks-message">
            <p>メール認証が成功しました</p>
            <p>本会員登録ありがとうございます</p>
            <router-link v-bind:to="{ name: 'home' }" class="to-home"
                >HOMEへ戻る</router-link
            >
        </form>
    </div>
</template>

<style scoped>
.thanks-content {
    height: 80vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
.thanks-message {
    background-color: #ffffff;
    box-shadow: 2px 2px 4px gray;
    border-radius: 5px;
    width: 500px;
    height: 350px;
    display: flex;
    align-items: center;
    flex-flow: column;
    justify-content: center;
    gap: 50px;
}
.thanks-message p {
    font-size: 25px;
}
.to-home {
    text-decoration: none;
    background-color: #2f60ff;
    color: #ffffff;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
}
/* ------ スマートフォンデザイン ------ */
@media screen and (max-width: 480px) {
    .thanks-message {
        padding: 0 10px;
    }
}
</style>
