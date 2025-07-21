<script lang="ts">
    import { contacts, docs, partners } from "$lib/env";
    import { t } from "$lib/i18n/translations";

    import SectionHeading from "$components/misc/SectionHeading.svelte";
    import BetaTesters from "$components/misc/BetaTesters.svelte";
</script>

<section id="imput">
<SectionHeading
    title="imput"
    sectionId="imput"
/>

DownloadAny выпущен как форк (вторичная разработка) на основе Cobalt, который был создан с любовью и заботой командой [imput](https://imput.net/) ❤️

</section>

<section id="licenses">
<SectionHeading
    title={$t("about.heading.licenses")}
    sectionId="licenses"
/>

Код DownloadAny api (сервер обработки) — open source и распространяется по лицензии AGPL-3.0.

Код фронтенда DownloadAny — [source first](https://sourcefirst.com/) и распространяется по лицензии CC-BY-NC-SA 4.0.
