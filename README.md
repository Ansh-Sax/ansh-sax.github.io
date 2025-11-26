# ansh-sax.github.io
Academic Website

The html files in this repository are pretty much self-explanatory in context of the tabs on the website.

The idea for "Publications" is that I'll make the paper title a hyperlink pointint directly to the pdf hosted on arxiv. This way, the most up-to-date publically available version of the paper should be accessible at all times (given that I keep the arxiv link up-to-date).

The idea for the "Blog" tab is to link each note / writing to a pdf living in the "notes" repository, which will in turn be locally editable using my personal computers via VSCode, through GitHack service which opens the pdf as if it was being natively hosted (i.e., without the github pdf viewer interface; for more on this see below).
This way, I can locally edit files on my personal computer and have the changes reflected upon comitting directly on the website in an aesthetically pleasing way without needing to do much else! Here's more information on this:
1. Oriignally I was hosting the pdfs inside the Ansh-Sax.github.io repository itself. The pdfs opened natively and looked nice. However, I wanted to organize the notes I write as a separate directory with all the relevant files (latex document, etc.), and putting a whole directory in this repository for each note would have led to clutter.
2. So, I created a new repository named "notes" to house directories for each piece of note / writing I put on the blog (or not!). If I link the notes in that repository in the Blog tab in this repository, then the pdf opens using the Github pdf viewer with all the other assets related to the pdf (like latex file) viewable on the sidebar. This was not aesthetically pleasing. One solution to fix this was to create GitHub pages for the notes repository too, but _ didn't want to do that -- I wanted to make it so that the only things that go on the academic website are directly controllable via this repository itself.
3. That's why I've used GitHack to point to the pdf in notes from the Blog tab in this repository. It makes it so that clicking on the link opens a pdf as if it were hosted natively. This allows me to keep the academic website and the notes on it completely separate while not compromising aesthetically. Earlier I was using jsDelivr which provides a similar service, except it caches the website for ~24 hours for faster loading times -- this also means that editing the pdf locally doesn't "instantly" reflect the changes on the website, taking 24 hours instead.
4. Completely separately, I've connected my GitHub account to the VSCode on my personal computer(s). I edit the document on the computer locally - commit the changes when I'm done - the change syncs on the notes repository - pdf changes automatically - the address of the pdf in the Blog tab here doesn't change, and therefore the pdf accessible via the website automatically changes. More on this in the README document in the notes repository.

The way the above is accomplished is via using the following piece of code:
<!-- Note 1 -->
            <div class="blog-entry">
                <div class="blog-title">
                    <!-- Note: The href filename below has the colon removed. 
                         Please ensure your file on GitHub is named exactly: 
                         Yang-Mills Learning Seminar Shen-Zhu-Zhu ’22, Part II.pdf -->
                    1. <a href="https://raw.githack.com/Ansh-Sax/notes/main/YM_Learning_Seminar_SSZ_Part_II/YM_Learning_Seminar_SSZ_Part_II.pdf" target="_blank">Yang-Mills Learning Seminar: Shen-Zhu-Zhu ’22, Part II</a>
                </div>
                <div class="blog-desc">
                    An exposition of Section 4.1 of <a href="https://arxiv.org/abs/2204.12737" target="_blank" class="taupe-hover"><i>A stochastic analysis approach to lattice Yang–Mills at strong coupling</i></a> by Shen-Zhu-Zhu (2022).
                    I based my talk at a learning seminar on these notes.
                </div>
            </div>
The colour used for each title (which is in italic) is Mahagony, and the colour used for links in the description (which is a smaller font) is Taupe.

I used Gemini to help me create this website. I took inspiration from https://soumith.ch/, https://cims.nyu.edu/~bourgade/, and https://sites.google.com/view/bbringmann/home?authuser=0.
