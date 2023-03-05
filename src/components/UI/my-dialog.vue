<template>
  <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="exampleModalLabel">Создать магазин</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <div class="modal-inputs d-flex justify-content-between mb-4">
            <div class="modal-inputs-item">
              <div class="modal-inputs-item-title title mb-2">Шаблон</div>
              <select class="form-select" aria-label="Default select example">
                <option selected>Стандартный</option>
                <option value="1">Стандартный</option>
                <option value="2">Стандартный</option>
                <option value="3">Стандартный</option>
              </select>
            </div>
            <div class="modal-inputs-item">
              <div class="modal-inputs-item-title title mb-2">Цветовая схема</div>
              <select class="form-select" aria-label="Default select example">
                <option selected>Классическая</option>
                <option value="1">Классическая</option>
                <option value="2">Классическая</option>
                <option value="3">Классическая</option>
              </select>
            </div>
          </div>
          <div class="modal-domen mb-4">
            <div class="modal-domen-title title mb-2">
              Домен
            </div>
            <div class="input-group mb-3">
              <input type="text" class="form-control" placeholder="Например: ivangrozniy"
                     aria-label="Recipient's username" aria-describedby="basic-addon2">
              <div class="input-group-append">
                <span class="input-group-text" id="basic-addon2">.work5.ru</span>
              </div>
            </div>
          </div>
          <div class="modal-description d-flex align-items-center">
            <div class="modal-description-img">
              <svg width="52" height="52" viewBox="0 0 52 52" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0_11_287)">
                  <mask id="mask0_11_287" style="mask-type:luminance" maskUnits="userSpaceOnUse" x="0" y="0" width="52"
                        height="52">
                    <rect width="52" height="52" fill="white"/>
                  </mask>
                  <g mask="url(#mask0_11_287)">
                  </g>
                  <g clip-path="url(#clip1_11_287)">
                    <path fill-rule="evenodd" clip-rule="evenodd"
                          d="M25.9253 0.944702C39.7224 0.944702 50.9059 11.8313 50.9059 25.2595C50.9059 38.6878 39.7224 49.5743 25.9253 49.5743C12.1282 49.5743 0.944702 38.6878 0.944702 25.2595C0.944702 11.8313 12.1282 0.944702 25.9253 0.944702V0.944702Z"
                          stroke="#6666D2" stroke-width="1.8894" stroke-miterlimit="22.9256"/>
                    <path
                        d="M23.6895 27.3918H27.9092V12.8434H23.6895V27.3918ZM28.8269 29.2272H22.7718C22.2635 29.2272 21.8541 28.8179 21.8541 28.3095V11.9302C21.8541 11.4219 22.2635 11.0125 22.7718 11.0125H28.8269C29.3353 11.0125 29.7446 11.4219 29.7446 11.9302V28.3095C29.7446 28.8179 29.3353 29.2272 28.8269 29.2272Z"
                        fill="#6666D2"/>
                    <path
                        d="M23.6895 38.0894H27.9092V34.4366H23.6895V38.0894ZM28.8269 39.9248H22.7718C22.2635 39.9248 21.8541 39.5155 21.8541 39.0071V33.5189C21.8541 33.0105 22.2635 32.6012 22.7718 32.6012H28.8269C29.3353 32.6012 29.7446 33.0105 29.7446 33.5189V39.0071C29.7446 39.5155 29.3353 39.9248 28.8269 39.9248Z"
                        fill="#6666D2"/>
                  </g>
                </g>
                <defs>
                  <clipPath id="clip0_11_287">
                    <rect width="52" height="52" fill="white"/>
                  </clipPath>
                  <clipPath id="clip1_11_287">
                    <rect width="51.8506" height="50.5145" fill="white"/>
                  </clipPath>
                </defs>
              </svg>
            </div>
            <div class="modal-description-text ms-3">
              В названии домена разрешены латиница и “-”, запрещается использовать словосочетание Work 5. После создания
              магазина Вы сможете прикрутить свой домен (например ivangrozniy.ru). Подробнее по <a href="#">ссылке</a>
            </div>
          </div>
        </div>
        <div class="modal-footer">
          <div>
            <my-button data-bs-dismiss="modal" class-btn="btn-secondary"
                       color-btn="#B1B1B1" hover-color-btn="gray">
              <div class="btn-text">Отмена</div>
            </my-button>
          </div>
          <my-button class-btn="btn-success"
                     color-btn="#55C97B" hover-color-btn="green">
            <div class="btn-text">Создать</div>
          </my-button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import MyButton from "@/components/UI/my-button.vue";

export default {
  name: "my-dialog",
  components: {MyButton}
}
</script>

<style scoped>

.modal-dialog {
  height: 100%;
  width: 100%;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: center;
  max-width: none;
}

.title {
  color: black;
}

.modal-content {
  width: 100%;
  max-width: 620px;
}

.modal-header, .modal-footer{
  border: none;
}

.modal-footer{
  justify-content: flex-start;
}

.modal-inputs-item {
  width: 240px;
}

.input-group-text {
  color: white;
  background: #6666CC;
  padding-right: 40px;
  padding-left: 40px;
}

.btn-close {
  background-size: 65%;
  background-image: url('src/assets/img/close.svg');
}

.modal-description-text a{
  text-decoration: none;
  color: #6666CC;
}

</style>