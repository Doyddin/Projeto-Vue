<script setup>
import { onMounted, reactive, ref } from "vue";
import ListPokemons from '../components/ListPokemons.vue'

let pokemons = reactive(ref());

onMounted(() => {
  fetch("https://pokeapi.co/api/v2/pokemon?limit=20&offset=0")
    .then((response) => response.json())
    .then((response) => {
      pokemons.value = response.results;
      console.log(pokemons);
    });
});
</script>

<template>
  <main>
    <div class="container">
      <div class="row mt-4">
        <div class="info">
          <div class="navbar col-2">
            <a class="icones novo-usuario col-6" href="">
              <h2><i class="bi bi-person-fill-add"></i></h2>
              <strong>Novo Usuário</strong>
            </a>
            <a class="icones tabela ativo col-6">
              <h2><i class="bi bi-grid-3x2"></i></h2>
              <strong>Tabela</strong>
            </a>
            <a class="icones ajudar col-6" href="">
              <h2><i class="bi bi-question-circle"></i></h2>
              <strong>Ajuda</strong>
            </a>
          </div>
          <div class="fundo-canhoto col-10">
            <div class="col-12">
              <h4>Gestão de Canhotos</h4>
              <label>1.300 <b>Canhotos Encontrados:</b></label>

            </div>
            <div class="row canhoto">
              <div class="test col-3">
                <select class="form-select" aria-label="Default select example">
                  <option selected disabled>Categoria</option>
                  <option value="1">Alimentação</option>
                  <option value="2">Combustível</option>
                  <option value="3">Estadia</option>
                </select>
              </div>
              <div class="col-3">
                <select class="form-select" aria-label="Default select example">
                  <option selected disabled>Valor</option>
                  <option value="1">100 até 2 mil</option>
                  <option value="2">2 mil até 5 mil</option>
                  <option value="3">5 mil até 7 mil</option>
                  <option value="4">7 mil até 10 mil</option>
                </select>
              </div>
              <div class="col-3">
                <select class="form-select" aria-label="Default select example">
                  <option selected disabled>Transportadora</option>
                  <option value="1">Alfa Transportes</option>
                  <option value="2">Braspress</option>
                  <option value="3">Patrus</option>
                  <option value="4">Rodonaves</option>
                  <option value="5">TNT Mercúrio</option>
                </select>
              </div>
              <form class="d-flex col-3" role="search">
                <input class="form-control me-2" type="search" placeholder="Procurar" aria-label="Search">
                <button class="btn btn-outline-success" type="submit"><i class="bi bi-search"></i></button>
              </form>
              <p id="addCanhoto"><a href="cadastroCanhoto.html">Adicionar Canhotos</a></p>
              <table class="table">
                <thead>
                  <tr>
                    <th scope="col">ID</th>
                    <th scope="col">Número NF</th>
                    <th scope="col">Entregador</th>
                    <th scope="col">Preço</th>
                    <th scope="col">Categorias</th>
                    <th scope="col">Data</th>
                    <th scope="col">Ação</th>
                  </tr>
                </thead>
                <tbody class="table-group-divider">
                  <tr>
                    <th scope="row">1</th>
                    <td>0000000000</td>
                    <td>Test</td>
                    <td>9.999,00</td>
                    <td>Test</td>
                    <td>01/01/0001</td>
                    <td>
                      <a href="detalhesCanhoto.html"><i class="bi bi-eye"></i></a>
                      <a href="#"><i class="bi bi-pencil"></i></a>
                    </td>
                  </tr>
                  <tr>
                    <th scope="row">2</th>
                    <td>0000000000</td>
                    <td>Test</td>
                    <td>9.999,00</td>
                    <td>Test</td>
                    <td>01/01/0001</td>
                    <td>
                      <a href="detalhesCanhoto.html"><i class="bi bi-eye"></i></a>
                      <a href="#"><i class="bi bi-pencil"></i></a>
                    </td>
                  </tr>
                  <tr>
                    <th scope="row">3</th>
                    <td>0000000000</td>
                    <td>Test</td>
                    <td>9.999,00</td>
                    <td>Test</td>
                    <td>01/01/0001</td>
                    <td>
                      <a href="detalhesCanhoto.html"><i class="bi bi-eye"></i></a>
                      <a href="#"><i class="bi bi-pencil"></i></a>
                    </td>
                  </tr>
                  <tr>
                    <th scope="row">4</th>
                    <td>0000000000</td>
                    <td>Test</td>
                    <td>9.999,00</td>
                    <td>Test</td>
                    <td>01/01/0001</td>
                    <td>
                      <a href="detalhesCanhoto.html"><i class="bi bi-eye"></i></a>
                      <a href="#"><i class="bi bi-pencil"></i></a>
                    </td>
                  </tr>
                  <tr>
                    <th scope="row">5</th>
                    <td>0000000000</td>
                    <td>Test</td>
                    <td>9.999,00</td>
                    <td>Test</td>
                    <td>01/01/0001</td>
                    <td>
                      <a href="detalhesCanhoto.html" class="icon-eye"><i class="bi bi-eye"></i></a>
                      <a href="#"><i class="bi bi-pencil"></i></a>
                    </td>
                  </tr>
                </tbody>
              </table>
              <div class="clearfix">
                <div class="hint-text">5 Itens Por Página</div>
                <ul class="pagination">
                  <li class="page-item disabled"><a href="" class="page-link">Anterior</a></li>
                  <li class="page-item active"><a href="" class="page-link">1</a></li>
                  <li class="page-item"><a href="" class="page-link">2</a></li>
                  <li class="page-item"><a href="" class="page-link">3</a></li>
                  <li class="page-item"><a href="" class="page-link">4</a></li>
                  <li class="page-item"><a href="" class="page-link">5</a></li>
                  <li class="page-item"><a href="" class="page-link">Próximo</a></li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
