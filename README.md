    let popcat_counter = 0;

    let cat = document.getElementById("p");
    let open_popcat =  function (){
        popcat_counter++;
        cat.innerHTML = popcat_counter;
        cat.id = "op";
        let pop_sound = new Audio("pops/pop1.mp3");
        pop_sound.load();
        pop_sound.play();
    }

    let close_popcat = function (){
        cat.id = "p";
    }

    let p_func = function (){
        setTimeout  (close_popcat, 50)
    }

    close_popcat = () => setTimeout(()=>cat.id="p", 50)

    document.addEventListener("keydown", open_popcat);
    document.addEventListener("keyup", close_popcat);
    document.addEventListener("pointerdown",open_popcat);
    document.addEventListener("pointerup",close_popcat);
