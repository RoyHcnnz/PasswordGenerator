<script setup lang="ts">
import { ref, onMounted } from 'vue';
</script>

<script lang="ts">
    export default {
        methods:{
            drawMatrix(){
                
                const canvas: any =  this.$refs.Matrix;
                const context = canvas.getContext('2d');

                const latin = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
                const nums = '0123456789';

                const alphabet = latin + nums;

                const fontSize = 4;
                const columns = canvas.width/fontSize;

                const rainDrops:number[] = [];

                for( let x = 0; x < columns; x++ ) {
                    rainDrops[x] = 1;
                }

                return () => {
                    context.fillStyle = 'rgba(0, 0, 0, 0.05)';
                    context.fillRect(0, 0, canvas.width, canvas.height);
                    
                    context.fillStyle = '#0F0';
                    context.font = fontSize + 'px monospace';

                    for(let i = 0; i < rainDrops.length; i++)
                    {
                        const text = alphabet.charAt(Math.floor(Math.random() * alphabet.length));
                        context.fillText(text, i*fontSize, rainDrops[i]*fontSize);
                        
                        if(rainDrops[i]*fontSize > canvas.height && Math.random() > 0.975){
                            rainDrops[i] = 0;
                        }
                        rainDrops[i]++;
                    }
                };
            }
        },
        mounted() {
            setInterval(this.drawMatrix() , 30);
        }
    };
</script>

<template>
    <canvas class="matrix" id="Matrix" ref="Matrix"></canvas>
</template>

<style scoped>
    .matrix{
        width: 100%;
        height: 100%;
        position: absolute;
        z-index: -1;
    }
</style>