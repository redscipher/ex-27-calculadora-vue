<script setup lang="ts">
// variaveis
let flgNumerico = true;

//constantees
const numerosCalculadora: string[] = ['1', '2', '3', '4', '5', '6', '7', '8', '9', 'C', '0', 'E'];
const operacoes: string[] = ['+', '-', '*', '/'];

// funcoes
function validaNumerico(num: string): boolean{
    // var retorno
    let controle: boolean = false;
    try {
        // valida se eh um numero
        if (parseInt(num) >= 0) controle= true;
    } catch (error) {
        console.log(error);
    } finally {
        return controle;
    }
}
// 
</script>

<template>
    <!--  -->
    <div class="container pt-5 text-center text-white">
        <div class="row">
            <div class="col-12">
                <form action="" class="ps-4 py-5 d-flex">
                    <div class="w-75 d-flex">
                        <input class="form-control mb-3 me-3" type="number" placeholder="Digite um número">
                        <select name="" id="" class="form-select mb-3 me-3 w-25 rounded-3">
                            <option value="1" selected>+</option>
                            <option value="2">-</option>
                            <option value="3">*</option>
                            <option value="4">/</option>
                        </select>
                        <input class="form-control mb-3" type="number" placeholder="Digite um número">
                    </div>
                    <label id="id-resultado" for="" class="form-label w-25 ms-3 mb-3 text-center">Resultado</label>
                </form>
            </div>
        </div>
        <div class="row">
            <div class="col-10">
                <ul class="row">
                    <li class="col-4 py-3" v-for="num in numerosCalculadora">
                        <button v-if="validaNumerico(num)" type="button" class="btn btn-secondary w-100">{{ num }}</button>
                        <button v-else type="button" class="btn btn-warning w-100">{{ num }}</button>
                    </li>
                </ul>
            </div>
            <div class="col-2">
                <ul class="row">
                    <li class="col-12 py-3" v-for="op in operacoes">
                        <button type="button" class="btn btn-light  w-100">{{ op }}</button>
                    </li>
                </ul>
            </div>
        </div>
    </div>
    <!--  -->
</template>

<style scoped lang="scss">
    // importacoes
    @use '../sass/variaveis';

    // elementos
    ul {
        list-style: none;
    }

    // ids
    #id-resultado{
        border: 2px dotted #ccc;
        border-radius: 10px;
        background-color: lighten(variaveis.$corFundo, 30%);
    }

    // 
</style>