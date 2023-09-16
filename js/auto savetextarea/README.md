
#host link:https://digvijay212.github.io/geekm5/js/auto%20savetextarea/


#js


const textarea = document.getElementById("myTextarea");

function saveToLocalStorage() {
    localStorage.setItem("savedText", textarea.value);
}

if (localStorage.getItem("savedText")) {
    textarea.value = localStorage.getItem("savedText");
}
textarea.addEventListener("input", saveToLocalStorage);

