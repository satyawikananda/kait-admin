<template>
    <div class='main-content'>
        <div class="page-header">
            <div class="row">
                <div class="col-md-6">
                    <h3>Modal</h3>
                </div>
                <div class="breadcrumb">
                    
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-md-6 col-12">
                <kait-card>
                    <kait-card-header>Basic Modal</kait-card-header>
                    <kait-card-body>
                        <kait-button @click="modalBasicOpen=true">Open Modal</kait-button>
                        <kait-modal :open='modalBasicOpen' @closeModal="modalBasicOpen=false">
                            <template v-slot:modal-header>
                                Modal Header
                            </template>
                            <template v-slot:modal-body>
                                Modal Body
                            </template>
                            <template v-slot:modal-footer>
                                <span class='text-gray-600'>Modal Footer</span>
                            </template>
                        </kait-modal>
                    </kait-card-body>
                    <kait-card-footer>
                        Card Footer
                    </kait-card-footer>
                </kait-card>
            </div>
            <div class="col-md-6 col-12">
                <kait-card>
                    <kait-card-header>Modal Position</kait-card-header>
                    <kait-card-body>
                        <!-- Modal Top Left -->
                        <kait-button @click="modalPosition.topLeft = true">Top Left</kait-button>
                        <kait-modal position="top-left" :open='modalPosition.topLeft' @closeModal="modalPosition.topLeft=false">
                            <template v-slot:modal-header>
                                Modal Header
                            </template>
                            <template v-slot:modal-body>
                                Modal Body
                            </template>
                            <template v-slot:modal-footer>
                                <span class='text-gray-600'>Modal Footer</span>
                            </template>
                        </kait-modal>

                        <!-- Modal Top Right -->
                        <kait-button @click="modalPosition.topRight = true" class='ml-3'>Top Right</kait-button>
                        <kait-modal position="top-right" :open='modalPosition.topRight' @closeModal="modalPosition.topRight=false">
                            <template v-slot:modal-header>
                                Modal Header
                            </template>
                            <template v-slot:modal-body>
                                Modal Body
                            </template>
                            <template v-slot:modal-footer>
                                <span class='text-gray-600'>Modal Footer</span>
                            </template>
                        </kait-modal>

                        <!-- Modal Top Center -->
                        <kait-button @click="modalPosition.topCenter = true" class='ml-3'>Top Center</kait-button>
                        <kait-modal position="top-center" :open='modalPosition.topCenter' @closeModal="modalPosition.topCenter=false">
                            <template v-slot:modal-header>
                                Modal Header
                            </template>
                            <template v-slot:modal-body>
                                Modal Body
                            </template>
                            <template v-slot:modal-footer>
                                <span class='text-gray-600'>Modal Footer</span>
                            </template>
                        </kait-modal>

                        <!-- Modal Top Center -->
                        <kait-button @click="modalPosition.topCenter = true" class='ml-3'>Bottom Center</kait-button>
                        <kait-modal position="top-center" :open='modalPosition.topCenter' @closeModal="modalPosition.topCenter=false">
                            <template v-slot:modal-header>
                                Modal Header
                            </template>
                            <template v-slot:modal-body>
                                Modal Body
                            </template>
                            <template v-slot:modal-footer>
                                <span class='text-gray-600'>Modal Footer</span>
                            </template>
                        </kait-modal>


                    </kait-card-body>
                    <kait-card-footer>
                        More at Documentation
                    </kait-card-footer>
                </kait-card>
            </div>
        </div>
       
    </div>
</template>
<script>
import 'vue-waves-effect/dist/vueWavesEffect.css'

export default {
    data() {
        return {
            modalBasicOpen: false,
            modalPosition: {
                topLeft: false,
                topRight: false,
                topCenter: false,
                bottomleft: false,
                bottomright: false,
                bottomcenter: false,
                center: false,
            }
        }
    },
    methods: {
        openModal() {
            this.modalBasicOpen = true;
            console.log(this.modalBasicOpen)
        }
    }
}
</script>