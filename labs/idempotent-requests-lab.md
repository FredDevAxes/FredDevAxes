# Idempotent requests

**v0.2.0 · Local prototype**

A technician sends an intervention request and loses the connection before the reply arrives. Did the server save it? The lab lets you repeat the send and compare what the browser knows with what the database contains.

<p><img src="../assets/labs/idempotent-requests-lab/guided-repeat-desktop-f98e968e6a2d.png" alt="Guided lab: two sends return one saved request, with separate client and server observations." width="900"></p>

## The experiment

The interface walks through repeated sends, a lost reply, concurrent requests and failures before saving. The API keeps the same request key between attempts. While that key is retained, retries with the same content return the saved result.

This is a local prototype using fictional maintenance requests. The guarantee covers the database operation, not payments, emails or other external effects. The repository contains the setup instructions, demo protocol and tests.

## Stack

NestJS · PostgreSQL · React · TypeScript

<p><a href="https://github.com/FredDevAxes/idempotent-requests-lab"><img src="../assets/ui/button-repository-913347d886e7.svg" alt="Open repository" width="210" height="44"></a></p>

---

<p><a href="README.md"><img src="../assets/ui/button-labs-185152e591d1.svg" alt="All labs" width="136" height="44"></a></p>
