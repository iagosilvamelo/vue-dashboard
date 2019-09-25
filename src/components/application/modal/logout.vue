<template>
  <transition mode="out-in" name="modal">
    <div class="modal fade" id="logoutModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hiden="true">
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="exampleModalLabel">Deseja realmente sair?</h5>
            <button class="close" type="button" aria-label="Close" @click="hide">
              <span>×</span>
            </button>
          </div>
          <div class="modal-body">Selecione sim para sair ou cancelar para voltar ao sistema.</div>
          <div class="modal-footer">
            <button class="btn btn-secondary" type="button" @click="hide">Cancelar</button>
            <a class="btn btn-primary" @click.self.prevent="logof">Sair</a>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: 'LogofModal',

  methods: {
    hide() {
      const modal = document.getElementById('logoutModal');

      modal.classList.remove('show');

      modal.setAttribute("style", "display: none");
      modal.setAttribute("ria-hidden", "true");
      modal.setAttribute("ria-modal", "false");
    },

    logof() { this.$store.dispatch("logof", true) }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
