<template>
  <div class="about">
    <Header />
    <div class="container">
      <div class="col">
        <h4>Account</h4>
        <hr />
        <form class="needs-validation" novalidate>
          <div class="row">
            <div class="col">
              <label for="name">Nome</label>
              <input
                type="text"
                class="form-control"
                placeholder="digite aqui"
                value=""
                key="name"
                required
              />
              <div class="invalid-feedback">Por favor preencha o nome</div>
            </div>
            <div class="col">
              <label for="user-name">User Name</label>
              <input
                type="text"
                class="form-control"
                placeholder="digite aqui"
                value=""
                key="username"
                required
              />
              <div class="invalid-feedback">Por favor preencha o username.</div>
            </div>
            <div class="col">
              <label for="email">Email</label>
              <input
                type="email"
                class="form-control"
                placeholder="digite aqui"
                value=""
                key="email"
                required
              />
              <div class="invalid-feedback">Por favor preencha o email.</div>
            </div>
          </div> 
          <div class="col mt-5">
            <h4>Address</h4>
            <hr />
          </div>

          <div class="row mt-3">
            <div class="col-4">
              <label for="zipcode">CEP</label>
              <input
                type="number"
                class="form-control"
                placeholder="digite aqui"
              />
            </div>
            <div class="col-4">
              <label for="street">Rua</label>
              <input
                type="text"
                class="form-control"
                placeholder="digite aqui"
              />
            </div>
            <div class="col-1">
              <label for="num">N.</label>
              <input type="number" class="form-control" placeholder="100" />
            </div>
            <div class="col-3">
              <label for="text">Complemento</label>
              <input
                type="text"
                class="form-control"
                placeholder="digite aqui"
              />
            </div>
          </div>
          <div class="row mt-3">
            <div class="col">
              <label for="">Bairro</label>
              <input
                type="text"
                class="form-control"
                placeholder="digite aqui"
              />
            </div>
            <div class="col">
              <label for="city">Cidade</label>
              <input
                type="text"
                class="form-control"
                placeholder="digite aqui"
              />
            </div>
            <div class="col">
              <label for="state">Estado</label>
              <input
                type="text"
                class="form-control"
                placeholder="digite aqui"
              />
            </div>
          </div>
          <div class="d-flex justify-content-between">
            <a href="/" class="btn btn-secondary mt-3"> Cancelar </a>
            <button class="btn btn-success mt-3"  :disabled="true"  type="submit">Salvar</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";

export default {
  name: "home-page",
  components: {
    Header,
  },
};

(function () {
  "use strict";
  window.addEventListener(
    "load",
    function () {
      // Fetch all the forms we want to apply custom Bootstrap validation styles to
      var forms = document.getElementsByClassName("needs-validation");
      // Loop over them and prevent submission
      var validation = Array.prototype.filter.call(forms, function (form) {
        form.addEventListener(
          "submit",
          function (event) {
            if (form.checkValidity() === false) {
              event.preventDefault();
              event.stopPropagation();
            }
            form.classList.add("was-validated");
            props.disabled= false
          },
          false
        );
      });
    },
    false
  );
})();
</script>
