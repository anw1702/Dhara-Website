<script lang="ts">
    export interface Feature {
      icon: string;
      title: string;
      description: string;
    }
    
    export let feature: Feature;
    </script>
    
    <div class="flex flex-col justify-center p-4 {feature.title !== 'Security' ? 'mt-5' : 'my-auto'} bg-emerald-800 rounded-xl border border-emerald-700 border-solid backdrop-blur-[2px]">
      <img loading="lazy" src={feature.icon} alt="" class="rounded-md aspect-square w-[50px]" />
      <h2 class="mt-5 text-2xl">{feature.title}</h2>
      <p class="mt-2 text-sm font-light leading-5">{feature.description}</p>
    </div>