<template>
<div class="lg:p-8 xl:p-8 sm:p-8 xs:p-8 space-y-4">
  <span class="text-4xl sm:mb-4 xs:text-base lg:mb-0 xl:mb-4 text-green-400 font-semibold">Valoraciones del producto</span>
  <p class="text-2xl lg:hidden xs:text-base sm:mb-4 lg:mb-0 xl:mb-4 text-black-200 font-semibold">Aquí puedes consultar las últimas valoraciones que los usuarios han hecho sobre este producto.</p>
  <div class="grid xs:grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-3">
        <div v-for="(item, index) in tests" :key="index">
          <a class="group block rounded-lg p-4 border border-gray-200">
            <dl class="xs:block sm:block lg:block xl:block grid-cols-2 grid-rows-2 items-center">
              <div class="grid grid-cols-3 gap-3">
                <svg width="120" height="24" viewBox="0 0 120 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <mask id="mask0" mask-type="alpha" maskUnits="userSpaceOnUse" x="0" y="0" width="24" height="24">
                  <g clip-path="url(#clip0)">
                  <path d="M12 17.27L18.18 21L16.54 13.97L22 9.24L14.81 8.63L12 2L9.19 8.63L2 9.24L7.46 13.97L5.82 21L12 17.27Z" fill="black"/>
                  </g>
                  </mask>
                  <g mask="url(#mask0)">
                  <rect width="24" height="24" fill="#FFD033"/>
                  </g>
                  <mask id="mask1" mask-type="alpha" maskUnits="userSpaceOnUse" x="24" y="0" width="24" height="24">
                  <g clip-path="url(#clip1)">
                  <path d="M36 17.27L42.18 21L40.54 13.97L46 9.24L38.81 8.63L36 2L33.19 8.63L26 9.24L31.46 13.97L29.82 21L36 17.27Z" fill="black"/>
                  </g>
                  </mask>
                  <g mask="url(#mask1)">
                  <rect x="24" width="24" height="24" fill="#FFD033"/>
                  </g>
                  <mask id="mask2" mask-type="alpha" maskUnits="userSpaceOnUse" x="48" y="0" width="24" height="24">
                  <g clip-path="url(#clip2)">
                  <path d="M60 17.27L66.18 21L64.54 13.97L70 9.24L62.81 8.63L60 2L57.19 8.63L50 9.24L55.46 13.97L53.82 21L60 17.27Z" fill="black"/>
                  </g>
                  </mask>
                  <g mask="url(#mask2)">
                  <rect x="48" width="24" height="24" fill="#FFD033"/>
                  </g>
                  <mask id="mask3" mask-type="alpha" maskUnits="userSpaceOnUse" x="72" y="0" width="24" height="24">
                  <g clip-path="url(#clip3)">
                  <path d="M84 17.27L90.18 21L88.54 13.97L94 9.24L86.81 8.63L84 2L81.19 8.63L74 9.24L79.46 13.97L77.82 21L84 17.27Z" fill="black"/>
                  </g>
                  </mask>
                  <g mask="url(#mask3)">
                  <rect x="72" width="24" height="24" fill="#FFD033"/>
                  </g>
                  <mask id="mask4" mask-type="alpha" maskUnits="userSpaceOnUse" x="96" y="0" width="24" height="24">
                  <g clip-path="url(#clip4)">
                  <path d="M108 17.27L114.18 21L112.54 13.97L118 9.24L110.81 8.63L108 2L105.19 8.63L98 9.24L103.46 13.97L101.82 21L108 17.27Z" fill="black"/>
                  </g>
                  </mask>
                  <g mask="url(#mask4)">
                  <rect x="96" width="24" height="24" fill="#FFD033"/>
                  </g>
                  <defs>
                  <clipPath id="clip0">
                  <rect width="24" height="24" fill="white"/>
                  </clipPath>
                  <clipPath id="clip1">
                  <rect width="24" height="24" fill="white" transform="translate(24)"/>
                  </clipPath>
                  <clipPath id="clip2">
                  <rect width="24" height="24" fill="white" transform="translate(48)"/>
                  </clipPath>
                  <clipPath id="clip3">
                  <rect width="24" height="24" fill="white" transform="translate(72)"/>
                  </clipPath>
                  <clipPath id="clip4">
                  <rect width="24" height="24" fill="white" transform="translate(96)"/>
                  </clipPath>
                  </defs>
                </svg>

                <dd class="group-hover:text-light-blue-200 text-sm font-medium xs:mb-4 sm:mb-4 lg:mb-4 xl:mb-4 ml-6">
                  {{item.rating}},0
                </dd>
              </div>
              <div>
                <dd class="group-hover:text-white leading-6 text-xs text-gray-600">
                {{item.author}} el {{item.date}}
                </dd>
              </div>
              <div>
                <dd class="text-sm  sm:mb-4 lg:mb-0 xl:mb-4 text-black-200 font-semibold">
                  {{item.comment}}
                </dd>
              </div>
              <div class="grid grid-cols-3 gap-3">
                  <button @click="test(item)"
                  :disabled="item.disabled"
                  v-bind:style="!item.disabled ? 'background: transparent' : 'background: #359435'"
                  id="#butDisabled"
                  class="flex items-center text-light-blue-600 text-sm font-medium xs:px-0 sm:px-0 lg:px-0 xl:px-4 py-2 border border-gray-200">
                  <svg width="32" height="29" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <mask id="mask0" mask-type="alpha" maskUnits="userSpaceOnUse" x="8" y="7" width="16" height="16">
                    <g clip-path="url(#clip0)">
                    <path d="M9.33337 20.3333H10.6667C11.0334 20.3333 11.3334 20.0333 11.3334 19.6667V13.6667C11.3334 13.3 11.0334 13 10.6667 13H9.33337V20.3333ZM22.5534 15.5867C22.6267 15.42 22.6667 15.24 22.6667 15.0533V14.3333C22.6667 13.6 22.0667 13 21.3334 13H17.6667L18.28 9.90001C18.3134 9.75334 18.2934 9.59334 18.2267 9.46001C18.0734 9.16001 17.88 8.88668 17.64 8.64668L17.3334 8.33334L13.06 12.6067C12.8067 12.86 12.6667 13.2 12.6667 13.5533V18.78C12.6667 19.6333 13.3667 20.3333 14.2267 20.3333H19.6334C20.1 20.3333 20.54 20.0867 20.78 19.6867L22.5534 15.5867Z" fill="black"/>
                    </g>
                    </mask>
                    <g mask="url(#mask0)">
                    <rect x="8" y="7" width="16" height="16" fill="black"/>
                    </g>
                    <defs>
                    <clipPath id="clip0">
                    <rect width="16" height="16" fill="black" transform="translate(8 7)"/>
                    </clipPath>
                    </defs>
                  </svg>
                    Es util
                </button>
                <div class="col-span-2 xs:px-7">
                  {{item.useful_count}} personas creéis que es útil
                </div>
              </div>
            </dl>
          </a>

        </div>
    </div> 
  </div>
  
  
</template>

<script>
import axios from 'axios'

export default {

  async asyncData() {
    const { data } = await axios.get(`http://localhost:3000/api/valoraciones`)
    let info = data.reviews.map((item) => {
     let time = item.date.substr(0,10).replace(/\-/g, ",");
     var fecha = new Date(time);
     var options = { weekday: 'long', year: 'numeric', month: 'long', day:'numeric' };
     item.date = fecha.toLocaleDateString("es-ES", options)
     item.disabled = false
     return item
    })
    return { tests: info}
  },
  methods: {
    test: function (val) {
      val.useful_count++
      val.disabled = true        
    },
  },
}
</script>
