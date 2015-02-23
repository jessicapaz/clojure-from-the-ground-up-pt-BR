<!-- This guide aims to introduce newcomers and experienced programmers alike to -->
<!-- the beauty of functional programming, starting with the simplest building -->
<!-- blocks of software. You’ll need a computer, basic proficiency in the -->
<!-- command line, a text editor, and an internet connection. By the end of this -->
<!-- series, you’ll have a thorough command of the Clojure programming -->
<!-- language. -->


# Clojure a partir do zero: Bem vindo

Este guia tem como objetivo introduzir os recém-chegados e programadores
experientes a beleza da programação funcional, começando com os blocos de
construção mais simples de software. Você vai precisar de um computador,
proficiência básica com linha de comando, um editor de texto, e conexão com a
internet. Até o final desta série, você vai ter um comando aprofundado da
linguagem de programação Clojure. (necessita revisao)


<!-- Who is this guide for? -->
<!-- Science, technology, engineering, and mathematics are deeply rewarding -->
<!-- fields, yet few women enter STEM as a career path. Still more are -->
<!-- discouraged by a culture which repeatedly asserts that women lack the -->
<!-- analytic aptitude for writing software, that they are not driven enough to -->
<!-- be successful scientists, that it’s not cool to pursue a passion for -->
<!-- structural engineering. Those few with the talent, encouragement, and -->
<!-- persistence to break in to science and tech are discouraged by persistent -->
<!-- sexism in practice: the old boy’s club of tenure, being passed over for -->
<!-- promotions, isolation from peers, and flat-out assault. This landscape -->
<!-- sucks. I want to help change it. -->


# Para quem é este guia ?

Ciência, tecnologia, engenharia e matemática são campos profundamente
gratificantes, mas poucas mulheres entram STEM (1) como um plano de
carreira. Ainda mais são desencorajados por uma cultura que repetidamente afirma
que as mulheres não têm a aptidão analítica para escrever software, que eles não
são movidos o suficiente para ser cientistas de sucesso, isso não é legal para
perseguir uma paixão para a engenharia estrutural. Os poucos com o talento,
encorajamento e persistência para quebrar em ciência e tecnologia são
desencorajados pelo sexismo persistente na prática: clube do velho menino de
posse, sendo preterido para promoções, o isolamento de seus pares, e flat-out
assault. Este cenário é uma merda. Eu quero ajudar a mudá-lo. (necessita
revisao)


(1) http://en.wikipedia.org/wiki/STEM_fields

<!-- Women Who Code, PyLadies, Black Girls Code, RailsBridge, Girls Who Code, -->
<!-- Girl Develop It, and Lambda Ladies are just a few of the fantastic groups -->
<!-- helping women enter and thrive in software. I wholeheartedly support these -->
<!-- efforts -->

Women Who Code, PyLadies, Black Girls Code, RailsBridge, Girls Who Code, Girl
Develop It, e Lambda Ladies são apenas alguns de muitos grupos fantásticos que
vem ajudando mulheres a entrar e proposerar em software. Eu sinceramente apoiar
estes esforços. (necessita revisao, e adicao dos links para os grupos
referenciados).

<!-- In addition, I want to help in my little corner of the technical -->
<!-- community–functional programming and distributed systems–by making high-quality -->
<!-- educational resources available for free. The Jepsen series has been, in part, -->
<!-- an effort to share my enthusiasm for distributed systems with beginners of all -->
<!-- stripes–but especially for women, LGBT folks, and people of color. -->


Além disso, eu quero ajudar no meu cantinho da programação funcional na
comunidade técnica e sistemas distribuídos por-fazer dos recursos educacionais
de alta qualidade disponíveis gratuitamente. A série Jepsen tem sido, em parte,
um esforço para compartilhar o meu entusiasmo em sistemas distribuídos com
iniciantes de todas as faixas, mas especialmente para as mulheres, pessoas LGBT,
e pessoas de cor. (necessita revisao e adicao de links referenciados. P.S
"people of color?" hã?)

<!-- As technical authors, we often assume that our readers are white, that our -->
<!-- readers are straight, that our readers are traditionally male. This is the -->
<!-- invisible default in US culture, and it’s especially true in tech. People -->
<!-- continue to assume on the basis of my software and writing that I’m straight, -->
<!-- because well hey, it’s a statistically reasonable assumption. -->

Como autores técnicos, que muitas vezes assumem que nossos leitores são brancos,
que os nossos leitores *straight*  são retas, que nossos leitores são tradicionalmente
masculino. Este é o padrão invisível na cultura dos Estados Unidos, e é
especialmente verdadeiro em tecnologia. As pessoas continuam a assumir com base
no meu software e escrita que eu sou hetero, porque bem hey, é uma suposição
razoável estatisticamente. (necessita revisao)

<!-- But I’m not straight. I get called faggot, cocksucker, and sinner. People say -->
<!-- they’ll pray for me. When I walk hand-in-hand with my boyfriend, people roll -->
<!-- down their car windows and stare. They threaten to beat me up or kill me. Every -->
<!-- day I’m aware that I’m the only gay person some people know, and that I can show -->
<!-- that not all gay people are effeminate, or hypermasculine, or ditzy, or obsessed -->
<!-- with image. That you can be a manicurist or a mathematician or both. Being -->
<!-- different, being a stranger in your culture, comes with all kinds of -->
<!-- challenges. I can’t speak to everyone’s experience, but I can take a pretty good -->
<!-- guess. -->

Mas eu não sou hetero. Sou chamado viado, filho da puta, e pecador. As pessoas
dizem que vão orar por mim. Quando eu ando de mãos dadas com meu namorado,
pessoas baixam suas janelas do carro e olham fixamente. Eles ameaçam
me bater ou me mata. Todos os dias eu estou ciente de que eu sou a única pessoa
gay algumas pessoas sabem, e que eu possa mostrar que nem todos os gays são
afeminados, ou hipermasculina, ou tolos, ou obcecado com a imagem. Que você pode
ser uma manicure ou um matemático ou ambos. Ser diferente, sendo um estranho em
sua cultura, vem com todos os tipos de desafios. Eu não posso falar com a
experiência de todos, mas eu posso tomar um bom palpite. (necessita reviso)

<!-- At the same time, in the technical community I’ve found overwhelming warmth and -->
<!-- support, from people of all stripes. My peers stand up for me every day, and I’m -->
<!-- so thankful–especially you straight dudes–for understanding a bit of what it’s -->
<!-- like to be different. I want to extend that same understanding, that same -->
<!-- empathy, to people unlike myself. Moreover, I want to reassure everyone that -->
<!-- though they may feel different, they do have a place in this community. -->

Ao mesmo tempo, na comunidade técnica que eu encontrei calor avassalador e
apoio, de pessoas de todas as faixas. Meus colegas ficam em pé para mim todos os dias,
e eu sou muito grato, especialmente vocês, caras-de retas entender um pouco de
como é ser diferente. Eu quero estender esse mesmo entendimento, essa mesma
empatia com as pessoas diferentes de mim. Além disso, quero tranquilizar todos
que, embora possam se sentir diferentes, eles têm um lugar nesta
comunidade. (necessita revisao)

<!-- So before we begin, I want to reinforce that you can program, that you can do -->
<!-- math, that you can design car suspensions and fire suppression systems and -->
<!-- spacecraft control software and distributed databases, regardless of what your -->
<!-- classmates and media and even fellow engineers think. You don’t have to be -->
<!-- white, you don’t have to be straight, you don’t have to be a man. You can grow -->
<!-- up never having touched a computer and still become a skilled programmer. Yeah, -->
<!-- it’s harder–and yeah, people will give you shit, but that’s not your fault and -->
<!-- has nothing to do with your ability or your right to do what you love. All it -->
<!-- takes to be a good engineer, scientist, or mathematician is your curiosity, your -->
<!-- passion, the right teaching material, and putting in the hours. -->

Então, antes de começar, quero reforçar que você pode programar, que você pode
fazer matemática, que você pode projetar as suspensões de automóveis e sistemas
de extinção de incêndios e software de controle de naves espaciais e bancos de
dados distribuídos, independentemente do que seus colegas de classe e meios de
comunicação e até mesmo colegas engenheiros pensar. Você não tem que ser
branco, você não tem que ser em linha reta, você não tem que ser um homem. Você
pode crescer sem nunca ter tocado em um computador e ainda se tornar um
programador habilidoso. Sim, é mais difícil e, sim, as pessoas vão te dar merda,
mas isso não é culpa sua e não tem nada a ver com sua capacidade ou seu direito
de fazer o que você ama. Tudo o que é preciso para ser um bom engenheiro,
cientista ou matemático é a sua curiosidade, a sua paixão, o material didático
direito, e horas práticando tudo isso. (necessita revisao)

<!-- There’s nothing in this guide that’s just for lesbian grandmas or just for -->
<!-- mixed-race kids; bros, you’re welcome here too. There’s nothing dumbed -->
<!-- down. We’re gonna go as deep into the ideas of programming as I know how to go, -->
<!-- and we’re gonna do it with everyone on board. -->

Não há nada neste guia que é apenas para avós lésbicas ou apenas para mestiços
filhos; cara, você é bem-vindo aqui também. Não há nada de bobos. Nós vamos ir
tão fundo nas idéias de programação como eu sei como ir, e nós vamos fazê-lo com
todos a bordo.

<!-- No matter who you are or who people think you are, this guide is for -->
<!-- you. -->

Não importa quem você é ou o que as pessoas pensam que você é, este guia é para você.
