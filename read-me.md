Steps :

index .css dont forget to reset properties for margin padding and box sizing

1.  Create Header component with their header module css
    then import in App.js like this :
    import Header from "./components/Layout/Header";
    then bring it inside of our funcion App component

function App() {
return (

<div className="App">
<!--* <Header />   -->
 </div>
);
}

2.  dentro del cart button component
    metemos el componente cart icon (cart/CartIcon):

        const HeaderCartButton = (props) => {

    return (
    <button className={classes.button}>
    <span className={classes.icon}>

    <!-- *<CartIcon /> -->

    </span>
    <span>Your Cart</span>
    <span className={classes.badge}>3</span>
    </button>
    );
    };

    3. Que a su vez nuestro HeaderCartButton
       pasara a nuetro componente Header.js

const Header = (props) => {
return (
<Fragment>

<header className={classes.header}>
<h1>React Meals</h1>

        <!--* <HeaderCartButton /> -->

      </header>
      <div className={classes["main-image"]}>
        <img src={mealsImage} alt="A table" />
      </div>
    </Fragment>

);
};

4.  we have three components

CartIcon ---> HeaderCartButton ---> Header ---> App.js

5.  Create more components Available meals , Meals summary and Meals

MealsSummary ---> Meals
AvailableMeals ---> Meals
Meals ---> App. js

function App() {
return (
<Fragment>
<Header />
<main>
<!-- *<Meals /> -->
</main>
</Fragment>
);
}
