<template>
  <div>
    <p>ホーム画面</p>
    <p><router-link to="sign-in">サインイン</router-link></p>
    <p><button @click="calendar">カレンダー</button></p>
    <p><button @click="profile">プロフィール</button></p>
    <p><button @click="share">共有</button></p>
  </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api';

export default defineComponent({
  setup(prop, context) {
    const calendar = () => {
      context.root.$router.push(
        { name: 'calendar', params: { type: { hoge: 123, fuga: 'xyz' } } },
        () => {},
        () => {},
      );
    };

    const profile = () => {
      context.root.$router.push(
        'profile',
        () => {},
        () => {},
      );
    };

    const share = () => {
      context.root.$router.push(
        'share',
        () => {},
        () => {},
      );
    };
    return {
      calendar,
      profile,
      share,
    };
  },
});
</script>
