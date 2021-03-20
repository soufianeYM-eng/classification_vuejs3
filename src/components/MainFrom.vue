<template lang="">
    <div>
        <p>
            Fait par : <br/> - Soufiane Yousfi Mghari <br/>
            - Leila Samih
        </p>
        <h1>Classification des animaux</h1>

        <div class="form-group">
          <label for="">Classification 1</label>
          <select class="form-control" v-model="class1" required>
            <option value="squeInt" selected="selected">Squelette interne</option>
            <option value="squeExt">Squelette externe</option>
            <option value="coqu">Coquille</option>
            <option value="squePeau">Squelette dans la peau</option>
            <option value="harap">Harpons urticants</option>
            <option value="corps">Corps avec des anneaux</option>
          </select>
        </div>
        <hr/>
        <div v-if="class1 === 'squeInt'">
            <div class="form-group"> 
            <label for="">Classification 2</label>
            <select class="form-control" v-model="class2" >
                <option value="squedos">Squelette d'os</option>
                <option value="squecartilage">Squelette de cartilage</option>
            </select>
            </div>
        </div>
        <div v-if="class1 === 'squeExt'">
            <div class="form-group"> 
            <label for="">Classification 2</label>
            <select class="form-control" v-model="class2" >
                <option value="2antennes">2 antennes</option>
                <option value="8pattes">8 pates et des chélicères</option>
                <option value="4antennes">4 antennes</option>
            </select>
            </div>
        </div>

        <div v-if="class1 === 'coqu'">
            <div class="form-group"> 
            <label for="">Classification 2</label>
            <select class="form-control" v-model="class2" >
                <option value="tentac">De nombreux tentacules sur la tête</option>
                <option value="2partiesCoq">La coquille en 2 parties</option>
                <option value="piedPorteur">1 pied porteur</option>
            </select>
            </div>
        </div>

        <div v-if="class1 === 'squePeau'">
            <div class="alert alert-success" role="alert">
                <strong>échinodermi</strong>
            </div>
            <img src="../assets/echino.jpg" alt="exemple"/>
        </div>
        <div v-if="class1 === 'harap'">
            <div class="alert alert-success" role="alert">
                <strong>cnidaire</strong>
            </div>
            <img src="../assets/cnidaire.jpg" alt="exemple"/>
        </div>
        <div v-if="class1 === 'corps'">
            <div class="alert alert-success" role="alert">
                <strong>annélide</strong>
            </div>
            <img src="../assets/annélide.jpg" alt="exemple"/>
        </div>

        <hr/>
        <div v-if="class2 === 'squedos'">
            <div class="form-group"> 
            <label for="">Classification 3</label>
            <select class="form-control" v-model="class3" >
                <option value="4membres">il a 4 membres</option>
                <option value="nageoires">il a des nageoires à rayons</option>
            </select>
            </div>
        </div>

        <div v-if="class2 === 'squecartilage'">
            <div class="form-group"> 
            <label for="">Classification 3</label>
            <select class="form-control" v-model="class3" >
                <option value="poissonCarti">poisson a squelette cartilagineux</option>
            </select>
            </div>
        </div>


        <div v-if="class2 === '2antennes'">
            <div class="form-group"> 
            <label for="">Classification 3</label>
            <select class="form-control" v-model="class3" >
                <option value="pairePatte">Paire de pattes par segment</option>
                <option value="6pattes">il a 6 pattes, il a des ailes</option>
            </select>
            </div>
        </div>

        <div v-if="class2 === '4antennes'">
            <div class="form-group"> 
            <label for="">Classification 3</label>
            <select class="form-control" v-model="class3" >
                <option value="céphalo">il a un céphalo-thorax</option>
            </select>
            </div>
        </div>

        <div v-if="class2 === '8pattes'">
            <div class="alert alert-success" role="alert">
                <strong>arachnide</strong>
            </div>
            <img src="../assets/arachnide.jpg" alt="exemple"/>
        </div>

        <div v-if="class2 === 'tentac'">
            <div class="alert alert-success" role="alert">
                <strong>céphalopode</strong>
            </div>
            <img src="../assets/céphalopode.jpg" alt="exemple"/>
        </div>
        
        <div v-if="class2 === '2partiesCoq'">
            <div class="alert alert-success" role="alert">
                <strong>bivalve</strong>
            </div>
            <img src="../assets/bivalve.jpg" alt="exemple"/>
        </div>

        <div v-if="class2 === 'piedPorteur'">
            <div class="alert alert-success" role="alert">
                <strong>gastéropode</strong>
            </div>
            <img src="../assets/gasteropode.jpg" alt="exemple"/>
        </div>

        <hr/>

        <div v-if="class3 === '4membres'">
            <div class="form-group"> 
            <label for="">Classification 4</label>
            <select class="form-control" v-model="class4" >
                <option value="gésier">il a un gésier</option>
                <option value="poils">il a des poils, il a des mamelles</option>
                <option value="carpace">il a une carapace dorsale et ventrale</option>
                <option value="machoire">il a une mâchoire à large ouverture</option>
                <option value="4doigts">il a 4 doigts à la main</option>
            </select>
            </div>
        </div>

        <div v-if="class3 === 'nageoires'">
            <div class="alert alert-success" role="alert">
                <strong>lissamphibien</strong>
            </div>
            <img src="../assets/lissamphibien.jpg" alt="exemple"/>
        </div>

        <div v-if="class3 === 'poissonCarti'">
            <div class="alert alert-success" role="alert">
                <strong>chondrichthyen</strong>
            </div>
            <img src="../assets/chondrichthyen.jpg" alt="exemple"/>
        </div>

        <div v-if="class3 === 'pairePatte'">
            <div class="alert alert-success" role="alert">
                <strong>myriapode</strong>
            </div>
            <img src="../assets/myriapode.jpg" alt="exemple"/>
        </div>

        <div v-if="class3 === '6pattes'">
            <div class="alert alert-success" role="alert">
                <strong>insecte</strong>
            </div>
            <img src="../assets/insecte.jpg" alt="exemple"/>
        </div>

        <div v-if="class3 === 'céphalo'">
            <div class="alert alert-success" role="alert">
                <strong>crustacé</strong>
            </div>
            <img src="../assets/crustacé.jpg" alt="exemple"/>
        </div>

        <hr/>
        <div v-if="class4 === 'gésier'">
            <div class="form-group"> 
            <label for="">Classification 5</label>
            <select class="form-control" v-model="class5" >
                <option value="plumes">il a des plumes</option>
                <option value="trou">il a un trou triangulaire sur les os de la tempe</option>
            </select>
            </div>
        </div>


        <div v-if="class4 === 'poils'">
            <div class="alert alert-success" role="alert">
                <strong>Chien, chat, éléphant, souris</strong>
            </div>
            <img src="../assets/poils.jpg" alt="exemple"/>
        </div>


        <div v-if="class4 === 'carpace'">
            <div class="alert alert-success" role="alert">
                <strong>Tortus</strong>
            </div>
            <img src="../assets/Tortus.jpg" alt="exemple"/>
        </div>

        <div v-if="class4 === 'machoire'">
            <div class="alert alert-success" role="alert">
                <strong>Lézards, serpents</strong>
            </div>
            <img src="../assets/machoire.jpg" alt="exemple"/>
        </div>

        <div v-if="class4 === '4doigts'">
            <div class="alert alert-success" role="alert">
                <strong>Grenouille, crapaud</strong>
            </div>
            <img src="../assets/4doigts.jpg" alt="exemple"/>
        </div>

        <div v-if="class5 === 'plumes'">
            <div class="alert alert-success" role="alert">
                <strong>oiseau</strong>
            </div>
            <img src="../assets/oiseau.jpg" alt="exemple"/>
        </div>

        <div v-if="class5 === 'trou'">
            <div class="alert alert-success" role="alert">
                <strong>crocodilien</strong>
            </div>
            <img src="../assets/crocodilien.jpg" alt="exemple"/>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            class1 : '',
            class2 :'',
            class3:'',
            class4:'',
            class5:'',
        }
    },
    methods:{
        display(){
            alert('Hello');
        }
    },
    computed:{

    }
}
</script>
<style lang="">
    
</style>