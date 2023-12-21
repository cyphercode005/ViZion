<template>
    <section class="allo-dist" id="sales">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <div class="block-text center">
                        <h3>{{ title }}</h3>
                        <p class="mt-12">{{ subtitle }}</p>
                        <p class="mt-12">{{ para }}</p>
                    </div>

                    <div class="allo-dist__main" data-aos="fade-up" data-aos-duration="800">
                        <div class="flat-tabs1">
                            <Tab />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import { dataChart } from '../../fake-data/data-chart';
import Tab from "../Tab/TabAlocation/Tab";

export default {
    name: "Chart",
    components: {
        Tab,
    },
    data() {
        return {
            dataChart,
            title: 'A Transparent Approach by ViZion Protocol',
            subtitle: `
At ViZion Protocol, we're not just building a blockchain platform; we're shaping the future of the music, film, and entertainment industry by Empowering Strategic Token Utilization.
`,
            para: `Our commitment to transparency is at the heart of ViZion Protocol. Here's how our tokens are distributed:`
        }
    },
};
</script>