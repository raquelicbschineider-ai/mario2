const mario = document.querySelector('.mario');

const pipe = document.querySelector('.pipe');


// FUNÇÃO PARA PULAR

const jump = () => {

    mario.classList.add('jump');

    setTimeout(() => {

        mario.classList.remove('jump');

    }, 500);

};


// VERIFICAÇÃO DA COLISÃO

const loop = setInterval(() => {

    const pipePosition = pipe.offsetLeft;

    const marioPosition = +window
        .getComputedStyle(mario)
        .bottom
        .replace('px', '');


    // COLISÃO

    if (
        pipePosition <= 120 &&
        pipePosition > 0 &&
        marioPosition < 80
    ) {

        // PARA O CANO

        pipe.style.animation = 'none';

        pipe.style.left = ${pipePosition}px;


        // PARA O MARIO

        mario.style.animation = 'none';

        mario.style.bottom = ${marioPosition}px;


        // TROCA A IMAGEM

        mario.src = './images/game-over.png';


        // DIMINUI O MARIO

        mario.style.width = '75px';


        // POSICIONA O MARIO

        mario.style.marginLeft = '50px';


        // PARA O LOOP

        clearInterval(loop);

    }

}, 10);


// DETECTA UMA TECLA

document.addEventListener('keydown', jump);