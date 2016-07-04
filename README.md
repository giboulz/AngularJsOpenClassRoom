# AngularJsOpenClassRoom
https://openclassrooms.com/courses/developpez-vos-applications-web-avec-angularjs/afficher-les-films-populaires

https://github.com/michelre
npm install
bower install

grunt serve



my note : 
angular note : 
<div ng-app="myApp">
    <div ng-controller="exemple1Ctrl">
        <input ng-model="age"/>
        <span>Vous êtes <b ng-bind="majeurOrMineurText()"></b></span>
</div>

-------------------------------------

var myApp = angular.module('myApp',[]);

myApp.controller("exemple1Ctrl", function($scope){
    $scope.age = 0;
    $scope.majeurOrMineurText = function(){
        return ($scope.age >= 18) ? "majeur" : "mineur";    
    };
});




ng-model : variable
ng-bind  : bind de valeur
ng-show : afficher ou pas
Angular possède nativement un certain nombre de modules comme $scope , $location
$rootScope : ensemhle des contextes de la page
$watch(watchFn, watchAction, deepWatch)

Directive : ng-model, ng-bind, ...

ngController : directive permettant d'attacher un contrôleur à la vue
ngRepeat : directive permettant de répéter un template pour chaque élément d'une collection.
ngModel : directive permettant de lier les input, textarea ou select à une propriété du contexte actuel.


création d'un projet : 

yo angular

création d'une route : 
yo angular:route popular

création d'un service : 
yo angular:factory serviceAjax

il existe angular-bootstrap
bower install angular-bootstrap -save

la définition des modules et des controlleurs / services, se fait dans le app.js

lancer les tests : 

grunt test 

lancer les tests aussi : 

karma start (dans le répertoire des tests); 

lancement du serveur : 
grunt test

création d'un controlleur : 

yo angular:controlleur NOM_CONTROLLEUR


recup de parametre dans controlleur : 

app.js :(les routes)
      .when('/search/:query', {

controlleur.js : 
        $scope.query = $routeParams.query;
