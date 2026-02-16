You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "blog.html",
    "context": {
      "title": "",
      "first_heading": "BLOG"
    }
  },
  {
    "path": "blog_delta-lake-architecture--simplifying-data-engineering---analytics-needs.html",
    "context": {
      "title": "Delta Lake Architecture: Simplifying Data Engineering & Analytics Needs",
      "first_heading": "Delta Lake Architecture: Simplifying Data Engineering & Analytics Needs"
    }
  },
  {
    "path": "blog_modernize-your-etl-processes-to-unleash-better-business-intelligence.html",
    "context": {
      "title": "Modernize Your ETL Processes To Unleash Better Business Intelligence",
      "first_heading": "Modernize Your ETL Processes To Unleash Better Business Intelligence"
    }
  },
  {
    "path": "blog_snowflake-vs-azure-synapse-analytics--the-battle-of-cloud-data-warehouses.html",
    "context": {
      "title": "Snowflake Vs Azure Synapse Analytics: The Battle of Cloud Data Warehouses",
      "first_heading": "Snowflake Vs Azure Synapse Analytics: The Battle of Cloud Data Warehouses"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/87b794ec556b63cc51afb001d70fc32a.css",
    "context": {
      "path": "css/87b794ec556b63cc51afb001d70fc32a.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/0662588f35796cafae9de4b9d45d5f66.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/081ed4ee76b1ab02e13798d3a0b9b6b1.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/086ebbe92f72022c4afc59aad043dfc3.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/0e816e4a7ec4a2fd76c751675e605d1e.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/1939407028ddfd3323b8caff5cd356b4.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/1a4d12e572bb5bcc0ca67f26783807bb.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/1cfd1ea2b0512b69e1be7fc81a34c9b6.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/428ff08473658518df27734b3ff9dbcb.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/4624dfb91599a4888150b0779466da71.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/5496d2d71072faa2a8b8170b090b54eb.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/56f8f71a7b4a2f780cbac96ad924f5b0.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/5b480ad4a9480197f2fcfa373bfda31c.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/616d0ab9110c399c62ac40fc511d240b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/61708b64b609aa69dfd56c6b142d3f16.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6b5e0519f275a12f75ce10f658b40c50.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/8c6c0003860173d9f5d367f09d13cdce.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/8eaa0515f704117f4b957160ae5ae474.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/975b5ed50141c59b88b07859560d9d87.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/97ac8ae5422276ff368f44ced68c8811.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/98fe94b223f2ea145abbd115ddb49d88.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/9fd8819c36dcce239cb6d8afd774cb4b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/a1d4754c88b792a93a17c5a336381e1a.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/a8214cd7bfa50939fa38a96af55cb903.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/a861ef6fd2ed2f922050e8c1f905c3e2.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/aed8f2bfe48571bd08f5720d48ed712d.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b14dc4e1f62a835800d1e376cc57269d.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b4ab02ca35ffc194c6b44151fc6dcfb4.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/bf24313416505b3afc839e36db5f63ca.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c2e8d2f659492347f98b23605f3dd019.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/cca4ad38a33aa59e5d5d153b040628fc.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/ccb4083622fad519326702073ea6e47a.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/d43c80086f1208710fe6ad1052edebfe.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/da93178670edd0044727e0173ed21823.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/e55563b7260a07619c07f342b476c8f5.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/eaaf03e9e7bbf7af7a17ef9c79510ac6.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/eef02da51d374759409e2ec7d1da538e.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/fec8b4f25803ee026494e37db1b009d0.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Bluegazelle Innovators",
      "first_heading": "We\u2019ll accelerate your journey from data to decisions"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.