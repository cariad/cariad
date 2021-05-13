# Cariad Eccleston 👩🏼‍💻 🏳️‍🌈 😷

Hey! I’m **Cariad**, pronounced "carry-add". I’m a **freelance DevOps engineer**, and I **work remotely** from the seaside in Exmouth, UK.

- 👩🏼‍💻 All about that **Python** and **Amazon Web Services**.
- 🏳️‍🌈 **Transgender**. Pronouns are **she/her**.
- 🤔 Working on my **presentation confidence** and **books**.
- 💬 Ask me about **any of my projects** and **contracting availability**!
- ✉️ **[cariad.io](https://cariad.io)** • **[cariad@cariad.io](mailto:cariad@cariad.io)**

## Recent contracts 🙋‍♀️

- 2020-2021: **[Freyda](https://freyda.io)**
    - Architecting cloud infrastructure in **Amazon Web Services**.
    - Building and deploying infrastructure-as-code with **Python**.
    - Building and taking care of the **CI/CD pipeline**.
    - Thinking about **encryption**, **serverless**, **scaling**, **monitoring**, **resilience** and **recovery**. _Y’know, the fun stuff!_
- 2020: **NHS Digital**, building .NET SOAP services and automated tests.
- 2005-2019: Full-time software developer and DevOps team lead at **Thomson Reuters**.

## Recent projects 🎉

### wev: with environment variables ⚙️

[cariad/wev](https://github.com/cariad/wev) is a cross-platform command-line tool for running commands _with environment variables_.

For example:

- `wev` can [create a multi-factor authenticated Amazon Web Services session](https://wevcli.app/examples/aws-mfa-on-command-line).
- `wev` can [set Amazon Web Services named profiles per-project](https://wevcli.app/examples/aws-profile-per-project).
- `wev` can [request an Amazon Web Services CodeArtifact authorisation token on behalf of pipenv](https://wevcli.app/examples/aws-codeartifact).

### sitestack.cloud 🌍

With (almost) one-click, [sitestack.cloud](https://sitestack.cloud) deploys all the infrastructure you need to host a static website in your own Amazon Web Services account.

Just drag-and-drop your site into the S3 bucket we deploy, and it’s live behind **HTTPS**, a **global CDN** and **beautiful URLs**; no `index.html` on the end.

Perfect for Hugo, Jekyll and other static site generators!

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
