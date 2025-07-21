<script lang="ts">
    import { t } from "$lib/i18n/translations";
    import { contacts, docs } from "$lib/env";

    import SectionHeading from "$components/misc/SectionHeading.svelte";
</script>

<section id="summary">
<SectionHeading
    title={$t("about.heading.summary")}
    sectionId="summary"
/>

DownloadAny 帮助你从你喜欢的网站保存任何内容：视频、音频、照片或 gif。只需粘贴链接，即可轻松下载！

没有广告、追踪、付费墙或其他干扰。只是一款随时随地都能用的便捷 Web 应用。
</section>

<section id="motivation">
<SectionHeading
    title={$t("about.heading.motivation")}
    sectionId="motivation"
/>

DownloadAny 的诞生是为了公众利益，保护用户免受其他下载器推送的广告和恶意软件的侵害。
我们相信，最好的软件应该是安全、开放且易用的。所有 imput 项目都遵循这些基本原则。
</section>

<section id="privacy-efficiency">
<SectionHeading
    title={$t("about.heading.privacy_efficiency")}
    sectionId="privacy-efficiency"
/>

所有到后端的请求都是匿名的，所有关于文件隧道的信息都经过加密。
我们严格执行零日志政策，不会存储或追踪任何个人相关的信息。

如果请求需要额外处理，比如封装修复或转码，DownloadAny 会直接在你的设备上处理媒体文件，
以确保最高的效率和隐私。

如果你的设备不支持本地处理，则会使用基于服务器的实时处理。
在这种情况下，处理后的媒体会直接流式传输到客户端，绝不会存储在服务器磁盘上。

你可以[启用强制隧道](/settings/privacy#tunnel)以进一步提升隐私。
启用后，DownloadAny 会对所有下载的文件进行隧道处理，而不仅仅是需要的文件。
没有人会知道你从哪里下载了什么，甚至你的网络服务商也不会知道。
他们只会看到你在使用 DownloadAny 实例。
</section>
