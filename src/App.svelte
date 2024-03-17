<script>
    // COMPONENTS
    // import { onMount } from 'svelte';
    import QuoteBox from '$components/Quote-box.svelte';

    // IMAGES
    import smith from '$images/smith.jpg';
    import deleon from '$images/de-leon.jpg';

    // VARIABLES

    // REACTIVE VARIABLES


    // async function init() {
    // }

    // onMount(init);
</script>

<header>
    <h1>HeD</h1>
</header>

<main id="container">
    <div id="panel-01" class="row panel no-border">
        <div class="center">
            <p class="purple-backdrop"><span class="bold">In 2023,</span> the McCreary Centre Society released its <a href="https://mcs.bc.ca/about_bcahs" target="_blank">latest survey</a> on the health of British Columbian teens. The survey has been conducted every five years for the past 30 years and is believed to accurately represent over 95% of B.C.’s 12- to 19-year-olds.</p>
            <p class="text-emphasis">It was the first post-pandemic survey and it found that <span class="purple">nonbinary youth</span> had significantly worse mental heath outcomes than their <span class="green">male</span> and <span class="lite-green">female</span> peers.</p>
            <p class="note">(Tap or click any chart for more info)</p>
        </div>
    </div>
    <!-- <div class="row legend no-border flex-container">
        <p class="">GUIDE: </p>
        <p><span class="swatch green"></span>Male</p>
        <p><span class="swatch lite-green"></span>Female</p>
        <p><span class="swatch purple"></span>Nonbinary</p>
    </div> -->
    <div class="row">
        <div class="panel two-third">
            <p>The survey found that nonbinary youth faced a much greater risk of serious mental health issues...</p>
            <iframe src='https://flo.uri.sh/story/2282024/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:200px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>
        </div>
        <div class="panel third">
            <p>... and reported higher levels of anxiety, depression and PTSD.</p>
            <iframe src='https://flo.uri.sh/visualisation/17044513/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:200px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>
        </div>
    </div>
    <div class="row text-row flex-center">
        <p class="text-container">Nonbinary youth made up</p>
        <p class="big-text purple bold-italic">5%</p>
        <p>of teens in B.C., according to the survey....</p>
    </div>
    <div class="row">
        <QuoteBox 
            align='right'
            id='deleon'
            image={deleon}
            imageAlt=''
            source='Nik De Leon, a nonbinary and genderqueer 18-year-old'
            quoteText='That five per cent is made up of youth, and youth who are struggling. And you can’t just swipe that under the rug. <span class="purple">These are people, these are kids.</span> And to ignore them, you’re neglecting this huge community.'
        />
    </div>
    <div class="row" id="panel-outcomes">
        <div class="panel full">
            <p>... but they face disproportionately high levels of bullying, abuse, exclusion and harassment.</p>
            <iframe src='https://flo.uri.sh/story/2282044/embed' title='Interactive or visual content' class='flourish-embed-iframe' frameborder='0' scrolling='no' style='width:100%;height:260px;' sandbox='allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation'></iframe>
        </div>
    </div>
    <div class="row">
        <QuoteBox 
            align='left'
            id='smith-quote'
            image={smith}
            quoteText='We definitely see young people who identify as nonbinary experiencing higher rates of <span class="purple">violence, discrimination, harassment, abuse, social exclusion, trauma, stigma.</span>'
            source='Annie Smith, executive director of the McCreary Centre Society'
        />
    </div>
    <div class="row" id="solutions-row">
        <div class="panel full no-border">
            <h2 class="center subhead purple-backdrop">Solutions exist, experts say, but there’s lots of work to be done</h2>
            <div class="text-block flex-container">
                <p class="border">Experts say things like gay-straight alliance clubs, LGBTQ+ inclusion policies, and gender-diversity classes in school can all help, but they need to be expanded and better supported.</p>
                <p class="border">Recently, though, there’s been a political and public backlash, with anti-SOGI protests in B.C. and several provinces putting policies in place that disproportionately target nonbinary youth.</p>
            </div>
        </div>
    </div>
    <div class="row">
        <QuoteBox 
            align='right'
            id='smith-quote-02'
            image={smith}
            maxWidth='150px'
            quoteText='It’s <span class="purple">all our responsibility</span> to really look at this data and think about how we can make safer spaces for these young people. <span class="purple">Because we know they’ll thrive if we do.</span>'
        />
    </div>
</main>

<footer>
    <p class="source">Source:  <a href="tk" target="_blank">tK</a></p>
</footer>
  
<style>
    @import '$css/normalize.css';
    @import '$css/fonts.css';
    @import '$css/colors.css';
    @import '$css/app.css';
    @import '$css/layout.css';
    /* @import '$css/legend.css'; */


    :global(#container .bold) {
        font-family: 'BentonSansCond-Bold';
    }
    :global(#container .bold-italic) {
        font-family: 'BentonSansCond-BoldItalic';
    }
    :global(#container .note) {
        color: var(--grey03);
        font-family: 'BentonSansCond-RegItalic';
    }
    :global(#container .center) {
        margin: 0 auto;
        text-align: center;
    }
    #container .big-text {
        font-size: 3rem;
        margin: 5px;
        width: 50px;
    }
    :global(#app .source a:hover) {
	    color: var(--brite_purple01);
	    transition: color ease-in-out 0.3s;
    }
    #container .text-block {
        filter: drop-shadow(6px 8px 4px rgba(155,63,134,0.3));
    }
    #container .text-block p {
        background-color: rgba(155,63,134,0.25); 
        border: 3px solid var(--brite_purple01);
        text-shadow: -1px 1px 2px #FFF;
    }
    .purple-backdrop {
        background-color: #9b3f86;
        border-radius: 5px;
        color: #FFF !important;
        margin-bottom: 20px !important;
        padding: 10px 4px;
        stroke-width: 0.25px;
        -webkit-stroke-width: 0.25px;
        text-shadow: 1px 2px 2px #231F20;
        transform: rotate(-1.2deg);
    }
    .purple-backdrop a {
        color: #FFF !important;
    }
    #container h2.subhead.purple-backdrop {
        transform: rotate(1.3deg);
    }
  


    /* SPECIFIC PANELS */
    #panel-01 p {
        margin: 7px 0;
        max-width: 500px;
    }
    #panel-01 p:nth-of-type(2) {
        margin: 0 auto;
        max-width: 450px;
        
    }
    #panel-01 p:first-of-type span:first-of-type {
        display: block;
        font-size: 2rem;
        margin: 8px 0 8px 5px;
        text-align: left;
        text-shadow: 2px 2px 2px #231F20;
    }
    #nb-pct-quote .chart-block {
        /* width: 25%; */
    }
    #nb-pct-quote .center-text {
        font-size: 4rem;
        left: 52%;
        position: absolute;
        top: 36%;
        transform: translate(-50%, 0);
    }
    #smith-quote-02 .image-quote-block {
        max-width: 500px;
    }
    #smith-quote-02 img {
        max-width: 150px;
        right: -20px;
        top: -10px;
    }
    #solutions-row,
    #panel-outcomes {
        margin-top: 2.2rem;
    }

    @media only screen and (min-width: 550px) {
        #container .big-text {
            font-size: 3rem;
            margin: 0 25px 0 5px;
            width: 50px;
        }
    }
</style>
