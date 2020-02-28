<template>
    <div class="container-fluid">
        <nav class="navbar fixed-top">
            <div class="navbar-brand">
                <router-link to="/" class="link-home"><h1>CinemaWeb IDN</h1></router-link>
            </div>
        </nav>
        <h1 class="h1-title text-center p-5">Movie Details</h1>
        <div v-for="(data, index) in movie" :value="data" :key="index">
            <div class="row" v-if="filmId == data.id">
                <div class="col-md-6 text-center">
                    <img v-bind:src="data.image"  class="img-fluid img-movie" v-bind:alt="data">
                </div>
                <div class="col-md-6 text-justify pl-5 pr-5">
                    <h1>{{data.title}}</h1>
                    <button type="button" class="btn btn-primary btn-lg">
                        IMDb : {{data.rating}}</button>
                    <hr>
                    <h6><b>
                        {{data.release}} | {{data.duration}} | {{data.genre}} | {{data.age}}
                    </b></h6>
                    <br/><br/>
                    <p>Director : {{data.director}}</p>
                    <p>Cast by : {{data.cast}}</p>
                    <br/>
                    <h4>SYNOPSYS</h4>
                    <p class="desc text-justify">{{data.desc}}</p>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-12">
                <p class="text-center pt-5">
                    <router-link to='/'><button class="btn-back">BACK TO HOME</button></router-link>
                </p>
            </div>
        </div>
        <div class="row">
            <div class="col-12">
                <p class="text-center pt-3 pb-3">
                    Copyright &copy;2020 Created by Rifqi Ardhian. All Rights Reserved
                </p>
            </div>
        </div>
    </div>
</template>
<script>
import Img1 from '../assets/movie/007.jpg';
import Img2 from '../assets/movie/parasite.jpg';
import Img3 from '../assets/movie/joker.jpg';
import Img4 from '../assets/movie/fast.jpg';
import Img5 from '../assets/movie/a star is born.jpg';
import Img6 from '../assets/movie/jurrasic.jpg';
import Img7 from '../assets/movie/queen.jpg';
import Img8 from '../assets/movie/pretty_woman.jpg';

export default {
  data() {
    return {
      filmId: this.$route.params.id,
      movie: [
        {
          id: 1,
          image: Img1,
          title: '007: NO TIME TO DIE (2020)',
          rating: '0,0/10',
          release: 'Coming Soon on April 2020',
          duration: '-',
          genre: 'Action, Adventure, Thriller',
          age: '17+',
          director: 'Cary Joji Fukunaga',
          cast: 'Daniel Craig, Lea Seydoux, Ana de Armas, and many more.',
          desc: 'Some time after the capture of Ernst Stavro Blofeld, James Bond has left active service. He is approached by Felix Leiter, his friend and a CIA officer, who enlists his help in the search for Valdo Obruchev, a missing scientist. When it becomes apparent that Obruchev was abducted, Bond must confront a danger the likes of which the world has never seen before.',
        },
        {
          id: 2,
          image: Img2,
          title: 'PARASITE (2019)',
          rating: '8,6/10',
          release: 'June 24, 2019 (Indonesia)',
          duration: '2h 12min',
          genre: 'Comedy, Drama, Thriller',
          age: '17+',
          director: 'Bong Joon Ho',
          cast: 'Kang-ho Song, Sun-kyun Lee, Yeo-jeong Jo, and many more.',
          desc: 'The Kim family—father Ki-taek, mother Chung-sook, daughter Ki-jung and son Ki-woo—live in a small semi-basement apartment (banjiha), have low-paying temporary jobs as pizza box folders, and struggle to make ends meet. One day, Min-hyuk, a friend of Ki-woos and a university student, gives the family a scholars rock, which is meant to promise wealth to whoever possesses it. He suggests that, when he leaves to study abroad, Ki-woo should take over his job as an English tutor to the wealthy Park familys daughter, Da-hye. Ki-woo poses as a university student and is hired by the Parks, Mrs. Park decides they will call him Kevin.',
        },
        {
          id: 3,
          image: Img3,
          title: 'JOKER (2019)',
          rating: '8,6/10',
          release: 'October 2, 2019 (Indonesia)',
          duration: '2h 2min',
          genre: 'Crime, Drama, Thriller',
          age: '17+',
          director: 'Todd Phillips',
          cast: 'Joaquin Phoenix, Robert De Niro, Zazie Beetz, and many more.',
          desc: 'Before the show goes live, Arthur requests that Murray introduce him as Joker, a reference to Murrays previous mockery. Arthur walks out to applause, but starts telling morbid jokes, confesses to the train murders, and rants about how society abandons the downtrodden and mentally ill. Arthur kills Murray and is arrested as riots break out across Gotham. One rioter corners the Wayne family in an alley and murders Thomas and his wife, Martha, sparing Bruce. Rioters in an ambulance crash into the police car carrying Arthur, freeing him, he dances to the cheers of the crowd.',
        },
        {
          id: 4,
          image: Img4,
          title: 'FAST & FURIOUS PRESENTS: HOBBS & SHAW (2019)',
          rating: '6,5/10',
          release: 'July 31, 2019 (Indonesia)',
          duration: '2h 17min',
          genre: 'Action, Adventure',
          age: '17+',
          director: 'David Leitch',
          cast: 'Dwayne Johnson, Jason Statham, Vanessa Kirby, and many more.',
          desc: 'Luke Hobbs and Deckard Shaw, Hatties brother, are both informed of the missing virus and are reluctantly assigned to work together to track it down. After a brief meeting at a CIA black site at Leadenhall Building, Deckard goes to Hatties house for information, while Hobbs manages to find Hattie, after a brief scuffle, he brings her to the CIA office, as Deckard then returns. The office is attacked, and Hattie is taken by Brixton, whom Deckard recognizes as an old colleague-turned-enemy hed previously shot and supposedly killed. Hobbs and Deckard pursue and rescue Hattie during an ensuing car chase, managing to escape from Brixton, who crashes into a double-decker bus. However, Brixton frames all three as traitors via Eteons control of global news media.',
        },
        {
          id: 5,
          image: Img5,
          title: 'A STAR IS BORN (2018)',
          rating: '7,7/10',
          release: 'October 19, 2018 (Indonesia)',
          duration: '2h 16min',
          genre: 'Drama, Music, Romance',
          age: '17+',
          director: 'Bradley Cooper',
          cast: 'Lady Gaga, Bradley Cooper, Sam Elliott, and many more.',
          desc: 'Jackson "Jack" Maine, a famous country-rock singer, privately battling an alcohol and drug addiction, plays a concert. His main support is Bobby, his manager and older half-brother. After a show, Jack goes out for drinks and visits a drag bar where he witnesses a tribute performance to Edith Piaf by Ally, who works as a waitress and singer-songwriter. Jack is amazed by her performance, and they spend the night talking to each other, where Ally discloses to him her unsuccessful efforts in pursuing a professional music career. Ally shares with Jack some lyrics she has been working on, and Jack tells Ally she is a talented songwriter and should perform her own material.',
        },
        {
          id: 6,
          image: Img6,
          title: 'JURASSIC WORLD : FALLEN KINGDOM (2018)',
          rating: '6,2/10',
          release: 'June 6, 2018 (Indonesia)',
          duration: '2h 8min',
          genre: 'Action, Adventure, Sci-Fi',
          age: '13+',
          director: 'J.A. Bayona',
          cast: 'Chris Pratt, Bryce Dallas Howard, Rafe Spall, and many more.',
          desc: 'In 2018, a U.S. Senate hearing in Washington, D.C. debates whether Isla Nublars dinosaurs should be saved from an impending volcanic eruption. Mathematician Dr. Ian Malcolm testifies that the dinosaurs should be allowed to die to correct John Hammond wrongfully cloning them. Meanwhile, Jurassic Worlds former operations manager, Claire Dearing, has established the Dinosaur Protection Group to save the animals. After the Senate rules against rescuing the animals, Hammonds former partner, Benjamin Lockwood, summons Claire to his Northern California estate. Lockwood and his aide, Eli Mills, reveal a plan to relocate the dinosaurs to a new island sanctuary. Claire is needed to reactivate the parks dinosaur tracking system to locate the animals, particularly Blue, the last surviving Velociraptor. Though they are now estranged, Claire recruits Owen Grady, Jurassic Worlds former Velociraptor trainer, to help capture her.',
        },
        {
          id: 7,
          image: Img7,
          title: 'BOHEMIAN RHAPSODY (2018)',
          rating: '8,0/10',
          release: 'October 30, 2018 (Indonesia)',
          duration: '2h 14min',
          genre: 'Biography, Drama, Music',
          age: '17+',
          director: 'Bryan Singer',
          cast: 'Rami Malek, Lucy Boynton, Gwilym Lee, and many more.',
          desc: 'Bohemian Rhapsody is a 2018 biographical drama film about Freddie Mercury, the lead singer of the British rock band Queen. It was directed by Bryan Singer from a screenplay by Anthony McCarten, and produced by Graham King and Queen manager Jim Beach. It stars Rami Malek as Mercury, with Lucy Boynton, Gwilym Lee, Ben Hardy, Joe Mazzello, Aidan Gillen, Tom Hollander, Allen Leech, and Mike Myers in supporting roles. Queen members Brian May and Roger Taylor served as consultants. A British-American venture, the film was produced by 20th Century Fox, Regency Enterprises, GK Films, and Queen Films, with Fox serving as distributor. The film follows the singers life from the formation of the band up to their 1985 Live Aid performance at the original Wembley Stadium.',
        },
        {
          id: 8,
          image: Img8,
          title: 'PRETTY WOMAN (1990)',
          rating: '7,0/10',
          release: 'Mar 23, 1990 (Indonesia)',
          duration: '1h 59min',
          genre: 'Comedy, Romance',
          age: 'R',
          director: 'Garry Marshall',
          cast: 'Richard Gere, Julia Roberts, Jason Alexander, and many more.',
          desc: 'High-powered businessman Edward Lewis is dumped by his girlfriend during an unpleasant phone call wherein he asked her to escort him during his business trip; she has finally had enough of being treated solely as his "beck and call girl." Edward is a corporate raider from New York, who buys companies that are in financial trouble and tears them down piece by piece. Leaving a business party in the Hollywood Hills, he takes his lawyers Lotus Esprit sports car and accidentally ends up on Hollywood Boulevard in the citys red-light district, where he encounters prostitute Vivian Ward. As he is having difficulties driving the car, she gets in and guides him to the Regent Beverly Wilshire Hotel, where he is staying. It becomes clear that Vivian knows more about the Lotus than he does, and he lets her drive. Vivian charges Lewis $20 for the ride, and they separate. She goes to a bus stop, where he finds her and offers to hire her for the night; the next day, he asks Vivian to play the role his girlfriend has refused, offering her $3000 to stay with him for the next six days as well as to buy her a new, more acceptable wardrobe. That evening, going to a business dinner, Edward is visibly moved by Vivians transformation brought about by the helpful manager of the hotel and begins seeing Vivian in a different light. He begins to open up to her, revealing details about his personal and business lives.',
        },
      ],
    };
  },
};
</script>
<style scoped>
.container-fluid {
    background-color: #e0e0e0;
    padding-top: 100px;
}
.navbar {
    width: 100%;
    background-color: #08344f;
    color: #dedede;
    margin-left: 0;
    box-shadow: 0 5px 7px 0 #363636;
}
.navbar-brand {
    font-family: 'Courgette';
}
.link-home {
    color: #dedede;
    text-decoration: none;
    transition: 0.3s;
}
.link-home:hover {
    color: gold;
}
.jumbotron {
    height: 250px;
    border-radius: 0;
}
.h1-title {
    font-family: 'Habibi';
    color: #cfc20e;
}
.img-movie {
    width: 500px;
    box-shadow: 0 5px 7px 0 rgb(17, 17, 17);
}
.btn-back {
    background-color: #cfc20e;
    color: #fff;
    border: 0px;
    border-radius: 60px;
    text-align: center;
    margin: 5px 2px;
    padding: 20px 15px;
    cursor: pointer;
    transition: 0.3s;
    margin: 20px;
    width: 300px;
}
.btn-back:hover {
    background-color: transparent;
    border: 2px solid #cfc20e;
    color: #cfc20e;
}
</style>
