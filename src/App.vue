<script setup>
import { ref } from 'vue';

const list = ref([]);

fetch('/list.json')
  .then(d => d.json())
  .then(res => {
    list.value = res;
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
                <a class="p-4 no-underline inline-block nav-link active hover:(bg-gray-300)" aria-current="page" href="#">商品</a>
              </li>
              <li class="nav-item inline">
                <a class="p-4 no-underline inline-block nav-link hover:(bg-gray-300)" href="#">當日特價</a>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </header>

    <section class="container mt-4">
      <div class="row items">
        <div class="col-sm-2">
          <div class="card" data-product-id="624946E">
            <img src="images/cat001.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">老大</h5>
              <p class="price">$20</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="044464F">
            <img src="images/cat002.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">貝貝</h5>
              <p class="price">$15</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="A6245B4">
            <img src="images/cat003.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">老虎</h5>
              <p class="price">$10</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="09DC594">
            <img src="images/cat004.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">胖胖</h5>
              <p class="price">$8.5</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="AAE759E">
            <img src="images/cat005.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">小花</h5>
              <p class="price">$9.99</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="D014739">
            <img src="images/cat006.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">黑臉</h5>
              <p class="price">$12.5</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
      </div>
      <hr>

      <section class="cart">
        <h2>購物車</h2>
        <table class="table cart-item-table">
          <thead>
            <tr>
              <th scope="col">項目</th>
              <th scope="col">數量</th>
              <th scope="col">單價</th>
              <th scope="col">小計</th>
              <th scope="col"></th>
            </tr>
          </thead>
          <tbody>
          </tbody>
          <tfoot>
            <tr>
              <td colspan="2"></td>
              <td>總價</td>
              <td><span class="total-price">$0</span></td>
              <td></td>
            </tr>
          </tfoot>
        </table>
        <button class="btn btn-lg btn-success empty-cart"><i class="fas fa-baby-carriage"></i> 清空購物車</button>
      </section>
    </section>
  </main>
</template>
