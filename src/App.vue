<script setup>
import { ref } from 'vue';
const catList = ref([]);

// 取得商品列表
fetch('/list.json')
  .then(res => res.json())
  .then(data => {
    catList.value = data;
  });

</script>

<template>
  <main>
    <header>
      <nav class="bg-light navbar navbar-expand-lg navbar-light">
        <div class="container-fluid">
          <a class="navbar-brand" href="/"><i class="fas fa-gem"></i> 賺很大商店</a>
          <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="m-0 navbar-nav">
              <li class="nav-item inline">
                <a class="p-4 no-underline inline-block nav-link active hover:(bg-gray-300)" aria-current="page"
                  href="#">商品</a>
              </li>
              <li class="nav-item inline">
                <a class="p-4 no-underline inline-block nav-link hover:(bg-gray-300)" href="#">當日特價</a>
              </li>
            </ul>
          </div>
        </div>

        <!-- 搜尋 -->
        <div class="mr-10">
          <label class="block relative">
            <i class="top-3 left-3 absolute fa-solid fa-magnifying-glass"></i>
            <input type="text" class="border text-xl py-1 pl-9">
          </label>
        </div>
      </nav>
    </header>

    <section class="container mt-4">
      <div class="row items">
        <div class="col-sm-2">
          <div class="card" data-product-id="624946E">
            <img src="/images/cat001.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">老大</h5>
              <p>$20 / 庫存: 7</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="044464F">
            <img src="/images/cat002.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">貝貝</h5>
              <p>$15 / 庫存: 3</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="A6245B4">
            <img src="/images/cat003.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">老虎</h5>
              <p>$10 / 庫存: 9</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="09DC594">
            <img src="/images/cat004.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">胖胖</h5>
              <p>$12 / 庫存: 5</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="AAE759E">
            <img src="/images/cat005.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">小花</h5>
              <p>$9 / 庫存: 12</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="D014739">
            <img src="/images/cat006.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">黑臉</h5>
              <p>$22 / 庫存: 8</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
      </div>

      <hr class="my-12">

      <section class="cart">
        <h2>購物車</h2>
        <table class="table cart-item-table">
          <thead>
            <tr>
              <th scope="col" class="w-1/5">項目</th>
              <th scope="col" class="w-1/5">數量</th>
              <th scope="col" class="w-1/5">單價</th>
              <th scope="col" class="w-1/5">小計</th>
              <th scope="col" class="w-1/5"></th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>商品1</td>
              <td>3</td>
              <td>$10</td>
              <td>$30</td>
              <td>
                <button class="mr-4 btn btn-sm btn-warning"><i class="fas fa-plus"></i></button>
                <button class="mr-4 btn btn-sm btn-warning"><i class="fas fa-minus"></i></button>
                <button class="btn btn-sm btn-danger"><i class="fas fa-trash"></i></button>
              </td>
            </tr>
            <tr>
              <td>商品2</td>
              <td>2</td>
              <td>$15</td>
              <td>$30</td>
              <td>
                <button class="mr-4 btn btn-sm btn-warning"><i class="fas fa-plus"></i></button>
                <button class="mr-4 btn btn-sm btn-warning"><i class="fas fa-minus"></i></button>
                <button class="btn btn-sm btn-danger"><i class="fas fa-trash"></i></button>
              </td>
            </tr>
            <tr>
              <td>商品3</td>
              <td>1</td>
              <td>$20</td>
              <td>$20</td>
              <td>
                <button class="mr-4 btn btn-sm btn-warning"><i class="fas fa-plus"></i></button>
                <button class="mr-4 btn btn-sm btn-warning"><i class="fas fa-minus"></i></button>
                <button class="btn btn-sm btn-danger"><i class="fas fa-trash"></i></button>
              </td>
            </tr>
          </tbody>
          <tfoot>
            <tr>
              <td colspan="3"></td>
              <td colspan="2">總價: <span class="ml-8">$ 99,999</span></td>
            </tr>
          </tfoot>
        </table>
        <button class="btn btn-lg btn-success empty-cart"><i class="fas fa-baby-carriage"></i> 清空購物車</button>
      </section>
    </section>
  </main>
</template>
