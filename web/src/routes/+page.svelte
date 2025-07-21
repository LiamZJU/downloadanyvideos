<script>
    import { t } from "$lib/i18n/translations";

    import Omnibox from "$components/save/Omnibox.svelte";
    import Meowbalt from "$components/misc/Meowbalt.svelte";
    import SupportedServices from "$components/save/SupportedServices.svelte";
</script>

<svelte:head>
    <title>{$t("general.cobalt")}</title>
    <meta property="og:title" content={$t("general.cobalt")} />
</svelte:head>

<div id="cobalt-save-container" class="center-column-container">
    <div class="main-title">
        <span style="color: black; font-weight: bold;">Download</span><span style="color: #fe0000; font-weight: bold;">Any</span>
    </div>
    <SupportedServices />
    <main
        id="cobalt-save"
        tabindex="-1"
        data-first-focus
    >
        <Omnibox />
    </main>
    <div id="terms-note">
        {$t("save.terms.note.agreement")}
        <a href="/about/terms">{$t("save.terms.note.link")}</a>
    </div>
    <div id="powered-by">
        Powered by <a href="https://x.com/ding_liam" target="_blank" rel="noopener" style="color:#fe0000;font-weight:bold;text-decoration:underline;">LiamDING</a>
    </div>
</div>

<style>
    #cobalt-save-container {
        padding: var(--padding);
        overflow: hidden;
    }

    #cobalt-save {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 100%;
        gap: 15px;
    }

    #terms-note {
        bottom: 0;
        color: var(--gray);
        font-size: 12px;
        text-align: center;
        padding-bottom: 6px;
        font-weight: 500;
    }

    .main-title {
        width: 100%;
        text-align: center;
        font-size: 2.2rem;
        font-family: inherit;
        margin-bottom: 0;
        margin-top: 0.2rem;
        letter-spacing: 1px;
    }

    @media screen and (max-width: 535px) {
        #cobalt-save-container {
            padding-top: calc(var(--padding) / 2);
        }

        #terms-note {
            font-size: 11px;
            padding-bottom: 0;
        }
    }

    #powered-by {
        text-align: center;
        font-size: 11px;
        color: var(--gray);
        margin-top: 2px;
        margin-bottom: 8px;
        letter-spacing: 0.5px;
    }
</style>
