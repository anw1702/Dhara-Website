<script lang="ts">
    const verticalLines = Array.from({ length: Math.ceil(1440 / 280) }, (_, i) => i * 280);
    const horizontalLines = Array.from({ length: Math.ceil(612 / 195) }, (_, i) => i * 195);
    </script>
    
    <div class="absolute inset-0 pointer-events-none">
      {#each verticalLines as x}
        <svg xmlns="http://www.w3.org/2000/svg" width="2" height="612" viewBox="0 0 2 612" fill="none" style="position: absolute; left: {x}px; top: 0;">
          <path d="M1 -150V1002" stroke="url(#paint0_linear_1_641)" stroke-opacity="0.15" stroke-width="1.5"/>
          <defs>
            <linearGradient id="paint0_linear_1_641" x1="1.5" y1="-150" x2="1.5" y2="1002" gradientUnits="userSpaceOnUse">
              <stop stop-color="#B7BDC6" stop-opacity="0"/>
              <stop offset="0.505" stop-color="#B7BDC6"/>
              <stop offset="1" stop-color="#B7BDC6" stop-opacity="0"/>
            </linearGradient>
          </defs>
        </svg>
      {/each}
    
      {#each horizontalLines as y}
        <svg xmlns="http://www.w3.org/2000/svg" width="1440" height="2" viewBox="0 0 1440 2" fill="none" style="position: absolute; left: 0; top: {y}px;">
          <path d="M-418 0.972168L1502 0.972394" stroke="url(#paint0_linear_1_639)" stroke-opacity="0.15" stroke-width="1.5"/>
          <defs>
            <linearGradient id="paint0_linear_1_639" x1="-418" y1="0.472168" x2="1502" y2="0.472293" gradientUnits="userSpaceOnUse">
              <stop stop-color="#B7BDC6" stop-opacity="0"/>
              <stop offset="0.505" stop-color="#B7BDC6"/>
              <stop offset="1" stop-color="#B7BDC6" stop-opacity="0"/>
            </linearGradient>
          </defs>
        </svg>
      {/each}
    </div>