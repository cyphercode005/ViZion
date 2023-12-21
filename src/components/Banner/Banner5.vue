
<template>
    <section class="banner-top style-4">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <div class="banner-top__content">
                        <h2 class="title">{{title}}</h2>
                        <p class="desc">{{desc}}</p>
                        <div class="button">
                            <a class="btn-action style-4" href="/home-defi-01"><span class="effect">BUY TOKEN NOW</span></a>
                        </div>
                    </div>
                </div>
                <div class="col-md-12">
                    <div class="banner-top__sale">
                        <div class="block-text">
                            <h3 class="heading">{{title2}}</h3>
                            <p class="fs-17">{{desc2}}</p>
                        </div>
                        <div class="sale-content">
                        <Countdown 
                            starttime="Jul 1, 2022 15:37:25" 
                            endtime="Dec 8, 2022 16:37:25" >
                        </Countdown>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
            
</template>

<script>
import Countdown from '../Layouts/Countdown.vue';
import "./styles.scss";
import { dataBanner } from '../../fake-data/databanner';

export default {
    name: "About",
     components: {
        Countdown,
    },
    data (){
        return {
            dataBanner,
            title : 'Join the future of ICOLand crypto trading strategies',
            title2 : '50.000.000 HVR to be sold!',
            desc : 'IcoCoin is a public blockchain protocol deploying a suite of algorithmic decentralized stablecoins which underpin a thriving ecosystem that brings DeFi to the masses.',
            desc2:'During Pre-Sale, get 5x tokens or 50.000 HVR per Ether. During regular sale, it will be 10.000 HVR per Ether.'
        }    
    }
};
</script>
            
            