Html code
<!DOCTYPE html>
<html>

<head>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" integrity="sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z" crossorigin="anonymous" />
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js" integrity="sha384-9/reFTGAW83EW2RDu2S0VKaIzap3H66lZH81PoYlFhbGU+6BZp6G7niu735Sk7lN" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js" integrity="sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8shuf57BaghqFfPlYxofvL8/KUEfYiJOMMV+rV" crossorigin="anonymous"></script>
</head>

<body>
    <div class="bg-container text-center d-flex flex-column justify-content-center">
        <h1 class="counter-heading">Counter</h1>
        <p id="counterValue" class="counter-value">0</p>
        <div>
            <button onClick="onDecrement()" class="button">DECREASE</button>
            <button onClick="onReset()" class="button">RESET</button>
            <button onClick="onIncrement()" class="button">INCREASE</button>
        </div>
    </div>
</body>

</html>

CSS CODE
@import url('https://fonts.googleapis.com/css2?family=Bree+Serif&family=Caveat:wght@400;700&family=Lobster&family=Monoton&family=Open+Sans:ital,wght@0,400;0,700;1,400;1,700&family=Playfair+Display+SC:ital,wght@0,400;0,700;1,700&family=Playfair+Display:ital,wght@0,400;0,700;1,700&family=Roboto:ital,wght@0,400;0,700;1,400;1,700&family=Source+Sans+Pro:ital,wght@0,400;0,700;1,700&family=Work+Sans:ital,wght@0,400;0,700;1,700&display=swap');

.bg-container {
    background-color: #f1f5f8;
    height: 100vh;
}

.counter-heading {
    font-family: "Roboto";
    font-size: 50px;
    font-weight: 800;
}

.counter-value {
    font-size: 75px;
    font-weight: 900;
}

.button {
    background-color: #f1f5f8;
    border-width: 2px;
    border-color: black;
    border-radius: 7px;
    margin: 8px;
    padding: 5px;
}

JAVA SCRIPT CODE
let counterElement = document.getElementById("counterValue");

function onDecrement() {
    let priviousCounterValue = counterElement.textContent;
    let updatedCounterValue = parseInt(priviousCounterValue) + 1;
    if (updatedCounterValue > 0) {
        counterElement.style.color = "red";
    } else if (updatedCounterValue < 0) {
        counterElement.style.color = "green";
    } else {
        counterElement.style.color = "black";
    }
    counterElement.textContent = updatedCounterValue
}

function onIncrement() {
    let priviousCounterValue = counterElement.textContent;
    let updatedCounterValue = parseInt(priviousCounterValue) - 1;
    if (updatedCounterValue > 0) {
        counterElement.style.color = "red";
    } else if (updatedCounterValue < 0) {
        counterElement.style.color = "green";
    } else {
        counterElement.style.color = "black";
    }
    counterElement.textContent = updatedCounterValue
}

function onReset() {
    let counterValue = 0
    counterElement.textContent = counterValue
    counterElement.style.color = "Black"
}
