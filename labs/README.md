# DevAxes Labs

Small projects where I explore a specific technical question. Each lab has its own public repository.

## Idempotent requests

<p><img src="../assets/labs/idempotent-requests-lab/lost-reply-e68d42e13b38.png" alt="Lost reply in v0.3.1: the client is unconfirmed while the server has saved one request; technical details are collapsed." width="900"></p>

**v0.3.1 · Local prototype**

A request is saved, but its response is lost. This lab shows how a retry can recover it without creating a second request.

`NestJS` `PostgreSQL` `React` `TypeScript`

Six guided scenarios compare what the client knows with what PostgreSQL saved: repeated sends, a lost reply, twenty concurrent attempts, a failure before saving, changed content under the same reference, and a separate request. Expand Technical details to inspect real HTTP attempts, saved records and request keys.

The client keeps the same key and content across retries and reloads. While the key is retained, the API returns the recorded result; after explicit purge, reusing it can create another request. This local prototype uses fictional maintenance data. Its guarantee covers the database transaction, with no payments, emails or other external effects.

<p><img src="../assets/labs/idempotent-requests-lab/recovered-reply-88ba24960bba.png" alt="Retry in v0.3.1 recovers the confirmation: two sends, one saved request and no duplicate." width="900"></p>

Retrying the same request recovers its confirmation: two sends, one saved request.

[Visual tour and recording](https://github.com/FredDevAxes/idempotent-requests-lab/blob/main/docs/visual-tour.md) · [Demo protocol](https://github.com/FredDevAxes/idempotent-requests-lab/blob/main/docs/demo.md) · [API contract](https://github.com/FredDevAxes/idempotent-requests-lab/blob/main/docs/contract.md)

<p><a href="https://github.com/FredDevAxes/idempotent-requests-lab"><img src="../assets/ui/button-repository-913347d886e7.svg" alt="Open Idempotent requests repository" width="210" height="44"></a></p>


---

## Mobile stack benchmark

<p><img src="../assets/labs/mobile-stack-benchmark/catalogue-6c5e0d63a8a0.png" alt="SwiftUI catalogue used in the mobile lab, showing fictional hiking equipment." width="180"></p>

**In progress**

The same catalogue in Flutter, React Native, Jetpack Compose and SwiftUI, with and without an animated transition.

`Flutter` `React Native` `Kotlin / Compose` `Swift / SwiftUI`

<p><a href="https://github.com/FredDevAxes/mobile-stack-benchmark"><img src="../assets/ui/button-repository-913347d886e7.svg" alt="Open Mobile stack benchmark repository" width="210" height="44"></a></p>

---

<p><a href="../README.md"><img src="../assets/ui/button-profile-41db3f0638fc.svg" alt="Back to profile" width="196" height="44"></a></p>

<p align="center"><a href="../projets/README.md">All mobile projects</a></p>
