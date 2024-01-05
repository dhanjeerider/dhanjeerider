### Hi there 👋

**dhanjeerider/dhanjeerider** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...


<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <title>Page title</title>
</head>
<body>
           <!--=============== REMIXICONS ===============-->
        <link href="https://cdn.jsdelivr.net/npm/remixicon@2.5.0/fonts/remixicon.css" rel="stylesheet">

        <!--=============== BATTERY ===============-->
        <section class="battery">
            <div class="battery__card">
                <div class="battery__data">
                    <p class="battery__text">Battery</p>
                    <h1 class="battery__percentage">
                        20%
                    </h1>

                    <p class="battery__status">
                        Low battery <i class="ri-plug-line animated-red"></i>
                    </p>
                </div>

                <div class="battery__pill">
                    <div class="battery__level">
                        <div class="battery__liquid"></div>
                    </div>
                </div>
            </div>
        </section>
        <style>/*=============== GOOGLE FONTS ===============*/
@import url('https://fonts.googleapis.com/css2?family=Google+Sans:wght@100;200;300;400;500;700;900&display=swap');

/*=============== VARIABLES CSS ===============*/
:root {
  /*========== Colors ==========*/
  /*Color mode HSL(hue, saturation, lightness)*/
  --gradient-color-red: linear-gradient(90deg, 
                          hsl(7, 89%, 46%) 15%,
                          hsl(11, 93%, 68%) 100%);
  --gradient-color-orange: linear-gradient(90deg, 
                           hsl(22, 89%, 46%) 15%,
                           hsl(54, 90%, 45%) 100%);
  --gradient-color-yellow: linear-gradient(90deg, 
                           hsl(54, 89%, 46%) 15%,
                           hsl(92, 90%, 45%) 100%);
  --gradient-color-green: linear-gradient(90deg, 
                          hsl(92, 89%, 46%) 15%,
                          hsl(92, 90%, 68%) 100%);
  --text-color: #fff;
  --body-color: hsl(0, 0%, 11%);
  --container-color: hsl(0, 0%, 9%);

  /*========== Font and typography ==========*/
  /*.5rem = 8px | 1rem = 16px ...*/
  --body-font: 'Google Sans', sans-serif;

  --biggest-font-size: 2.5rem;
  --normal-font-size: .938rem;
  --smaller-font-size: .75rem;
}

/* Responsive typography */
@media screen and (min-width: 968px) {
  :root {
    --biggest-font-size: 2.75rem;
    --normal-font-size: 1rem;
    --smaller-font-size: .813rem;
  }
}

/*=============== BASE ===============*/
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

body {
  font-family: var(--body-font);
  font-size: var(--normal-font-size);
  background-color: var(--body-color);
  color: var(--text-color);
}

/*=============== BATTERY ===============*/
.battery{
    height: 100vh;
    display: grid;
    place-items: center;
    margin: 0 1.5rem;
}

.battery__card{
    position: relative;
    width: 100%;
    height: 240px;
    background-color: var(--container-color);
    padding: 1.5rem 2rem;
    border-radius: 1.5rem;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    align-items: center;
}

.battery__text{
    margin-bottom: .5rem;
}

.battery__percentage{
    font-size: var(--biggest-font-size);
}

.battery__status{
    position: absolute;
    bottom: 1.5rem;
    display: flex;
    align-items: center;
    column-gap: .5rem;
    font-size: var(--smaller-font-size);
}

.battery__status i{
    font-size: 1.25rem;
}

.battery__pill{
    position: relative;
    width: 75px;
    height: 180px;
    background-color: var(--container-color);
    box-shadow: inset 20px 0 48px hsl(0, 0%, 16%),
                inset -4px 12px 48px hsl(0, 0%, 56%);
    border-radius: 3rem;
    justify-self: flex-end;
}

.battery__level{
    position: absolute;
    inset: 2px;
    border-radius: 3rem;
    overflow: hidden;
}

.battery__liquid{
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 36px;
    background: var(--gradient-color-red);
    box-shadow: inset -10px 0 12px hsla(0, 0%, 0%, .1),
                inset 12px 0 12px hsla(0, 0%, 0%, .15);
    transition: .3s;
}

.battery__liquid::after{
    content: '';
    position: absolute;
    height: 8px;
    background: var(--gradient-color-red);
    box-shadow: inset 0 -3px 6px hsla(0, 0%, 0%, .2);
    left: 0;
    right: 0;
    margin: 0 auto;
    top: -4px;
    border-radius: 50%;
}

/* Full battery icon color */
.green-color{
    background: var(--gradient-color-green);
}

/* Battery charging animation */
.animated-green{
    background: var(--gradient-color-green);
    animation: animated-chargin-battery 1.2s infinite alternate;
}

/* Low battery animation */
.animated-red{
    background: var(--gradient-color-red);
    animation: animated-low-battery 1.2s infinite alternate;
}

.animated-green,
.animated-red,
.green-color{
    -webkit-background-clip: text;
    color: transparent;
}

@keyframes animated-chargin-battery{
    0%{
        text-shadow: none;
    }
    100%{
        text-shadow: 0 0 6px hsl(92, 90%, 68%);
    }
}

@keyframes animated-low-battery{
    0%{
        text-shadow: none;
    }
    100%{
        text-shadow: 0 0 8px hsl(0, 89%, 46%);
    }
}

/* Liquid battery with gradient color */
.gradient-color-red,
.gradient-color-red::after{
    background: var(--gradient-color-red);
}

.gradient-color-orange,
.gradient-color-orange::after{
    background: var(--gradient-color-orange);
}

.gradient-color-yellow,
.gradient-color-yellow::after{
    background: var(--gradient-color-yellow);
}

.gradient-color-green,
.gradient-color-green::after{
    background: var(--gradient-color-green);
}

/*=============== BREAKPOINTS ===============*/
/* For small devices */
@media screen and (max-width: 320px){
    .battery__card{
        zoom: .8;
    }
}

/* For medium devices */
@media screen and (min-width: 430px){
    .battery__card{
        width: 312px;
    }
}

/* For large devices */
@media screen and (min-width: 1024px){
    .battery__card{
        zoom: 1.5;
    }
}</style>
<script>
   /*=============== BATTERY ===============*/
initBattery()

function initBattery(){
    const batteryLiquid = document.querySelector('.battery__liquid'),
          batteryStatus = document.querySelector('.battery__status'),
          batteryPercentage = document.querySelector('.battery__percentage')
    
    navigator.getBattery().then((batt) =>{
        updateBattery = () =>{
            /* 1. We update the number level of the battery */
            let level = Math.floor(batt.level * 100)
            batteryPercentage.innerHTML = level+ '%'

            /* 2. We update the background level of the battery */
            batteryLiquid.style.height = `${parseInt(batt.level * 100)}%`

            /* 3. We validate full battery, low battery and if it is charging or not */
            if(level == 100){ /* We validate if the battery is full */
                batteryStatus.innerHTML = `Full battery <i class="ri-battery-2-fill green color"></i>`
                batteryLiquid.style.height = `103%` /* To hide the ellipse */
            }
            else if(level <= 20 &! batt.charging){ /* We validate if the battery is low */
                batteryStatus.innerHTML = `Low battery <i class="ri-plug-line animated-red"></i>`
            }
            else if(batt.charging){ /* We validate if the battery is charging */
                batteryStatus.innerHTML = `Charging... <i class="ri-flashlight-line animated-green"></i>`
            }
            else{ /* If it's not loading, don't show anything. */
                batteryStatus.innerHTML = ''
            }

            /* 4. We change the colors of the battery and remove the other colors */
            if(level <= 20){
                batteryLiquid.classList.add('gradient-color-red')
                batteryLiquid.classList.remove('gradient-color-orange', 'gradient-color-yellow','gradient-color-green')
            }
            else if(level <= 40){
                batteryLiquid.classList.add('gradient-color-orange')
                batteryLiquid.classList.remove('gradient-color-red', 'gradient-color-yellow','gradient-color-green')
            }
            else if(level <= 80){
                batteryLiquid.classList.add('gradient-color-yellow')
                batteryLiquid.classList.remove('gradient-color-red', 'gradient-color-orange','gradient-color-green')
            }
            else{
                batteryLiquid.classList.add('gradient-color-green')
                batteryLiquid.classList.remove('gradient-color-red', 'gradient-color-orange','gradient-color-yellow')
            }
        }
        updateBattery()

        /* 5. Battery status events */
        batt.addEventListener('charginchange', () => {updateBattery()})
        batt.addEventListener('levelchange', () => {updateBattery()})
    })      
}
</script>
</body>
</html>
