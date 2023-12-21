<!-- <template>
<div class="js-countdown" v-show ="statusType !== 'expired'">
    <div class="countdown__timer">
        <div class="countdown__item day"> {{ days }} </div>
        <div class="countdown__item countdownhours"> {{ hours }} </div>
        <div class="countdown__item countdownminutes"> {{ minutes }} </div>
        <div class="countdown__item countdownseconds"> {{ seconds }} </div>
    </div>
</div>
       
</template>

<script>


export default {
    name:"Countdown",
    props: ['starttime','endtime','trans'] ,
    data: function(){
        return{
            timer:"",
            start: "",
            end: "",
            interval: "",
            days:"",
            minutes:"",
            hours:"",
            seconds:"",
        
        };
    },

    mounted(){
        this.start = new Date(this.starttime).getTime();
        this.end = new Date(this.endtime).getTime();
        // Update the count down every 1 second
        this.timerCount(this.start,this.end);
        this.interval = setInterval(() => {
            this.timerCount(this.start,this.end);
        }, 1000);
    },
    methods: {
        timerCount: function(start,end){
            // Get todays date and time
            var now = new Date().getTime();

            // Find the distance between now an the count down date
            var distance = start - now;
            var passTime =  end - now;

            if(distance < 0 && passTime < 0){
                this.statusType = "expired";
                this.statusText = this.wordString.status.expired;
                clearInterval(this.interval);
                return;

            }else if(distance < 0 && passTime > 0){
                this.calcTime(passTime);
                this.statusType = "running";

            } else if( distance > 0 && passTime > 0 ){
                this.calcTime(distance); 
                this.statusType = "upcoming";
            }
        },
        calcTime: function(dist){
        // Time calculations for days, hours, minutes and seconds
            this.days = Math.floor(dist / (1000 * 60 * 60 * 24));
            this.hours = Math.floor((dist % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            this.minutes = Math.floor((dist % (1000 * 60 * 60)) / (1000 * 60));
            this.seconds = Math.floor((dist % (1000 * 60)) / 1000);
        }
        
    }
}


</script> -->

<template>
    <div class="js-countdown" v-show="statusType !== 'expired'">
        <div class="countdown__timer">
            <div class="countdown__item day"> {{ days }} </div>
            <div class="countdown__item countdownhours"> {{ hours }} </div>
            <div class="countdown__item countdownminutes"> {{ minutes }} </div>
            <div class="countdown__item countdownseconds"> {{ seconds }} </div>
        </div>
    </div>
</template>
    
<script>
export default {
    name: "Countdown",
    props: ['starttime', 'endtime', 'trans'],
    data: function () {
        return {
            timer: "",
            start: new Date(this.starttime).getTime(),
            end: new Date(this.endtime).getTime(),
            interval: null,
            days: "",
            hours: "",
            minutes: "",
            seconds: "",
            statusType: "",
            statusText: ""
        };
    },

    mounted() {
        this.timerCount(this.start, this.end);
        this.interval = setInterval(() => {
            this.timerCount(this.start, this.end);
        }, 1000);
    },

    beforeUnmount() {
        clearInterval(this.interval);
    },

    methods: {
        timerCount: function (start, end) {
            var now = new Date().getTime();
            var distance = start - now;
            var passTime = end - now;

            if (distance < 0 && passTime < 0) {
                this.statusType = "expired";
                this.statusText = this.trans.status.expired; // Ensure 'trans' prop is passed correctly
                clearInterval(this.interval);
            } else if (distance < 0 && passTime > 0) {
                this.calcTime(passTime);
                this.statusType = "running";
            } else if (distance > 0 && passTime > 0) {
                this.calcTime(distance);
                this.statusType = "upcoming";
            }
        },

        calcTime: function (dist) {
            this.days = Math.floor(dist / (1000 * 60 * 60 * 24));
            this.hours = Math.floor((dist % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            this.minutes = Math.floor((dist % (1000 * 60 * 60)) / (1000 * 60));
            this.seconds = Math.floor((dist % (1000 * 60)) / 1000);
        }
    }
}
</script>