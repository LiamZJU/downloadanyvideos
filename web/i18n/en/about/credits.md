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

DownloadAny is released as a secondary development based on Cobalt, which was made with love and care by [imput](https://imput.net/) ❤️

</section>

<section id="licenses">
<SectionHeading
    title={$t("about.heading.licenses")}
    sectionId="licenses"
/>

DownloadAny api (processing server) code is open source and licensed under AGPL-3.0.

DownloadAny frontend code is [source first](https://sourcefirst.com/) and is licensed under CC-BY-NC-SA 4.0.

</section>
