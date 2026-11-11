const I18N = {
  zh: {
    "nav.about": "关于",
    "nav.products": "产品矩阵",
    "nav.scenes": "应用场景",
    "nav.credentials": "资质认证",
    "nav.contact": "联系",

    "hero.title": "让脑健康<br><em>可测量</em>，也可管理。",
    "hero.lead": "心源科技聚焦生命科学与人工智能的融合，以非植入式脑机接口为入口，通过实时脑波监测与 AI 分析，为焦虑、失眠等问题提供个性化评估与干预，构建脑健康全周期管理服务。",
    "hero.v.base": "深圳 · 中国",
    "hero.v.focus": "BCI × AI 脑健康",
    "hero.v.model": "技术 · 产品 · 场景 · 数据",

    "about.title": "关于<em>心源</em>",

    "p1.tag": "检测硬件 · C 端",
    "p1.name": "FlowSense 智能睡眠头带",
    "p1.desc": "面向个人的睡眠与脑健康入口，在自然入睡状态下完成脑电采集，并以脑-声闭环实现助眠干预。",
    "p1.s1k": "核心功能", "p1.s1v": "EEG 实时监测 · SOI 指数",
    "p1.s2k": "干预方式", "p1.s2v": "脑-声闭环助眠",
    "p1.s3k": "配套",     "p1.s3v": "14 天训练计划",
    "p1.s4k": "建议零售价","p1.s4v": "¥1,999",
    "p1.more": "产品详情 →",
    "p1.alt": "FlowSense 智能睡眠头带",

    "credentials.title": "知识产权与<em>全球准入</em>",

    "contact.email.k": "Email",
    "contact.tel.k": "Tel"
  },

  en: {
    "nav.about": "About",
    "nav.products": "Products",
    "nav.scenes": "Applications",
    "nav.credentials": "Credentials",
    "nav.contact": "Contact",

    "hero.title": "Brain health,<br><em>measured</em> and managed.",
    "hero.lead": "Xinyuan Neurotech sits at the intersection of life science and artificial intelligence. Starting from non-invasive brain–computer interfaces, we combine real-time EEG monitoring with AI analysis to deliver personalised assessment and intervention for anxiety, insomnia and beyond — a full-cycle brain health service.",
    "hero.v.base": "Shenzhen · China",
    "hero.v.focus": "BCI × AI Brain Health",
    "hero.v.model": "Technology · Product · Scenario · Data",

    "about.title": "About <em>Xinyuan</em>",

    "p1.tag": "Sensing · Consumer",
    "p1.name": "FlowSense Smart Sleep Headband",
    "p1.desc": "A personal entry point into sleep and brain health — EEG is captured naturally during sleep, and a closed-loop brain–sound intervention helps users fall asleep.",
    "p1.s1k": "Core", "p1.s1v": "Real-time EEG · SOI index",
    "p1.s2k": "Intervention", "p1.s2v": "Closed-loop brain–sound",
    "p1.s3k": "Programme", "p1.s3v": "14-day training plan",
    "p1.s4k": "MSRP", "p1.s4v": "RMB 1,999",
    "p1.more": "Details →",
    "p1.alt": "FlowSense smart sleep headband",

    "credentials.title": "IP and <em>global access</em>",

    "contact.email.k": "Email",
    "contact.tel.k": "Tel"
  }
};

function setLang(lang){
  const dict = I18N[lang];
  if(!dict) return;

  document.documentElement.lang = lang === "zh" ? "zh-CN" : "en";
  document.documentElement.classList.toggle("lang-en", lang === "en");

  document.querySelectorAll("[data-i18n]").forEach(el => {
    const v = dict[el.dataset.i18n];
    if(v !== undefined) el.textContent = v;
  });

  document.querySelectorAll("[data-i18n-html]").forEach(el => {
    const v = dict[el.dataset.i18nHtml];
    if(v !== undefined) el.innerHTML = v;
  });

  document.querySelectorAll("[data-i18n-alt]").forEach(el => {
    const v = dict[el.dataset.i18nAlt];
    if(v !== undefined) el.alt = v;
  });

  localStorage.setItem("lang", lang);
  document.getElementById("langToggle")
    .setAttribute("aria-label", lang === "zh" ? "Switch to English" : "切换到中文");
}

document.addEventListener("DOMContentLoaded", () => {
  setLang(localStorage.getItem("lang") || "zh");
  document.getElementById("langToggle").addEventListener("click", () => {
    setLang(document.documentElement.classList.contains("lang-en") ? "zh" : "en");
  });
});
