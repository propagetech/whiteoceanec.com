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
    "path": "White-Paper.html",
    "context": {
      "title": "White Papers | White Papers",
      "first_heading": "The Emergence of the Customer Success function within SaaS companies"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
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
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/a9e8199f16808a35e5f3e34c5bbd6f10.css",
    "context": {
      "path": "css/a9e8199f16808a35e5f3e34c5bbd6f10.css"
    }
  },
  {
    "path": "css/ffdc705a4f552d469d51f3b98a5752db.css",
    "context": {
      "path": "css/ffdc705a4f552d469d51f3b98a5752db.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/199171441ab54a9dbe4bde25bf64bd62.webp",
    "context": {
      "refs": [
        {
          "alt": "White Papers/Case Studies",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/321b1ec90761b4963b855c131188bc9f.webp",
    "context": {
      "refs": [
        {
          "alt": "Ownership of the Account",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/58d2ca438df5eb31b53a4e69743ff08d.webp",
    "context": {
      "refs": [
        {
          "alt": "Consulting",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5cbb2965da7082ff7cafae281cd9c808.webp",
    "context": {
      "refs": [
        {
          "alt": "White Ocean Expert Consulting",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5cf2f3c4fbc505c31ffff6f06dd57c1b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6f7c508f434d469c6c85a99f521a963d.webp",
    "context": {
      "refs": [
        {
          "alt": "Emerging Leaders",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/80d499882e4e2e081b24d51b4f0e7ba2.webp",
    "context": {
      "refs": [
        {
          "alt": "Global Research",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/88f8ccb22ec8f52bd9bb2d261004ea2f.webp",
    "context": {
      "refs": [
        {
          "alt": "The #1 Opportunity Most American Companies are Missing",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a92336ba66efb826de55d1fb68c1e06a.webp",
    "context": {
      "refs": [
        {
          "alt": "Satya Prakash",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b2927ab8a295b7f8e0a4f90934964e94.webp",
    "context": {
      "refs": [
        {
          "alt": "World Wide Access",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b8871ecbe925600248465d81aa58f299.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/be6f5fd25740cfad088cc21f85a5fcf3.webp",
    "context": {
      "refs": [
        {
          "alt": "Executive Search",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c3869cca1770a8fa16bec75feb3e9fb7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cc62122593371d3bb50e9da617e0c9f0.webp",
    "context": {
      "refs": [
        {
          "alt": "The Emergence of the Customer Success function within SaaS companies",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d1e4850d2eea31ea079aac5e6c86ca7b.webp",
    "context": {
      "refs": [
        {
          "alt": "Independent Experts\u00a0Panel",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d2345ee89b60b653e10098806e6ac14e.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d3ba33abf0ab3ccf989c70824f25a904.webp",
    "context": {
      "refs": [
        {
          "alt": "Thought Leadership",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dfdce8101c0c41d6cd6fc1e20361cec8.webp",
    "context": {
      "refs": [
        {
          "alt": "The Playbook for recruiting Rockstars",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e1632b6c247da79cdb7640de5075e0ed.webp",
    "context": {
      "refs": [
        {
          "alt": "Back to Bharat",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Home | White Ocean | Expert Consulting",
      "first_heading": "WHITE OCEAN EXPERT CONSULTING"
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
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "thought-leadership.html",
    "context": {
      "title": "Thought Leadership | White Ocean",
      "first_heading": "The #1 Opportunity Most American Companies are Missing"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.