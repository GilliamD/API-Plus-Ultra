Front end Group Project for Digital Crafts

Japanese media site made with approaches to templating and single page app in vanilla JS

sample code from anime page: //First page populator function strawHats() { const luffy = get( https://api.themoviedb.org/3/tv/80853?api_key=cc42102845a020075536de832b824222 ); //Muhyo & Roji

luffy.then(function(rubber) {
    console.log(rubber)
        //Grabbing relvent information of which to populate in the DOM


        const doodle = rubber.backdrop_path
        const photo = rubber.poster_path
        const name = rubber.name
        const home = rubber.homepage
        const overview = rubber.overview
        const dubs = rubber.original_language

        //Setting pointers to HTML IDs as variables
        const icon = document.getElementById('icon1');
        const image = document.createElement('img');
        const iframe = document.createElement('iframe')
        const title = document.getElementById('title1');
        const website = document.getElementById('website1');
        const desk = document.getElementById('description1');
        const lang = document.getElementById('lang1');

        //Setting items 1 and 3 for Carousel
        let video = `https://www.youtube.com/embed/LYUuTF7vLcg`
        let art = `https://img1.ak.crunchyroll.com/i/spire3/8522d0abbd4217fc6b4628b1488577561533274977_full.jpg`
        let watch = `https://www.crunchyroll.com/muhyo-rojis-bureau-of-supernatural-investigation`
        car(doodle,video,art, watch);
        //Changing carousel items when name is clicked
        title.addEventListener('click', function(){
            car(doodle,video,art,watch);
        });

        //Card items
        image.setAttribute('src', `https://image.tmdb.org/t/p/w300_and_h450_bestv2/${photo}`);
        icon.appendChild(image);
        title.innerHTML = name;
        website.innerHTML = home;
        website.setAttribute('href', home);
        website.setAttribute('target', '_blank');
        desk.innerHTML = overview;
        lang.innerHTML = "available languages: " + dubs;
        
    });
Resources: NES Framework, BootStrap, jQuery

Video Game API = https://api.rawg.io/

Contribitors: Kyrathedork, GilliamD