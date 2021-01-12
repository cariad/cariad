# Cariad Eccleston 👩🏼‍💻 🏳️‍🌈 😷

Hey! I’m **Cariad**, pronounced "carry-add". I’m a **freelance DevOps engineer**, and I **work remotely** from the seaside in Exmouth, UK.

- 👩🏼‍💻 All about that **Python** and **Amazon Web Services**.
- 🧪 It ain’t done until it’s **tested**.
- 🏳️‍🌈 **Transgender**. Pronouns are **she/her**.
- 🤔 Working on my **presentation confidence** and **books**.
- 💬 Ask me about **any of my projects** and **contracting availability**.
- ✉️ **[@cariadeccleston](https://twitter.com/cariadeccleston)** • **[cariad@hey.com](mailto:cariad@hey.com)**

## My values 💕

- 👩‍🏫 **Support your team to succeed without you.** Share your knowledge. Be a teacher, not a hoarder.
- 💥 **Fail early, fail often.** If you’re not failing, you’re not experimenting. If you're not experimenting, you're not innovating. If you're not innovating, the startup across the street will eat your lunch.
- ✌️ **Chill.** Empower folks to fix their own mistakes. Contribute without shaming. We all fuck up.
- ❤️ **Empathise.** The language we use with our colleagues is more important than the language we use in Visual Studio Code. Zero tolerance for bigotry.

## Recent contracts 🙋‍♀️

- 2020-2021: **[Freyda](https://freyda.io)**
    - Architect cloud infrastructure in **Amazon Web Services**.
    - Build and deploy infrastructure-as-code with **Python**.
    - Build and take care of the **CI/CD pipeline**.
    - Think about **encryption**, **serverless**, **scaling**, **monitoring**, **resilience** and **recovery**. _Y’know, the fun stuff!_
- 2020: **NHS Digital**, building .NET SOAP services and automated tests.
- 2005-2019: Full-time software developer and DevOps team lead at **Thomson Reuters**.

## Recent projects 🎉

### sitestack.cloud 🌍

With (almost) one-click, [sitestack.cloud](https://sitestack.cloud) deploys all the infrastructure you need to host a static website in your own Amazon Web Services account.

Just drag-and-drop your site into the S3 bucket we deploy, and it’s live behind **HTTPS**, a **global CDN** and **beautiful URLs**; no `index.html` on the end.

Perfect for Hugo, Jekyll and other static site generators!

### cariad/hugo-ci ⛴

[cariad/hugo-ci](https://github.com/cariad/hugo-ci) is a Docker image for building and testing (and optionally deploying) Hugo sites.

Use it in your local development directory to build your Hugo site and verify that your **HTML is well-formed**, **valid** and all your **images have `alt` attributes** before you go live:

```bash
docker run --mount "type=bind,source=$(pwd),target=/workspace" --rm cariad/hugo-ci
```

### hugo-ci-action ⚙️

[hugo-ci-action](https://github.com/marketplace/actions/build-validate-and-deploy-a-hugo-site) is a GitHub Action for building and testing (and optionally deploying) Hugo sites.

Build and test your Hugo site with just one line:

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: cariad/hugo-ci-action@v1
```

To deploy after testing, set AWS credentials in your workflow's environment variables then add `with/s3-bucket`:

```yaml
env:
  AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
  AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: cariad/hugo-ci-action@v1
        with:
          s3-bucket: mybucket
```

### s3headersetter 🎁

[s3headersetter](https://github.com/cariad/s3headersetter) is a cross-platform CLI tool for setting HTTP headers on Amazon Web Services S3 objects.

Simply create a configuration file to describe the headers and objects to match:

```yaml
rules:
  - header:        Cache-Control
    when:
      - extension: .html
        then:      max-age=3600, public
      - extension: .css
        then:      max-age=604800, public
    else:          max-age=31536000, public

  - header:        Content-Type
    when:
      - extension: .woff2
        then:      font/woff2
```

…then run `s3headersetter` to connect and update your objects:

```bash
s3headersetter -config config.yml -bucket my-website-bucket
```

### py-tupper ∞

A Python package for plotting [Tupper's Self-Referential Formula](https://cariad.io/tupper/).

Just install and run to see something cool:

```bash
pip3 install tupper
python3 -m tupper
```

```text
        █                   █                █ ██ █     █                █  █ █     █    █ ██ █      █   █
        █                   █ █      █       █  █ █     █                █  █ █     █    █  █ █      █   █
██      █                  █  █      █    ██ █  █ █ █ █ █ ██ ████  ███ ███ █  █ █ █ █    █  █  █      █  █
 █      █                  █  █  █ █ █       █ █  █  █  █    █ █ █ █ █ █ █ █  █ █ █ █    █ █   █      █  █
 █      █                  █  █  █ █ █       █ █  █ █ █ █    █ █ █ ███ ███ █  █  █  █    █ █   █      █  █
 █      █               █ █   █   █  █  ██        █     █                  █  █ █   █  █       █   ██  █ █
███   █ █               █ █   █  █   █ █  █       █     █                   █ █     █  █      █   █  █ █ █
     █  █ ██ █   ██   ███ █   █      █   █        ███ ███                   █ ███ ███ █       █     █  █ █
███ █   █ █ █ █ █  █ █  █ █   █ ████ █  █                                                          █   █ █
     █  █ █ █ █ █  █ █  █ █   █      █ █                                                          █    █ █
██    █ █ █ █ █  ██   ███ █   █ █ ██ █ ████                                                       ████ █ █
  █     █                 █   █ █  █ █                                                          █      █ █
 █      █                  █  █ █  █ █                                                          █     █  █
█       █                  █  █ █ █  █                                                         █      █  █
███     █                  █  █ █ █  █                                                                █  █
        █                   █ █      █                                                               █   █
        ███                 █ ███  ███                                                               █ ███
```

## Availability

I’m currently in a very happy contract, but I’d love to chat about any exciting projects you have coming up later in 2021.

- ✉️ [cariad@hey.com](mailto:cariad@hey.com)
- 🐦 [@cariadeccleston](https://twitter.com/cariadeccleston)
