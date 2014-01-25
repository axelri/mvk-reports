## Liten latex-howto

Börja med att ladda ner en latex-miljö till din platform. På Mac verkar [MacTex](http://tug.org/mactex/) populärast, för Windows verkar [MikTex](http://miktex.org/) vara ett schysst alternativ. Sitter du på linux är det enklast att googla "min dist latex". För ubuntu kan du skriva ```sudo apt-get install texlive-base``` för basutbudet och ```sudo apt-get install texlive-full``` för en större mängd paket. Det följer ofta med speciella program för att editera och kompilera latex-filer (speciellt på Windows verkar det också smidigast), men man kan också jobba med en texteditor och kommandotolken.

### Skriva latex
Rapporterna är uppdelade i olika tex-filer, som läggs ihop automatiskt när man kompilerar huvudfilen. Tanken är att man bara ska behöva skriva i filen man är ansvarig för, och inte behöva tänka på hur allt sätts samman. För att ange en ny rapportdel skriver du bara ```\section{Ditt kapitel}```, ```\subsection{Ditt underkapitel}``` osv. Sedan skriver du bara text som vanligt, latex ignorerar extra mellanslag och radbyten. Två radbyten innebär dock ett nytt stycke.

### Kompilera filerna

Använder du Mac/Linxu cd:ar du in till rätt mapp och skriver bara ```make```, ```pdflatex report.tex``` eller ```xelatex report.tex```. Xelatex har ett enklare stöd för andra språk än engelska, så föredra det om du har möjligheten. På Windows öppnar du antagligen enklast ```report.tex``` i din latex-editor och kompilerar filen därifrån.

#### Vid kaos

Det vanligaste felet är att korsreferenser eller innehållsförteckningar blir konstiga. Kompilerar man en gång till brukar det lösa sig. Det andra vanliga felet som kan uppstå är att man inte har alla latex-paket som filen använder sig av (de som finns under ```\usepackage{<package>}```). Man kan ofta ladda ner enskilda paket genom en pakethanterare, som följde med MikTex eller MacTex. I ubuntu man kan hantera paket genom kommandot ```tlmgr```.

### Hjälp

För lite mer avancerad användning brukar [The Not so Short Introduction to Latex](http://tobi.oetiker.ch/lshort/lshort.pdf) vara en bra referens. Wikibooks och StackOverflow kryllar också av exempel. Happy texing!
