<template>
  <div class = "lg:w-[88%] mx-auto">
    <Header/>
    <div>
      <div class = "w-full max-h-[694px] relative">
        <img class = "w-full h-full z-50"  src = "/img/hero.svg">
        <button class = "z-51 flex flex-row justify-center items-center 
        lg:p-[12px_14px] gap-[14px] absolute w-[80px] h-[30px] sm:w-[100px] sm:h-[30px]  md:w-[174px] md:h-[44px] left-[8%] 
        top-[45%] bg-[#FF5C00] rounded-[12px] font-archivo font-medium 
        md:text-sm sm:text-[13px] text-[10px] leading-[20px] text-white">Tìm hiểu thêm</button>
      </div>
      <div class = "grid grid-cols-12 py-8">
        <div class ="col-span-4"></div>
        <div class = "lg:col-span-8 sm:w-full w-[85%] mx-auto col-span-12 grid sm:grid-cols-3 gap-4">
          <div class = "sm:col-span-1 h-[248px] bg-[#F5F5F7] rounded-[27px] p-7 flex flex-col justify-between">
            <div><img src = "/img/icon1.svg"></div>
            <div>Dịch vụ chuyển phát nhanh quốc tế nhanh chóng</div>
          </div>
          <div class = "sm:col-span-1 h-[248px] bg-[#F5F5F7] rounded-[27px] p-7 flex flex-col justify-between">
            <div><img src = "/img/icon2.svg"></div>
            <div>Giao hàng tận tay, tối ưu trải nghiệm khách hàng</div>
          </div>
          <div class = "sm:col-span-1 h-[248px] bg-[#F5F5F7] rounded-[27px] p-7 flex flex-col justify-between">
            <div><img src = "/img/icon3.svg"></div>
            <div>Dễ dàng tracking và quản lý đơn hàng của bạn</div>
          </div>
        </div>
      </div>

      <div class = "grid grid-cols-12 gap-4">
        <div class = "col-span-4">
          <div class = "h-[694px] bg-[#F5F5F7] rounded-[27px] py-8 px-6">
            <div><img src = "/img/logo.svg"></div>
            <p class = "font-archivo font-medium text-4xl leading-[48px] text-black">ƯỚC TÍNH CHI PHÍ</p>
            <div class = "font-helvetica font-normal text-sm leading-[20px] text-[#17171E] opacity-70 my-4">Vui lòng nhập các thông tin sau đây để ước tính chi phí vận chuyển đơn hàng của bạn</div>
            <UForm  class="" @submit="onSubmit">
              <div class = "flex flex-col gap-2 mt-7">
                <label for="email" class="flex items-center gap-1 item text-sm font-medium leading-6 text-gray-900">
                  <span>Số điện thoại hoặc Email</span>
                  <span>
                    <svg width="6" height="6" viewBox="0 0 6 6" fill="none" xmlns="http://www.w3.org/2000/svg">
                      <path d="M1.946 5.96L1.19 5.386L2.534 3.664L0.42 3.034L0.728 2.124L2.772 2.894L2.702 0.695999H3.668L3.584 2.894L5.67 2.124L5.95 3.034L3.836 3.65L5.194 5.386L4.41 5.96L3.192 4.112L1.946 5.96Z" fill="#E8173C"/>
                    </svg>
                  </span>
                </label>
                <UInput size = "xl"  :ui="{ color: { variant: { none: 'bg-transparent focus:ring-0 focus:shadow-none' } } }" placeholder="Nhập số điện thoại hoặc email" class = "bg-white border border-[#E5E5E5] rounded-[10px] box-input">
                  <template #leading>
                    <UAvatar
                      src="/img/user.svg"
                      size="xs"
                    />
                  </template>
                </UInput>
              </div>
              <div class = "grid grid-cols-3 gap-3 mt-4">
                <div class = "col-span-1 flex flex-col gap-2">
                  <label for="email" class="flex items-center gap-1 item text-sm font-medium leading-6 text-gray-900">
                    <span>Dài</span>
                    <span>
                      <svg width="6" height="6" viewBox="0 0 6 6" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M1.946 5.96L1.19 5.386L2.534 3.664L0.42 3.034L0.728 2.124L2.772 2.894L2.702 0.695999H3.668L3.584 2.894L5.67 2.124L5.95 3.034L3.836 3.65L5.194 5.386L4.41 5.96L3.192 4.112L1.946 5.96Z" fill="#E8173C"/>
                      </svg>
                    </span>
                  </label>
                  <UInput size = "xl"  :ui="{ color: { variant: { none: 'bg-transparent focus:ring-0 focus:shadow-none' } } }" class = "bg-white border border-[#E5E5E5] rounded-[10px] box-input">
                    <template #trailing>
                      <span class="font-helvetica font-normal text-sm leading-[20px] text-[#868689]">cm</span>
                    </template>
                  </UInput>
                </div>
                <div class = "col-span-1 flex flex-col gap-2">
                  <label for="email" class="flex items-center gap-1 item text-sm font-medium leading-6 text-gray-900">
                    <span>Rộng</span>
                    <span>
                      <svg width="6" height="6" viewBox="0 0 6 6" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M1.946 5.96L1.19 5.386L2.534 3.664L0.42 3.034L0.728 2.124L2.772 2.894L2.702 0.695999H3.668L3.584 2.894L5.67 2.124L5.95 3.034L3.836 3.65L5.194 5.386L4.41 5.96L3.192 4.112L1.946 5.96Z" fill="#E8173C"/>
                      </svg>
                    </span>
                  </label>
                  <UInput size = "xl"  :ui="{ color: { variant: { none: 'bg-transparent focus:ring-0 focus:shadow-none' } } }" class = "bg-white border border-[#E5E5E5] rounded-[10px] box-input">
                    <template #trailing>
                      <span class="font-helvetica font-normal text-sm leading-[20px] text-[#868689]">cm</span>
                    </template>
                  </UInput>
                </div>
                <div class = "col-span-1 flex flex-col gap-2">
                  <label for="email" class="flex items-center gap-1 item text-sm font-medium leading-6 text-gray-900">
                    <span>Cao</span>
                    <span>
                      <svg width="6" height="6" viewBox="0 0 6 6" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M1.946 5.96L1.19 5.386L2.534 3.664L0.42 3.034L0.728 2.124L2.772 2.894L2.702 0.695999H3.668L3.584 2.894L5.67 2.124L5.95 3.034L3.836 3.65L5.194 5.386L4.41 5.96L3.192 4.112L1.946 5.96Z" fill="#E8173C"/>
                      </svg>
                    </span>
                  </label>
                  <UInput size = "xl"  :ui="{ color: { variant: { none: 'bg-transparent focus:ring-0 focus:shadow-none' } } }" class = "bg-white border border-[#E5E5E5] rounded-[10px] box-input">
                    <template #trailing>
                      <span class="font-helvetica font-normal text-sm leading-[20px] text-[#868689]">cm</span>
                    </template>
                  </UInput>
                </div>
              </div>
              <div class = "flex flex-col gap-2 mt-5">
                <label  class="flex items-center gap-1 item text-sm font-medium leading-6 text-gray-900">
                  <span>Trọng lượng</span>
                  <span>
                    <svg width="6" height="6" viewBox="0 0 6 6" fill="none" xmlns="http://www.w3.org/2000/svg">
                      <path d="M1.946 5.96L1.19 5.386L2.534 3.664L0.42 3.034L0.728 2.124L2.772 2.894L2.702 0.695999H3.668L3.584 2.894L5.67 2.124L5.95 3.034L3.836 3.65L5.194 5.386L4.41 5.96L3.192 4.112L1.946 5.96Z" fill="#E8173C"/>
                    </svg>
                  </span>
                </label>
                <UInput size = "xl"  :ui="{ color: { variant: { none: 'bg-transparent focus:ring-0 focus:shadow-none' } } }" placeholder="Nhập trọng lượng" class = "bg-white border border-[#E5E5E5] rounded-[10px] box-input">
                  <template #leading>
                    <UAvatar
                      src="/img/icon-weight.svg"
                      size="xs"
                    />
                  </template>
                  <template #trailing>
                      <span class="font-helvetica font-normal text-sm leading-[20px] text-[#868689]">gram</span>
                  </template>
                </UInput>
              </div>
              <div class = "flex justify-between mt-8 items-center">
                <div class = "flex flex-col">
                  <p class = "font-helvetica font-normal text-xs leading-[20px] flex items-center text-[#868689]">Cước tạm tính</p>
                  <p class = "font-helvetica font-medium text-[20px] leading-[32px] flex items-center text-[#17171E]">$1000.00</p>
                </div>
                <button class = "flex flex-row justify-center
                 p-[12px_14px] gap-[14px] w-[128px]
                 h-[44px] left-[260px] top-[498px] bg-[#FF5C00] rounded-[12px]
                 font-archivo font-medium text-[14px] leading-[20px] items-center
                  text-white flex-none order-0 flex-grow-0">Tính giá</button>
              </div>
            </UForm>
          </div>
        </div>
        <div class = "col-span-8">
          <img src = "/img/icon4.svg">
        </div>
      </div>
      <div class = "service  my-10">
        <div class = "font-archivo font-normal font-medium text-[40px] leading-[60px] 
            uppercase text-[#17171E]">
          <p>DỊCH VỤ CỦA</p>
          <p>THE HUMAN EXPRESS</p>
        </div>
        <div class = "grid grid-cols-2 mt-6">
          <div class = "col-span-1 h-[441px] bg-[#FF5C00] rounded-[27px] flex flex-col p-3">
            <div>
              <img src = "/img/international_shipping.png">
            </div>
            <div>
             <p>VẬN CHUYỂN QUỐC TẾ</p>
             <p>Với tính kịp thời ổn định và dịch vụ tiết kiệm chi phí, dịch vụ của chúng tôi đã được nhiều khách hàng tin tưởng và đánh giá cao</p> 
            </div>
          </div>
          <div></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>

</script>

<style scoped>
.icon-user{background: url("/img/user.svg") no-repeat 0 0/contain;}
.box-input:focus {
  border: none !important;
}
</style>