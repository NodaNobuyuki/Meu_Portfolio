<script>
    export let y;
    let tabs = [
        {name: 'Projetos', link:'#projetos'},
        {name: 'Sobre Mim', link: '#sobre'},

    ];

    import { locale } from "svelte-i18n";

    const switchToEnglish = () => {
        locale.set('en');
    };
</script>



<header class={'sticky z-[50] top-0 duration-200 px-6 flex items-center justify-between border border-solid' + (
    y > 0 
            ? 'py-4 bg-slate-950 border-violet-950' 
            : 'py-6 bg-transparent border-transparent')}>
    <h1 class="font-medium">
        
        <b class="font orbitron">Carlos </b> Nobuyuki Noda Jr
        
    </h1>

    <!-- faz o botão trocar de c-->
    <div class="sm:flex ml-auto pr-4 items-center gap-4 hidden">
         {#each tabs as tab, index}
            <a href={tab.link} class="duration-200 hover:text-violet-400" target={index === 2 ? "_blank" : ""}>
                <p>{tab.name}</p>
            </a>
         {/each}
    </div>
    <a href="https://www.linkedin.com/in/carlos-nobuyuki-13b079261/"
    target="_blank"
    
        class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white
        text-slate-950">
        <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 
        group-hover:translate-x-full z-0 duration-200">
    
        </div>
        <h4 class="relative z-9"> Entre em contato!</h4>
    </a>

    
</header>