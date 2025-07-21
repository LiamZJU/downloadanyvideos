<script lang="ts">
    import { t } from "$lib/i18n/translations";
    import SectionHeading from "$components/misc/SectionHeading.svelte";
</script>

<section id="general">
<SectionHeading
    title={$t("about.heading.general")}
    sectionId="general"
/>

这些条款仅适用于官方 DownloadAny 实例。
在其他情况下，你可能需要联系实例托管者以获取准确信息。
</section>

<section id="saving">
<SectionHeading
    title={$t("about.heading.saving")}
    sectionId="saving"
/>

保存功能简化了从互联网下载内容的流程，
我们对保存内容的用途不承担任何责任。

处理服务器的工作方式类似高级代理，绝不会将任何请求内容写入磁盘。
所有操作都在内存中完成，隧道结束后会被永久清除。
我们没有下载日志，也无法识别任何用户。

你可以在[隐私政策](/about/privacy)中了解隧道的工作原理。
</section>

<section id="responsibility">
<SectionHeading
    title={$t("about.heading.responsibility")}
    sectionId="responsibility"
/>

你（终端用户）对使用我们的工具、如何使用和分发所得内容负全部责任。
请在使用他人内容时保持谨慎，并始终注明原作者。
确保不违反任何条款或许可。

用于教育目的时，请务必注明来源并标注原作者。

合理使用和署名对所有人都有益处。
</section>

<section id="abuse">
<SectionHeading
    title={$t("about.heading.abuse")}
    sectionId="abuse"
/>

由于 DownloadAny 完全匿名，我们无法自动检测滥用行为。
如遇到其他问题，可通过[社区页面](/about/community)上的任意方式联系我们获取支持。
</section>
