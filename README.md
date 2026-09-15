<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>John H. Torrejos — Molecular Biology &amp; Bioinformatics Researcher</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#1B2320;
    --paper:#F5F6F0;
    --paper-deep:#ECEEE4;
    --rule:#D8D9CC;
    --green:#3B6E52;   /* A */
    --blue:#2B5A82;    /* C */
    --rust:#A63D40;    /* T */
    --dark:#1B2320;    /* G */
    --muted:#5B6259;
    --max:740px;
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--paper);
    color:var(--ink);
    font-family:'Inter',sans-serif;
    font-size:17px;
    line-height:1.65;
    -webkit-font-smoothing:antialiased;
  }
  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.001ms !important; animation-iteration-count:1 !important; transition-duration:0.001ms !important;}
  }

  h1,h2,h3{
    font-family:'Fraunces',serif;
    font-weight:500;
    margin:0;
    color:var(--dark);
  }

  a{color:inherit;}

  .mono{
    font-family:'JetBrains Mono',monospace;
    letter-spacing:0.01em;
  }

  .wrap{
    max-width:var(--max);
    margin:0 auto;
    padding:0 28px;
  }

  /* ---------- nav ---------- */
  nav{
    position:sticky; top:0; z-index:10;
    background:rgba(245,246,240,0.92);
    backdrop-filter:blur(6px);
    border-bottom:1px solid var(--rule);
  }
  nav .wrap{
    display:flex; align-items:center; justify-content:space-between;
    padding-top:16px; padding-bottom:16px;
  }
  .nav-mark{
    font-family:'JetBrains Mono',monospace;
    font-size:14px;
    font-weight:500;
  }
  .nav-links{
    display:flex; gap:22px;
    list-style:none; margin:0; padding:0;
    font-family:'JetBrains Mono',monospace;
    font-size:13px;
  }
  .nav-links a{
    text-decoration:none;
    color:var(--muted);
    border-bottom:1px solid transparent;
    padding-bottom:2px;
    transition:color .15s, border-color .15s;
  }
  .nav-links a:hover, .nav-links a:focus-visible{
    color:var(--ink);
    border-color:var(--rust);
  }
  .nav-toggle{display:none;}

  /* ---------- hero ---------- */
  header.hero{
    padding:76px 0 40px;
  }
  .hero-eyebrow{
    font-size:13px;
    color:var(--muted);
    margin-bottom:14px;
  }
  .hero h1{
    font-size:clamp(42px, 8vw, 68px);
    line-height:1.02;
    letter-spacing:-0.01em;
  }
  .hero .role{
    font-family:'Fraunces',serif;
    font-style:italic;
    font-weight:400;
    font-size:clamp(18px,3vw,22px);
    color:var(--muted);
    margin-top:14px;
    max-width:34ch;
  }
  .trace{
    width:100%;
    height:64px;
    margin:34px 0 22px;
    display:block;
  }
  .trace path{
    fill:none;
    stroke-width:1.6;
    stroke-linecap:round;
    stroke-linejoin:round;
  }
  .trace-a{stroke:var(--green);}
  .trace-c{stroke:var(--blue);}
  .trace-g{stroke:var(--dark);}
  .trace-t{stroke:var(--rust);}
  .trace path{
    stroke-dasharray:900;
    stroke-dashoffset:900;
    animation:draw 1.7s cubic-bezier(.3,.8,.3,1) forwards;
  }
  .trace-c path{animation-delay:.08s;}
  .trace-g path{animation-delay:.16s;}
  .trace-t path{animation-delay:.24s;}
  @keyframes draw{to{stroke-dashoffset:0;}}

  .contact-line{
    font-family:'JetBrains Mono',monospace;
    font-size:13.5px;
    color:var(--muted);
    display:flex; flex-wrap:wrap; gap:6px 10px;
  }
  .contact-line span:not(:last-child)::after{
    content:"";
  }
  .contact-line a{text-decoration:none; border-bottom:1px solid var(--rule);}
  .contact-line a:hover{border-color:var(--rust); color:var(--rust);}

  /* ---------- sections ---------- */
  section{
    padding:56px 0;
    border-top:1px solid var(--rule);
  }
  .section-head{
    display:flex; align-items:baseline; justify-content:space-between;
    gap:16px;
    margin-bottom:30px;
  }
  .section-head h2{
    font-size:28px;
  }
  .section-num{
    font-family:'JetBrains Mono',monospace;
    font-size:13px;
    color:var(--muted);
  }

  .lede{
    max-width:62ch;
    color:var(--ink);
    font-size:17.5px;
  }

  /* ---------- timeline ---------- */
  .timeline{
    position:relative;
    padding-left:26px;
    border-left:1px solid var(--rule);
  }
  .entry{
    position:relative;
    padding-bottom:34px;
  }
  .entry:last-child{padding-bottom:0;}
  .entry::before{
    content:"";
    position:absolute;
    left:-31px; top:6px;
    width:9px; height:9px;
    border-radius:50%;
    background:var(--paper);
    border:2px solid var(--dark);
  }
  .entry-role{
    font-family:'Fraunces',serif;
    font-weight:500;
    font-size:19px;
    margin-bottom:3px;
  }
  .entry-org{
    font-style:italic;
    color:var(--muted);
    font-size:15.5px;
    margin-bottom:10px;
  }
  .entry ul{
    margin:0; padding-left:18px;
  }
  .entry li{
    margin-bottom:6px;
    font-size:15.5px;
  }
  .entry li::marker{color:var(--rust);}

  /* ---------- competencies ---------- */
  .comp-group{
    margin-bottom:28px;
  }
  .comp-group:last-child{margin-bottom:0;}
  .comp-label{
    font-family:'JetBrains Mono',monospace;
    font-size:13px;
    color:var(--muted);
    margin-bottom:10px;
  }
  .tag-row{
    display:flex; flex-wrap:wrap; gap:8px;
  }
  .tag{
    font-family:'JetBrains Mono',monospace;
    font-size:12.5px;
    padding:6px 10px;
    border-left:2px solid var(--dark);
    background:var(--paper-deep);
    white-space:nowrap;
  }
  .comp-group.bioinfo .tag{border-color:var(--green);}
  .comp-group.software .tag{border-color:var(--blue);}
  .comp-group.wetlab .tag{border-color:var(--rust);}
  .comp-group.other .tag{border-color:var(--dark);}

  /* ---------- talks ---------- */
  .talk{
    padding:18px 0;
    border-bottom:1px solid var(--rule);
    display:grid;
    grid-template-columns:1fr;
    gap:6px;
  }
  .talk:last-child{border-bottom:none;}
  .talk-title{
    font-family:'Fraunces',serif;
    font-size:17px;
    font-weight:500;
    line-height:1.35;
  }
  .talk-venue{
    font-family:'JetBrains Mono',monospace;
    font-size:12.5px;
    color:var(--muted);
  }

  /* ---------- two column ---------- */
  .split{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:40px;
  }
  @media (max-width:640px){
    .split{grid-template-columns:1fr;}
  }
  .block-label{
    font-family:'JetBrains Mono',monospace;
    font-size:13px;
    color:var(--muted);
    margin-bottom:14px;
  }
  .edu-item{margin-bottom:22px;}
  .edu-item:last-child{margin-bottom:0;}
  .edu-degree{
    font-family:'Fraunces',serif;
    font-weight:500;
    font-size:16.5px;
    margin-bottom:2px;
  }
  .edu-school{
    font-style:italic;
    color:var(--muted);
    font-size:14.5px;
    margin-bottom:6px;
  }
  .edu-item p{
    margin:0;
    font-size:14.5px;
    color:var(--ink);
  }
  ul.plain{margin:0; padding-left:18px;}
  ul.plain li{
    font-size:15px;
    margin-bottom:8px;
  }
  ul.plain li::marker{color:var(--rust);}

  /* ---------- footer ---------- */
  footer{
    padding:56px 0 72px;
    border-top:1px solid var(--rule);
  }
  footer h2{
    font-size:30px;
    margin-bottom:14px;
  }
  footer p{
    max-width:48ch;
    color:var(--muted);
    margin-bottom:22px;
  }
  .footer-contacts{
    display:flex; flex-wrap:wrap; gap:22px;
    font-family:'JetBrains Mono',monospace;
    font-size:14.5px;
  }
  .footer-contacts a{
    text-decoration:none;
    border-bottom:1px solid var(--rule);
  }
  .footer-contacts a:hover{border-color:var(--rust); color:var(--rust);}
  .foot-note{
    margin-top:40px;
    font-size:12.5px;
    color:var(--muted);
  }

  :focus-visible{
    outline:2px solid var(--rust);
    outline-offset:2px;
  }

  @media (max-width:560px){
    .nav-links{gap:14px; font-size:12px;}
    body{font-size:16px;}
  }
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <div class="nav-mark">j. torrejos</div>
    <ul class="nav-links">
      <li><a href="#about">about</a></li>
      <li><a href="#research">research</a></li>
      <li><a href="#skills">skills</a></li>
      <li><a href="#talks">talks</a></li>
      <li><a href="#contact">contact</a></li>
    </ul>
  </div>
</nav>

<header class="hero">
  <div class="wrap">
    <div class="hero-eyebrow mono">Quezon City, Metro Manila, Philippines</div>
    <h1>John H.<br>Torrejos</h1>
    <p class="role">Molecular biology &amp; bioinformatics researcher, working where wet-lab biology meets computation.</p>

    <svg class="trace" viewBox="0 0 700 64" preserveAspectRatio="none" aria-hidden="true">
      <path class="trace-a-p" d="M0,32 C20,10 40,54 60,32 C80,10 100,54 120,20 C140,4 155,44 175,32 C195,20 210,50 230,32" stroke="var(--green)" fill="none" stroke-width="1.6"/>
      <path class="trace-c-p" d="M0,40 C25,20 45,50 70,26 C95,6 115,46 140,30 C165,14 185,48 210,28 C230,12 245,44 260,32" stroke="var(--blue)" fill="none" stroke-width="1.6"/>
      <path class="trace-g-p" d="M0,26 C22,44 42,14 65,30 C88,46 108,18 130,34 C152,48 170,20 190,32 C210,42 225,24 240,30" stroke="var(--dark)" fill="none" stroke-width="1.6"/>
      <path class="trace-t-p" d="M0,34 C18,48 36,16 58,28 C80,40 100,18 122,32 C144,46 160,22 182,30 C202,38 216,26 230,30" stroke="var(--rust)" fill="none" stroke-width="1.6"/>
    </svg>

    <div class="contact-line">
      <span>jhtorrejos@up.edu.ph</span>
      <span>+63 916 481 7667</span>
      <span>Quezon City, PH</span>
    </div>
  </div>
</header>

<section id="about">
  <div class="wrap">
    <div class="section-head">
      <h2>About</h2>
      <span class="section-num mono">01</span>
    </div>
    <p class="lede">
      I work at the intersection of molecular biology, programming, and complex systems. My experience spans single-cell imaging and analysis of cancer cell lines, transcriptome analysis of cancer cell lines, insects, and plants using high-performance computing, and wet-lab molecular biology. I'm interested in studying cellular signaling mechanisms through high-throughput imaging and large-scale dataset analysis.
    </p>
  </div>
</section>

<section id="research">
  <div class="wrap">
    <div class="section-head">
      <h2>Research experience</h2>
      <span class="section-num mono">02</span>
    </div>

    <div class="timeline">

      <div class="entry">
        <div class="entry-role">Taiwan International Internship Program Intern</div>
        <div class="entry-org">Laboratory for Cell Dynamics, Institute of Molecular Biology, Academia Sinica</div>
        <ul>
          <li>Investigated the synergistic effect of nutlin-3a and the Wip1 inhibitor GSK 2830371 on p53-mediated cell death using single-cell imaging.</li>
        </ul>
      </div>

      <div class="entry">
        <div class="entry-role">Project Technical Specialist I</div>
        <div class="entry-org">Disease Molecular Biology and Epigenetics Laboratory, National Institute of Molecular Biology and Biotechnology, UP Diliman</div>
        <ul>
          <li>Ran cytotoxicity assays on hit compounds from the Tuklas Lunas drug discovery program.</li>
          <li>Applied Python, R, and Jupyter in a high-performance computing environment to identify differentially expressed genes implicated in cancer.</li>
          <li>Investigated the circPTK2–miR-92a–PTEN regulatory axis in A549 lung adenocarcinoma cells.</li>
          <li>Characterized the functional pseudogene INGX and its role in promoting cell cycle progression, survival, and migration in HCT116 colorectal cancer cells.</li>
        </ul>
      </div>

      <div class="entry">
        <div class="entry-role">Undergraduate Thesis Student</div>
        <div class="entry-org">Functional Genomics Laboratory, National Institute of Molecular Biology and Biotechnology, UP Diliman</div>
        <ul>
          <li>Thesis 1: Analyzed the transcriptome of the endoparasitoid <em>Comperiella calauanica</em> to profile chemosensory genes, using the Trinity, rnaSPAdes, and Trans-ABySS assemblers.</li>
          <li>Thesis 2: Conducted transcriptomic analysis of rice and the white stem borer in collaboration with the International Rice Research Institute (IRRI).</li>
        </ul>
      </div>

      <div class="entry">
        <div class="entry-role">PGC Bioinformatics Training and Internship Program</div>
        <div class="entry-org">Core Facility for Bioinformatics, Philippine Genome Center, UP Diliman</div>
        <ul>
          <li>Completed 240 hours of training in bioinformatics pipelines, including technical support for and development of the Integrated Sequence Local Alignment Pipeline for COVID-19 (ISLAP), a COVID-19 data management website.</li>
        </ul>
      </div>

      <div class="entry">
        <div class="entry-role">PGC Bioinformatics Virtual Immersion Program</div>
        <div class="entry-org">Core Facility for Bioinformatics, Philippine Genome Center, UP Diliman</div>
        <ul>
          <li>Trained in the full transcriptome analysis pipeline, from assembly through annotation, sponsored by the Functional Genomics Laboratory.</li>
        </ul>
      </div>

      <div class="entry">
        <div class="entry-role">Plant Tissue Culture Training</div>
        <div class="entry-org">Harbest Agribusiness Corporation, Pasig, Philippines</div>
        <ul>
          <li>Practiced micropropagation of orchids, aroids, and other ornamental plants under an industry-leading research laboratory.</li>
        </ul>
      </div>

      <div class="entry">
        <div class="entry-role">Aseptic Tissue Culture Training</div>
        <div class="entry-org">Philippine Horticultural Society Inc., Quezon City, Philippines</div>
        <ul>
          <li>Performed embryo rescue, meristem culture, and callus culture of orchids; induced mutations in orchid calli and fern spores to generate novel phenotypes.</li>
          <li>Aseptically cultured Drosera, Venus flytrap, and pitcher plant specimens.</li>
        </ul>
      </div>

      <div class="entry">
        <div class="entry-role">High School STEM Research</div>
        <div class="entry-org">Philippine Science High School, Central Visayas Campus, Argao, Cebu</div>
        <ul>
          <li>Primary research: soil properties of Cebu cinnamon (<em>Cinnamomum cebuense</em>) forest reserves in Tabunan and Nug-As, Cebu.</li>
          <li>Secondary research: diversity of mollusks in the intertidal habitat of Taloot, Argao, Cebu.</li>
        </ul>
      </div>

      <div class="entry">
        <div class="entry-role">Marine Science Summer Internship Program</div>
        <div class="entry-org">SEAFDEC Aquaculture Department, Tigbauan, Iloilo, Philippines</div>
        <ul>
          <li>Carried out identification, biodiversity assessment, and aquaculture work on fishes, mollusks, and crustaceans.</li>
        </ul>
      </div>

    </div>
  </div>
</section>

<section id="skills">
  <div class="wrap">
    <div class="section-head">
      <h2>Competencies</h2>
      <span class="section-num mono">03</span>
    </div>

    <div class="comp-group bioinfo">
      <div class="comp-label">bioinformatics</div>
      <div class="tag-row">
        <span class="tag">FastQ trimming</span>
        <span class="tag">Trinity</span>
        <span class="tag">Trans-ABySS</span>
        <span class="tag">rnaSPAdes</span>
        <span class="tag">BUSCO</span>
        <span class="tag">Bowtie2</span>
        <span class="tag">TransRate</span>
        <span class="tag">DESeq2</span>
        <span class="tag">DIAMOND</span>
        <span class="tag">Docker</span>
        <span class="tag">Linux / Bash</span>
      </div>
    </div>

    <div class="comp-group software">
      <div class="comp-label">software &amp; analysis</div>
      <div class="tag-row">
        <span class="tag">Python</span>
        <span class="tag">R</span>
        <span class="tag">Jupyter</span>
        <span class="tag">Perl</span>
        <span class="tag">GraphPad Prism</span>
        <span class="tag">ImageJ</span>
        <span class="tag">MATLAB</span>
        <span class="tag">Snakemake</span>
        <span class="tag">Git</span>
        <span class="tag">Benchling</span>
        <span class="tag">SnapGene Viewer</span>
        <span class="tag">Swiss-Model</span>
      </div>
    </div>

    <div class="comp-group wetlab">
      <div class="comp-label">wet lab</div>
      <div class="tag-row">
        <span class="tag">Single-cell / high-content imaging</span>
        <span class="tag">ddPCR &amp; PCR</span>
        <span class="tag">Gene cloning</span>
        <span class="tag">Site-directed mutagenesis</span>
        <span class="tag">Gel electrophoresis</span>
        <span class="tag">Bacterial transformation</span>
        <span class="tag">RNA extraction</span>
        <span class="tag">RT-qPCR</span>
        <span class="tag">SDS-PAGE / western blot</span>
        <span class="tag">Mammalian cell culture</span>
      </div>
    </div>

    <div class="comp-group other">
      <div class="comp-label">web &amp; graphics</div>
      <div class="tag-row">
        <span class="tag">ReactJS</span>
        <span class="tag">MongoDB</span>
        <span class="tag">API development</span>
        <span class="tag">Metabase</span>
        <span class="tag">BioRender</span>
        <span class="tag">Canva</span>
      </div>
    </div>
  </div>
</section>

<section id="talks">
  <div class="wrap">
    <div class="section-head">
      <h2>Conference presentations</h2>
      <span class="section-num mono">04</span>
    </div>

    <div class="talk">
      <div class="talk-title">Probing into the synergistic effect of nutlin-3a and Wip1 inhibitor (GSK 2830371) on p53-mediated cell death using single-cell imaging</div>
      <div class="talk-venue">Taiwan International Internship Program — Oral &amp; Poster Presentation</div>
    </div>

    <div class="talk">
      <div class="talk-title">The regulator is regulated: probing the circPTK2–miR-92a–PTEN regulatory axis in lung adenocarcinoma cells</div>
      <div class="talk-venue">Philippine Society for Cell Biology, 7th International &amp; 15th Annual Meeting, Manila — Poster Presentation</div>
    </div>

    <div class="talk">
      <div class="talk-title">Profiling the transcriptomes of the white stem borer infesting resistant and susceptible rice varieties</div>
      <div class="talk-venue">55th Pest Management Council of the Philippines Anniversary — Poster Presentation</div>
    </div>

    <div class="talk">
      <div class="talk-title">Identification of putative chemosensory genes from the transcriptomes of Comperiella calauanica</div>
      <div class="talk-venue">54th Pest Management Council of the Philippines Anniversary — Oral Paper Presentation</div>
    </div>
  </div>
</section>

<section id="education">
  <div class="wrap">
    <div class="section-head">
      <h2>Education &amp; awards</h2>
      <span class="section-num mono">05</span>
    </div>

    <div class="split">
      <div>
        <div class="block-label">education</div>
        <div class="edu-item">
          <div class="edu-degree">B.S. Molecular Biology and Biotechnology</div>
          <div class="edu-school">University of the Philippines Diliman</div>
          <p>Magna cum laude — cumulative GWA of 1.29</p>
        </div>
        <div class="edu-item">
          <div class="edu-degree">Science, Technology &amp; Mathematics Strand</div>
          <div class="edu-school">Philippine Science High School — Central Visayas Campus</div>
          <p>Graduated with High Honors, GWA 1.25; Proficiency Award for Biology</p>
        </div>
      </div>

      <div>
        <div class="block-label">awards &amp; distinctions</div>
        <ul class="plain">
          <li>Magna cum laude, cumulative GWA of 1.29</li>
          <li>Consistent University/College Scholar, 2019–2023</li>
          <li>Department of Science and Technology (DOST) Merit Scholar, 2019–2023</li>
          <li>Proficiency Award for Biology</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<footer id="contact">
  <div class="wrap">
    <h2>Get in touch</h2>
    <p>Open to conversations on cellular signaling, high-throughput imaging, and large-scale dataset analysis. Academic references available on request.</p>
    <div class="footer-contacts">
      <a href="mailto:jhtorrejos@up.edu.ph">jhtorrejos@up.edu.ph</a>
      <a href="tel:+639164817667">+63 916 481 7667</a>
      <span>Quezon City, Metro Manila, Philippines</span>
    </div>
    <div class="foot-note mono">John H. Torrejos — updated 2026</div>
  </div>
</footer>

</body>
</html>
