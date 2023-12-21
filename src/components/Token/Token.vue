
<template>
    <section class="token-details style-1" id="token">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <div class="block-text center">
                        <h3>{{title}}</h3>
                        <p class="mt-12">{{subtitle}}
                        </p>
                    </div>
                </div>
            </div>
            <div class="row mt-25">
                <div class="col-md-6">
                    <div class="infomation" data-aos="fade-up" data-aos-duration="800">
                        <ul class="info-list">
                            <li :class="item.classAction" v-for="item in dataTokendetails.slice(0,6)" :key="item.id">
                                <h5>{{item.title}}</h5>
                                <p class="fs-17">{{item.desc}}</p>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col-md-6">
                    <div class="token-details__image">
                            <img src='/Images/New_Pic3.png' height="650px" width="700px" alt="Image" /> 
                        </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>

import "./styles.scss";
import { dataTokendetails } from '../../fake-data/data-tokendeials';

export default {
    name: "Feature",
     data (){
        return {
            dataTokendetails,
            title: 'Utility Token Info',
            subtitle : 'ViZion Protocol is at the forefront of the blockchain innovation, transforming the music, film, and entertainment industry. Our Eco-System, built on the powerful SOLANA blockchain, is designed to revolutionize how these industries operate.',
        }    
    }
};
</script>
            
            