<template>
  <div class="tarefa">
    <Header />
    <div class="container">
      <div class="col">
        <h4>Tasks</h4>
        <hr />
        <form action="">
          <div class="row">
            <div class="col-6 mt-3">
              <label for="title">Title</label>
              <input
                type="text"
                class="form-control"
                placeholder="digite aqui"
                v-model="inputTitle"
              />
            </div>
            <div class="col-6 mt-3">
              <label for="status">Status</label>
              <select
                class="form-control custom-select"
                v-model="inputStatus"
                id="status"
              >
                <option>ToDo</option>
                <option>WiP</option>
                <option>Done</option>
              </select>
            </div>
          </div>
          <div class="col-12 mt-3">
            <label for="text_area">Description</label>
            <textarea
              class="form-control"
              id="text_area"
              rows="3"
              placeholder="digite aqui"
              v-model="inputDescription"
            ></textarea>
            <div class="d-flex justify-content-between">
              <a href="" class="btn btn-light mt-3"> Cancelar </a>
              <a
                href=""
                @click.stop.prevent="salvarInfo()"
                id="salvarTask"
                class="btn btn-success mt-3"
              >
                Salvar
              </a>
            </div>
          </div>
        </form>
        <div class="container mt-5">
          <table class="table">
            <thead>
              <tr>
                <th scope="col">ID</th>
                <th scope="col">Title</th>
                <th scope="col">Description</th>
                <th scope="col">Status</th>
                <th scope="col"> Action</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <th scope="row">{{id}}</th>
                <td>{{title}}</td>
                <td>{{description}}</td>
                <td>{{status}}</td>
                <td><font-awesome-icon icon="fa-solid fa-trash-can" /></td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";

export default {
  name: "Tarefas",
  components: {
    Header,
  },
  methods: {
    salvarInfo() {
      const title = this.inputTitle;
      this.title = title;
      const status = this.inputStatus;
      this.status = status;
      const description = this.inputDescription;
      this.description = description;
    },
  },
  data() {
    return {
      title: "",
      status: "",
      description: "",
      inputTitle: "",
      inputStatus: "",
      inputDescription: "",
    };
  },
};
</script>
