<template>
    <div class="thanks-content">
        <div class="thanks-message">
            <p>仮会員登録ありがとうございます</p>
            <div class="sentence">
                <span
                    >ご入力いただいたメールアドレスに、"メールアドレスの確認"メールを送信いたします。</span
                >
                <span
                    >ログイン後、メール本文中の"メールアドレスの確認"のリンクをクリックし、アカウントの本登録を完了してください。</span
                >
            </div>
            <router-link v-bind:to="{ name: 'user-login' }" class="toLogin"
                >ログインする</router-link
            >
        </div>
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
    width: 700px;
    height: 350px;
    display: flex;
    align-items: center;
    flex-flow: column;
    justify-content: center;
    gap: 40px;
    padding: 0 30px;
}
.thanks-message p {
    font-size: 25px;
}
.sentence span {
    display: inline-block;
    line-height: 25px;
}
.toLogin {
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
