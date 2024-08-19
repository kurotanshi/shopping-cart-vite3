<script setup>
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
              <p class="price">$20</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="044464F">
            <img src="/images/cat002.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">貝貝</h5>
              <p class="price">$15</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="A6245B4">
            <img src="/images/cat003.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">老虎</h5>
              <p class="price">$10</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="09DC594">
            <img src="/images/cat004.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">胖胖</h5>
              <p class="price">$8.5</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="AAE759E">
            <img src="/images/cat005.jpg" class="card-img-top" alt="">
            <div class="card-body">
              <h5 class="card-title fw-light fs-6">小花</h5>
              <p class="price">$9.99</p>
              <button class="btn btn-sm btn-warning fw-light"><i class="fas fa-cat"></i></button>
            </div>
          </div>
        </div>
        <div class="col-sm-2">
          <div class="card" data-product-id="D014739">
            <img src="/images/cat006.jpg" class="card-img-top" alt="">
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
            <tr>
              <td>商品1</td>
              <td>3</td>
              <td>$10</td>
              <td>$30</td>
              <td><button class="btn btn-sm btn-danger"><i class="fas fa-trash"></i></button></td>
            </tr>
            <tr>
              <td>商品2</td>
              <td>2</td>
              <td>$15</td>
              <td>$30</td>
              <td><button class="btn btn-sm btn-danger"><i class="fas fa-trash"></i></button></td>
            </tr>
            <tr>
              <td>商品3</td>
              <td>1</td>
              <td>$20</td>
              <td>$20</td>
              <td><button class="btn btn-sm btn-danger"><i class="fas fa-trash"></i></button></td>
            </tr>
          </tbody>
          <tfoot>
            <tr>
              <td colspan="3"></td>
              <td>總價</td>
              <td><span class="total-price">$ 99999</span></td>
            </tr>
          </tfoot>
        </table>
        <button class="btn btn-lg btn-success empty-cart"><i class="fas fa-baby-carriage"></i> 清空購物車</button>
      </section>
    </section>
  </main>

  <!-- modal -->
  <div
    v-show="false"
    class="h-full bg-opacity-75 bg-slate-900 w-full top-0 left-0 fixed">
    <div class="bg-white mx-auto border-2 h-[75vh] p-4 top-[12vh] w-2/3 relative overflow-y-scroll">
      <h2 class="text-center mb-4">老大</h2>

      <div class="bg-no-repeat bg-top bg-contain flex h-60 w-full justify-center"
        style="background-image: url('images/cat001.jpg')">
      </div>

      <ul class="my-4 px-4">
        <li 
          class="border-bottom text-xl py-4 leading-8 block">
          <div><i class="fas fa-user"></i> <span class="ml-4">user123</span></div>
          <div><i class="fas fa-star"></i> <span class="ml-4">5</span></div>
          <div>
            <i class="fas fa-comments"></i>
            <div class="-mt-7 pl-10">這隻貓咪很可愛，而且很聽話，非常容易照顧。</div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
