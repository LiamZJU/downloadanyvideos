<script lang="ts">
    import { t } from "$lib/i18n/translations";
    import cachedInfo from "$lib/state/server-info";
    import { getServerInfo } from "$lib/api/server-info";

    import Skeleton from "$components/misc/Skeleton.svelte";
    import PopoverContainer from "$components/misc/PopoverContainer.svelte";

    let services: string[] = [];
    let expanded = true;
    let servicesContainer: HTMLDivElement;
    let loaded = false;

    // 用户量级排序，常见大平台优先
    const serviceOrder = [
        "twitter", "bilibili", "instagram", "tiktok", "xiaohongshu", "facebook", "reddit", "pinterest", "vimeo", "youtube", "tumblr", "snapchat", "soundcloud", "vk", "dailymotion", "ok", "rutube", "bluesky", "streamable", "loom", "newgrounds", "twitch clips"
    ];

    function sortServices(arr: string[]) {
        return arr.slice().sort((a, b) => {
            const ia = serviceOrder.indexOf(a.toLowerCase());
            const ib = serviceOrder.indexOf(b.toLowerCase());
            if (ia === -1 && ib === -1) return a.localeCompare(b);
            if (ia === -1) return 1;
            if (ib === -1) return -1;
            return ia - ib;
        });
    }

    const loadInfo = async () => {
        await getServerInfo();
        if ($cachedInfo) {
            loaded = true;
            services = sortServices($cachedInfo.info.cobalt.services);
        }
    };
    loadInfo();
</script>

<div id="supported-services" class:expanded>
    <div class="services-title">
        {$t("save.services.title")}
    </div>
    <PopoverContainer id="services-popover" expanded={true}>
        <div
            id="services-container"
            bind:this={servicesContainer}
            tabindex="-1"
        >
            {#if loaded}
                {#each services as service}
                    <div class="service-item">{service}</div>
                {/each}
            {:else}
                {#each { length: 17 } as _}
                    <Skeleton
                        class="elevated"
                        width={Math.random() * 44 + 50 + "px"}
                        height="24.5px"
                    />
                {/each}
            {/if}
        </div>
    </PopoverContainer>
</div>

<style>
    #supported-services {
        display: flex;
        position: relative;
        max-width: 400px;
        flex-direction: column;
        align-items: center;
        height: 35px;
        margin-bottom: 0;
        margin-top: 0.5rem;
    }
    .services-title {
        font-size: 14px;
        font-weight: 500;
        margin-bottom: 2px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    #services-container {
        display: flex;
        flex-wrap: wrap;
        flex-direction: row;
        gap: 3px;
    }
    .service-item {
        display: flex;
        padding: 4px 8px;
        border-radius: calc(var(--border-radius) / 2);
        background: var(--button-elevated);
        font-size: 12.5px;
        font-weight: 500;
    }
</style>
