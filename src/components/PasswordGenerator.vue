<template>
    <div class="main">
        <div class="generator">
            <div class="password-display">
                <p>aabbcc0123456789aabbcc0123456789aabbcc0123456789aabbcc</p>
            </div>
            <div class="length">
                <p>length:</p>
                <input type="range" min="1" max="512" value="16" class="slider" id="passwordRange">
                <input type="number" class="length-input" >
            </div>
            <div class="options">
                <div class="option">
                    <input type="checkbox" id="uppercase" name="uppercase" checked />
                    <label class="option-label" for="uppercase">Uppercase</label>
                </div>
                <div class="option">
                    <input type="checkbox" id="lowercase" name="lowercase" checked />
                    <label for="lowercase">Lowercase</label>
                </div>
                <div class="option">
                    <input type="checkbox" id="numbers" name="numbers" checked />
                    <label for="numbers">Numbers</label>
                </div>
                <div class="option">
                    <input type="checkbox" id="symbols" name="symbols" checked />
                    <label for="symbols">Symbols</label>
                </div>
            </div>
            <div class="main-button">
                <button>GENERATE PASSWORD</button>
            </div>
            <div class="secondary-button">
                <button>COPY</button>
                <button>RANDOM CONFIG</button>
            </div>
        </div>
    </div>
</template>

<style>
    .main{
        width: 100%;
        height: calc(100vh - 60px - 50px);

        display: flex;
        justify-content: center;
        align-items: center;

        font-family: "Courier Prime", monospace;
    }

    .generator{
        width: 30%;
        height: 50%;
        border: solid 1px var(--color-primary-trans);
        border-radius: 5px;
        padding-top: 30px;

        display: flex;
        flex-direction: column;
        gap: 20px;
        align-items: center;
    }

    .password-display{
        width: 86%;
        max-height: 150px ;
        border: solid 1px var(--color-primary-trans);
        border-radius: 5px;
        padding: 15px 5px;

        font-family: "Share Tech Mono", monospace;
        font-size: 1.6em;
        word-break: break-all;
        line-height: 0.9;

        display: flex;
        justify-content: center;
        overflow-y: scroll;
        scrollbar-width: none;
    }
    .password-display::selection{
        color: var(--color-primary-dark);
        background: var(--color-primary-trans);
    }
    .password-display:focus-within{
        border-width: 3px;
    }

    .length{
        font-size: 1.2em;
        font-family: "Courier Prime", monospace;
        width: 86%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .slider {
        display: inline;

        -webkit-appearance: none;  /* Override default CSS styles */
        appearance: none;
        width: 60%; /* Full-width */
        height: 3px; /* Specified height */
        background: var(--color-primary-trans); /* Grey background */
        opacity: 0.7; /* Set transparency (for mouse-over effects on hover) */
        -webkit-transition: .2s; /* 0.2 seconds transition on hover */
        transition: opacity .2s;
    }
    .slider:active{
        outline: var(--color-primary) thin solid;
    }
    .slider::-webkit-slider-thumb {
        -webkit-appearance: none; /* Override default look */
        appearance: none;
        width: 3px; /* Set a specific slider handle width */
        height: 15px; /* Slider handle height */
        opacity: 1;
        background: var(--color-primary); /* Green background */
        cursor: pointer; /* Cursor on hover */
    }
    .slider::-moz-range-thumb {
        width: 3px; /* Set a specific slider handle width */
        height: 15px; /* Slider handle height */
        opacity: 1;
        background: var(--color-primary); /* Green background */
        cursor: pointer; /* Cursor on hover */
    }
    .slider:hover {
        opacity: 1; /* Fully shown on mouse-over */
    }
    .length-input{
        width: 2em;
        font-size: 1em;
        font-family: "Courier Prime", monospace;
        border:none;
        background-color: var(--color-primary-dark);
        color: var(--color-primary);
    }
    /* Chrome, Safari, Edge, Opera  hide arrow*/
    input::-webkit-outer-spin-button,
    input::-webkit-inner-spin-button {
        -webkit-appearance: none;
        margin: 0;
    }
    /* Firefox hide arrow*/
    /*input[type=number] {
        -moz-appearance: textfield;
    }*/
    .length-input:focus{
        outline: solid thin var(--color-primary-mono);
    }

    .options{
        width: 86%;

        display: flex;
        flex-wrap: wrap;
    }

    .option{
        width: 50%;

        display: flex;
    }

    .option:active{
        background: var(--color-primary-dark);
    }

    .option label{
        margin-left: 10px;
    }

    .option input{
        accent-color: var(--color-primary);
    }

    .main-button{
        width: 86%;
    }
    .main-button button{
        cursor:pointer;
        width: 100%;
        height: 35px;
        background-color: var(--color-primary);
        border: none;
        border-radius: 5px;
        transition-duration: 0.4s;

        font-family: "Courier Prime", monospace;
        font-weight: bold;
        font-size: 20px;
    }
    .main-button button:hover{
        background-color: var(--color-primary-light-20);
    }
    .main-button button:active{
        background-color: var(--color-primary-dark-10);
    }

    .secondary-button{
        width: 86%;
        display: flex;
        justify-content: space-between;
    }

    .secondary-button button{
        cursor:pointer;
        width: 48%;
        height: 35px;
        background-color: transparent;
        color: var(--color-primary);
        border: solid thin var(--color-primary);
        border-radius: 5px;
        transition-duration: 0.4s;

        font-family: "Courier Prime", monospace;
        font-weight: bold;
        font-size: 16px;
    }
    .secondary-button button:hover{
        background-color: #03251A;
        border:none;
    }
    .secondary-button button:active{
        background-color: #064a34;
        border: solid thin var(--color-primary);
        color: var(--color-primary-light-20);
    }

</style>