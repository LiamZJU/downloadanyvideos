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

DownloadAny 由基于 [imput](https://imput.net/) 用爱与关怀打造的 Cobalt 上二次开发而发布的 ❤️

</section>

<section id="licenses">
<SectionHeading
    title={$t("about.heading.licenses")}
    sectionId="licenses"
/>

DownloadAny api（处理服务器）代码是开源的，遵循 AGPL-3.0 许可。

DownloadAny 前端代码为 [source first](https://sourcefirst.com/)，遵循 CC-BY-NC-SA 4.0 许可。

</section>
