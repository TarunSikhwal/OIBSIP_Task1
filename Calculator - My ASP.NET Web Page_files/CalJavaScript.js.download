function getInputValue() {
    let num = event.target.innerText
    console.log(num);
    printValue(num);
}
let buttons = document.getElementsByTagName('button');
console.log(buttons.length);
for (var i = 0; i < buttons.length; i++) {
    buttons[i].setAttribute('onclick', 'getInputValue()');
}
function printValue(val) {
    let res = document.querySelector('#display');
    let current = res.innerHTML;
    if (res.innerHTML == "") {
        if (val != "C" && val != "DEL") {
            res.innerHTML = "";
            res.innerHTML += val;
        }
    }
    else {
        if (val == "DEL") {
            console.log(current[current.length - 1]);
            res.innerText = current.slice(0, -1);
            if (res.innerHTML.length <= 1) {
                res.innerHTML = "0";
            }
        }
        if (val != "C" && val != "DEL" && val != "=") {
            res.innerHTML += val;
        }
        if (val == "=") {
            let result = res.innerHTML;
            res.innerHTML = eval(result);
        }
        if (val == "C") {
            res.innerHTML = "";
        }
    }
}