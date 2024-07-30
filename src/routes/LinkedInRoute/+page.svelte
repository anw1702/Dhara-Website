<script lang="ts">
    import { onMount } from "svelte";
    import In from '@/img/LinkedIn.png';
  
    let isAndroid: boolean = false;
  
    onMount(() => {
      isAndroid = /Android/i.test(navigator.userAgent);
    });
  </script>
  
  <style>
    .dialog-box {
      @apply bg-white rounded-lg shadow-lg p-6 relative overflow-hidden;
      @apply  mx-auto;
      @apply flex items-center justify-center;
      @apply text-gray-800 text-2xl;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  
    .dialog-box::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, #ff6ec4, #7873f5, #43e97b, #38f9d7);
      background-size: 400% 400%;
      animation: gradient-flow 15s linear infinite;
      z-index: -1;
    }
  
    .dialog-box::after {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      border: 2px solid transparent;
      border-radius: inherit;
      box-sizing: border-box;
      z-index: -1;
    }
  
    @keyframes gradient-flow {
      0% {
        background-position: 0% 50%;
      }
      50% {
        background-position: 100% 50%;
      }
      100% {
        background-position: 0% 50%;
      }
    }
  
    .dialog-box img {
      @apply mx-2 w-12 h-12;
    }
  
    @media (min-width: 640px) {
      .dialog-box {
        @apply p-8;
        @apply text-3xl;
      }
  
      .dialog-box img {
        @apply w-48 h-12;
      }
    }
  </style>
  
  <main class="min-h-screen flex items-center justify-center bg-gray-100">
    <div class="dialog-box">
      <p>We will be on</p>
      <img src={In} alt="Twitter X" />
      <p>soon...</p>
    </div>
  </main>
  