<template>
  <div class="about">
        <Header />
    <div class="container">
      <div class="col">
          <h4>Account</h4>
        <hr>
      <form>
        <div class="row">
          <div class="col">
            <label for="name">Nome</label>
            <input type="text" class="form-control" placeholder="Nome Completo da Silva">
          </div>
          <div class="col">
            <label for="user-name">User Name</label>
            <input type="text" class="form-control" placeholder="nickmeu">
          </div>
          <div class="col">
            <label for="email">Email</label>
            <input type="email" class="form-control" placeholder="eu@mail.com">
          </div>
        </div>
      </form>
            <div class="col mt-5">
          <h4>Address</h4>
        <hr>
            </div>
            <form>
        <div class="row mt-3">
          <div class="col-4">
            <label for="zipcode">CEP</label>
            <input type="number" class="form-control" placeholder="digite aqui">
          </div>
          <div class="col-4">
            <label for="street">Rua</label>
            <input type="text" class="form-control" placeholder="digite aqui">
          </div>
          <div class="col-1">
            <label for="num">N.</label>
            <input type="number" class="form-control" placeholder="100">
          </div>
          <div class="col-3">
            <label for="text">Complemento</label>
            <input type="text" class="form-control" placeholder="digite aqui">
          </div>
        </div>
        <div class="row mt-3">
          <div class="col">
            <label for="">Bairro</label>
            <input type="text" class="form-control" placeholder="digite aqui">
          </div>
          <div class="col">
            <label for="city">Cidade</label>
            <input type="text" class="form-control" placeholder="digite aqui">
          </div>
          <div class="col">
            <label for="state">Estado</label>
            <input type="text" class="form-control" placeholder="digite aqui">
          </div>
        </div>
      </form>
      </div>
    <div class="d-flex justify-content-between">
        <button class="btn btn-secondary mt-3"> Cancelar </button>
        <button class="btn btn-success mt-3"> Salvar </button>
    </div>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header.vue';

export default {
  name: 'home-page',
  components: {
    Header,
  },
};
</script>
