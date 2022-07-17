<template>
<h1>{{ msg }}</h1>
  <form ref="form" @submit.prevent="sendEmail">
    <label>Name</label>
    <input type="text" name="user_name">
    <label>Email</label>
    <input type="email" name="user_email">
    <label>Message</label>
    <textarea name="message"></textarea>
    <input type="submit" value="Send">
  </form>
</template>

<script>
import emailjs from '@emailjs/browser';

export default {
  methods: {
    sendEmail() {
        let data = new FormData();
        data.append('user_name','Eric')
        data.append('user_email','eands9@yahoo.com')
        data.append('message','This is a Test')
        emailjs.sendForm('service_g3yknwq', 'template_zah7m3u', this.$refs.form, 'Pp57yBinHJjAjXu1n')
        // emailjs.sendForm('service_g3yknwq', 'template_zah7m3u', this.data, 'Pp57yBinHJjAjXu1n')
            .then((result) => {
                console.log('SUCCESS!', result.text);
            }, (error) => {
                console.log('FAILED...', error.text);
            });
    }
  },
  props: {
    msg: String
  }
}
</script>
