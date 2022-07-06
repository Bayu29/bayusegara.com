<template>
  <div class="" data-aos="zoom-in" data-aos-anchor-placement="top-bottom">
    <section class="get-in-touch-section">
      <div class="title-get-in-touch text-center">GET IN TOUCH</div>
      <p class="subtitle-get-in-touch">Interested in working together? Feel free to contact me for any project collaboration.</p>
      <div class="row">
        <div class="col-lg-6">
          <img class="get-in-touch-illustration" src="/images/get-in-touch illustration.png">
        </div>
        <div class="col-lg-6">
          <form class="form-mail" autocomplete="off">
            <div class="form-group">
              <div class="row">
                <div class="col-md-6">
                  <div class="form-group">
                    <input class="form-control form-mail-control" name="name" placeholder="Name" autocomplete="off">
                  </div>
                </div>
                <div class="col-md-6">
                  <div class="form-group">
                    <input class="form-control form-mail-control" name="email" placeholder="Email" v-model="from" autocomplete="off">
                  </div>
                </div>
              </div>
            </div>
            <div class="form-group">
              <input type="text" class="form-control form-mail-control" placeholder="Subject" v-model="subject" autocomplete="off">
            </div>
            <div class="form-group">
              <textarea name="message" class="form-control form-mail-control" id="message" cols="30" v-model="message" rows="10" placeholder="Message" autocomplete="off"></textarea>
            </div>
            <div class="form-group">
              <div class="">
                <div class="">
                    <button class="btn btn-orange btn-block" type="button" @click="send">Submit</button>
                </div>
              </div>
            </div>
          </form>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name :'mail',
  data () {
    return {
      email : '',
      message : '',
      from : '',
      subject : '',
    }
  },
  methods:{
    send() {
      this.$mail.send({
        from : this.from,
        subject: this.subject,
        text : this.message
      })
    }
  }
}
</script>
