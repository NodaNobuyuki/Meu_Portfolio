<script>
    import { createEventDispatcher } from "svelte";
    import Step from "./Step.svelte"

    let steps = [
        {name: 'Cursando Segurança da Informação, na Fatec Ourinhos', icon: 'fa-solid fa-shield-halved'},
        {name: 'IDS e Machine Learning', icon: 'fa-solid fa-charging-station'},
        {name: 'Credenciado pela AMBIMA, na certificação CPA-10', icon: 'fa-solid fa-dollar-sign'},
        
    ];
    let benefits = [
        {name: 'Administrador de Redes e Segurança', description: 'Experiência com Linux, Zabbix, e integração do Suricata com ELK Stack para monitoramento avançado.' },
        {name: 'Desenvolvedor de Machine Learning', description: 'Desenvolvimento de Sistemas de Detecção de Intrusão para carros elétricos utilizando redes neurais, cobrindo desde a normalização de um dataset especializado até as parametrizações finais.'},
        {name: 'Escritor por Hobby', description: 'Com o fim de aprimorar minha escrita em Inglês, criei uma página no Substack, uma página pessoal para escrever sobre assuntos diversos, desde atualidades até assuntos de interesse pessoal.'},
        {name: 'Entusiásta de Estatística e Análise de Dados', description: 'Aplicação de álgebra linear e estatística em projetos diversos para análise e previsões.'},
        { name: 'Profissional credenciado CPA-10 – ANBIMA', description: 'Obtive a certificação CPA-10 da ANBIMA, que valida meus conhecimentos sobre o mercado financeiro, produtos de investimento, fundos de investimento e conceitos essenciais de economia e renda fixa/variável.' },
    ]
</script>

<main class="flex flex-col flex=1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 
        lg:gap-10">
            <h2 class="font text-4xl sm:text-5xl md:text-6xl">
                Olá! Eu sou <span class="orbitron text-violet-400">Carlos Nobuyuki  </span>
                <br> Tecnólogo em <span class="orbitron text-violet-400">Segurança da Informação </span>

            </h2>
            <p class="text-base sm:text-lg md:text-xl">
            IA, Cybersegurança e profissional certificado pela AMBIMA!   
            </p>

            <a class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins
            relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer" 
            href="https://www.linkedin.com/in/carlos-nobuyuki-13b079261/" target="_blank">
            <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 
            group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9"> Entre em contato! &rarr;</h4>
            </a>
        </div>
        <div class="relative grid place-items-center mx-auto">
            <img src={"images/profile.jpg"} 
                 alt="Perfil" 
                 class="object-cover z-[2] max-h-[70vh] w-full max-w-[550px] sm:max-w-[550px]"/>
        </div>
            
    </section>
    
    <section id="projetos" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
      

            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Um pouco mais sobre <span class="poppins text-violet-400">minhas habilidades</span>
            </h3>
            

        </div>
      

        <div class="grid grid-cols-l lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}> 
                <p>Experiência com segurança em <strong class="text-violet-400">redes de computadores, banco de dados e sistemas operacionais,</strong> além de aulas sobre programação e desenvolvimento de sistemas seguros!</p>
            </Step>

            <Step step={steps[1]}> 
                <p>Pesquisa científica sobre um IDS com utilização de Machine Learning <strong class="text-violet-400"> para carros elétricos,</strong> para a proteção contra spoofing e DDoS!</p>
            </Step>

            <Step step={steps[2]}> 
                <p>Conhecimentos em <strong class="text-violet-400"> produtos de investimento</strong>, <strong class="text-violet-400">fundamentos de economia</strong>, <strong class="text-violet-400">gestão de risco e compliance!</strong> </p>
            </Step>
        </div>
    </section>
    <section id="sobre" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 
        before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 
        after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl">Quer saber mais</h6>
            <h3 class="font-semibold text-exl sm:text-4xl md:text-5xl"> 
                Um pouco <span class="poppins text-violet-400"> sobre mim? </span> 
            </h3>
        </div>

        <p class="mx-auto poppins font-semibold text-xl sm:text-xl md:text-2xl">Eu sou...</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w [800px]">
            {#each benefits as benefits, index}
            <div class="flex gap-6 sm:gap-8">
                <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                    0{index+1}
                </p>
                <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-2xl sm:text-3xl md:text-5xl">
                        {benefits.name}
                    </h3>
                    <p>{benefits.description}</p>
                </div>
            </div>
            {/each }
        </div>
    </section>
</main>