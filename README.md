# URL <a href="https://arannamoy-mondal.github.io/Circle-Progress-Bar/">https://arannamoy-mondal.github.io/Circle-Progress-Bar/</a>

# This is basically a sample circle progress bar. If you need to make this type of element in any project simply you create the css file and copy past code link this file with html file and then, you need to same code below,
#
# CSS File
```
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
}

main{
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: #222;
    padding: 50px;
}

.container{
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 40px;
}

.container .progress{
    position: relative;
    width: 150px;
    height: 150px;
    border-radius: 50%;
    color: #fff;
    background: #444 linear-gradient(to right,
    transparent 50%,var(--clr)0);
}

.container .progress h3{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    font-size: 2.5rem;
    z-index: 1;
    font-weight: 500;
}

.container .progress h3 span{
    font-size: 2rem;
    font-weight: 400;
}

.container .progress h4{
    position: absolute;
    top: 62%;
    left: 50%;
    transform: translateX(-50%);
    z-index: 1;
    font-weight: 500;
    color: var(--clr);
    /* text-transform: uppercase; */
}

.container .progress::before{
    content: '';
    display: block;
    height: 100%;
    margin-left: 50%;
    transform-origin: left;
    border-radius: 0 100% 100% 0/50%;
}

.container .progress::after{
    content: '';
    position: absolute;
    inset: 10px;
    border-radius: 50%;
    background: #222 50%;
}


.container .progress::before{
    background: var(--clr);
    transform: rotate(calc(((var(--i) - 50) * 0.01turn)));
}

.container .progress.less::before{
    background: #444;
    transform: rotate(calc(((var(--i) - 0) * 0.01turn)));
}

/* for small screen mobile */
@media screen and (max-width:576px) {
    main{
        margin: auto;
        width: 100%;
    }
    #headLine h3{
         text-align: center;
         font-size: 1rem;
    }
    .container{
        flex-direction: column;
        gap: 15px;
    }   
    .container .progress h3{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
        font-size: 1.5rem;
        z-index: 1;
        font-weight: 500;
    } 
    .container .progress h3 span{
        font-size: 1.5rem;
        font-weight: 400;
    }
    #solidity{
        color: purple;
    }
}

/* for large device */
@media screen and (max-width:992px) {
    
}

```
# For greater or equal 50%
```
<div class="container">
<div class="progress" style="--i:"x?";--clr:#color"> <!-- "Here "x?" is the percentage of progress,#color is desire color"-->
           <h3>100<span>%</span></h3><!-- Dummy text -->
           <h4>CpIsFun</h4><!-- Dummy text -->
       </div>
</div>      
```
# For less than 50%
```
<div class="less"> <!-- just use less class type instead of progress -->
<div class="progress" style="--i:"x?";--clr:#color"> <!--"Here "x?" is the percentage of progress,#color is your desire color"-->
           <h3>100<span>%</span></h3><!-- Dummy text -->
           <h4>CpIsFun</h4><!-- Dummy text -->
       </div>
</div>
```

