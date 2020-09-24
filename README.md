# JDM
Basic Community Site

With this site I wasn't aiming at design, I made this just for the example of using scss.
Why I chose this particular theme is because I like cars and especially JDM.

Her is the surge URL so you can check out the website. 
http://numberless-border.surge.sh/

Sass tools/aspects i found useful!

1. Variables

I used variables (not many) and they really help with saving time. 
What you want to start with is begin with the dollar sign ($) before the variable.
Then what you do is that you give the variable a color in this example $primarycolor ("black");
here you can see the variable name is "$primarycolor", if I want
to change the color of number of things in the code i only have to change the color in the 
variable, and voila! Every element which has the variable has been changed!

2. @import

I used this tool very helpful to keep the code short and easy to navigate through. What I did with this 
is that I made 3 extra scss files, imported them in the main scss file with "@import "./variables" and then everything
id do in the "_variables" file will automatically transfer to the main scss file. 

3. Nesting

Nesting is one of the coolest thing about sass. With nesting you can add multible classes in elements, lets see an example. 
If you have a header element and inside the header you have a paragraph and an image. In normal css you would do 
              header[
              color: blue;
              }
              .p{
              fontsize: 10px;
              }
              .h2{
              color: black;
              }
   But with nesting in sass you do this:
   
   
   header{
   color: blue;
              
              .p{
              fontsize: 10px;
              }
              .h2{
              color: black;
              }
              }
 As you can see you can "nest" the paragraph and h2 element in the header element. It really helps keep the code organized.
 
 
 4. @mixins 
 
 I also used mixins, which is a good way to save time. You use mixins like this: 
                            @mixin (name the mixin) display{
                              display: flex;
                              justify-content: center;
                              align-items: center;
                              }
                              
 So when you have done making this mixin which has the name "display" you can apply it to your code like this:
 
                        header{
                        @include display;
                        color: black;
                        font-size: 30px;
                        }
In the header element I put "@include display" which you do to call the mixin and apply it!

another aspect of mixins is a little bit more overwhelming but really useful, I did not use it in my code 
since the website is small and was only made to test my scss skills but here we go. 
Lets say you are making a border and you have this code:
          
          .border{
          border-radius: 15px;
          border-width: 15px;
          border-top-left-radius: 15px;
          }
And lets say you have multible borders in your project and you have to use this code multible times. To utilize mixins to 
help you, you do this.

          @mixin border ($p) (<--this is an instance and you can name it anything){
                border-radius: $p;
                 border-width: $p;        <---- here you add the instance in stead of the arguments.
                border-color: $p;


After you do this the only thing left is to add it to the code like this:

        .test{
          @include: border(30px) <---When adding 30px in there you change all the arguments to 30px (before they were 15px), so you see, mixins can 
          help you save extreme time if you have a lot of repetitions in your code!
          
          
          
      


5.  Reference symbol

When nesting you can use the "&" symbol to reference the parent elemen, lets see an example:

        a{
        &:hover{color: red}   <---(a:hover{color:red}
        &:visited{color: purple} <-----(a:visited{color:purple}
        
so, basically what's happening here is that the "&" symbol references the parent (a). As you can see it saves time 
and it makes nesting look neat!
        
        
                            
