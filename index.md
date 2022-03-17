<h1> My Knitting Meme </h1>
  
This is my knitting meme. I made it because I enjoy the galaxy brain meme format and I'm sad that there aren't that many knitting memes out there. Its height is screwy because I couldn't figure out how to fix that in R but the energy is there. 

![knitting_meme](https://user-images.githubusercontent.com/100880136/158886493-8bfd7fa9-f743-429f-af8d-e997a1111254.png)


<h3>These are the reasons I made it: </h3>
<ul>
  <li>I enjoy knitting and I'm sad there aren't very many knitting memes </li>
  <li>It taught me about how to create, manipulate and combine images in R </li>
  <li>I like the galaxy brain meme format and I think the images I found are cool </li>
  <li>My lecturer is cool and gives us fun assignments so we can actually focus on them (hi Anna!) </li>
  <li>It's original, since knitting memes are usually old-fashioned and don't use fun meme formats like this one </li>
  </ul>

<h3> Here are some examples of typical knitting memes </h3> 


<h3>This is the code I used to create it: </h3>
<ol> 
<li>*Creating and naming the text images:* 

garter_text <- image_blank(width = 500, height = 500, color = "#000000") %>% image_annotate(text = "knitting in garter \nstitch because it's the \neasiest stitch and \nthe first one \nyou learned", color = "#FFFFFF", size = 50, font = "Calibri", gravity = "center") 

stock_text <- image_blank(width = 500, height = 500, color = "#000000") %>% image_annotate(text = "knitting in stockinette \nstitch because it 'lies flat' \nand is the most \ncommon/popular stitch", color = "#FFFFFF", size = 50, font = "Calibri", gravity = "center") 

all_text <- image_blank(width = 500, height = 500, color = "#000000") %>% image_annotate(text = "knitting in whatever \nstitch works best \nfor your current \nproject because knitting \nis a diverse art \nand every stitch \nhas its place somewhere", color = "#FFFFFF", size = 50, font = "Calibri", gravity = "center") 

fancy_text <- image_blank(width = 500, height = 500, color = "#000000") %>% image_annotate(text = "knitting exclusively \nin colourwork \ndiamond brocade to \nflex on the \nknitting circle", color = "#FFFFFF", size = 50, font = "Calibri", gravity = "center") </li>


<li>*Reading in the galaxy brain images:* 

brain_1 <- image_read("http://epilepsyu.com/wp-content/uploads/2015/09/small-brain.jpg") %>% image_scale(500) 

brain_2 <- image_read("https://i.kym-cdn.com/photos/images/original/001/563/180/493.jpg") %>% image_scale(500) 

brain_3 <- image_read("https://secretlabinstitute.files.wordpress.com/2021/02/galaxy-brain-m-stage-3.png?w=1200") %>% image_scale(500) 

brain_4 <- image_read("https://i1.wp.com/lucloi.vn/wp-content/uploads/2020/03/6e8734dfe00c1b1d-1024x512-1.jpg?resize=1024%2C512&ssl=1") %>% image_scale(500) </li>


<li>*Making the rows:* 

row_1 <- image_append(c(garter_text, brain_1))

row_2 <- image_append(c(stock_text, brain_2))

row_3 <- image_append(c(all_text, brain_3))

row_4 <- image_append(c(fancy_text, brain_4)) </li>


<li>*Stacking the rows:* 

full_meme -> image_append(c(row_1, row_2, row_3, row_4), stack = TRUE) %>% image_scale(750) </li>
