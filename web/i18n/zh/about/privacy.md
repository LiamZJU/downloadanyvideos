<script lang="ts">
    import env from "$lib/env";
    import { t } from "$lib/i18n/translations";

    import SectionHeading from "$components/misc/SectionHeading.svelte";
</script>

<section id="general">
<SectionHeading
    title={$t("about.heading.general")}
    sectionId="general"
/>

DownloadAny 的隐私政策很简单：我们不会收集或存储你的任何信息。
你在这里做什么，只属于你自己，与我们或任何其他人无关。

这些条款仅适用于官方 DownloadAny 实例。
在其他情况下，你可能需要联系实例托管者以获取准确信息。
</section>

<section id="local">
<SectionHeading
    title={$t("about.heading.local")}
    sectionId="local"
/>

使用本地处理的工具会在离线、本地环境下运行，
绝不会将任何处理数据发送到其他地方。
只要适用，都会明确标注为本地处理。
</section>

<section id="saving">
<SectionHeading
    title={$t("about.heading.saving")}
    sectionId="saving"
/>

使用保存功能时，DownloadAny 可能需要代理、封装修复或转码文件。
如遇此情况，会为此目的创建一个临时隧道，
并为媒体存储最少量的必要信息，保留 90 秒。

在未经修改的官方 DownloadAny 实例上，
**所有隧道数据都用只有终端用户才能访问的密钥加密**。

加密的隧道数据可能包括：
- 来源服务名称
- 媒体文件的原始 URL
- 区分处理类型所需的内部参数
- 最小化的文件元数据（生成的文件名、标题、作者、创作年份、版权信息）
- 关于原始请求的最少信息（用于隧道过程中 URL 失效时的处理）

这些数据会在 90 秒后从服务器内存中彻底清除。
即使是实例拥有者，也无法访问缓存的隧道数据，
只要 DownloadAny 源码未被修改。

隧道中的媒体数据绝不会被存储或缓存。
所有处理都是实时进行的，即使是封装修复和转码也是如此。
DownloadAny 隧道就像一个匿名代理。

如果你的设备支持本地处理，
则加密隧道信息会更少，因为数据会直接返回给客户端。

你可以[在 github 查看相关源码](https://github.com/LiamZJU/downloadanyvideos)
了解其工作原理。
</section>

<section id="encryption">
<SectionHeading
    title={$t("about.heading.encryption")}
    sectionId="encryption"
/>

临时存储的隧道数据采用 AES-256 标准加密。
解密密钥只包含在访问链接中，绝不会被记录、缓存或存储。
只有终端用户才能访问链接和加密密钥。
每个请求的隧道都会生成唯一密钥。
</section>

{#if env.PLAUSIBLE_ENABLED}
<section id="plausible">
<SectionHeading
    title={$t("about.heading.plausible")}
    sectionId="plausible"
/>

我们使用 [plausible](https://plausible.io/) 以完全匿名的方式
统计大致的 DownloadAny 活跃用户数。不会存储任何可识别你或你请求的信息。
所有数据都经过匿名化和聚合处理。
我们自建并管理 DownloadAny 使用的 [plausible 实例](https://{env.PLAUSIBLE_HOST}/)。

plausible 不使用 cookie，完全符合 GDPR、CCPA 和 PECR。

如果你希望不参与匿名分析，可以在[隐私设置](/settings/privacy#analytics)中关闭。
关闭后，plausible 脚本将不会被加载。

[了解 plausible 对隐私的承诺](https://plausible.io/privacy-focused-web-analytics)。
</section>
{/if}

<section id="cloudflare">
<SectionHeading
    title={$t("about.heading.cloudflare")}
    sectionId="cloudflare"
/>

我们使用 cloudflare 服务用于：
- DDoS 与滥用防护
- 机器人防护（cloudflare turnstile）
- 托管和部署静态渲染的 Web 应用（cloudflare workers）

这些都是为了为所有用户提供最佳体验所必需的。
在我们所知的所有方案中，cloudflare 是最私密、最可靠的服务商。

cloudflare 完全符合 GDPR 和 HIPAA。

[了解 cloudflare 对隐私的承诺](https://www.cloudflare.com/trust-hub/privacy-and-data-protection/)。
</section>
