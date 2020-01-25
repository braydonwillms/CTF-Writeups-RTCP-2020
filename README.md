# CTF-Writeups-RTCP-2020
# Misc
## Strong Password - 1
Eat, Drink, Pet, Hug, Repeat!

flags are entered in the format rtcp{flag}

We basically just have to guess here.
flag: rtcp{rice_tea_cat_panda}

## Off-Topic - 5
off-topic

The discord off-topic channel description asks for the name of the catpanda in the server picture. If we look at the picture's alt text on the webpage, the name is "Jubie".
flag: rtcp{Jubie}

## A Friend In Need Is A Friend Indeed - 50
Hm, I see a lot of potential friends in the midst of that discord, but... one is not like the others; maybe I'll slide into their dms and strike up a conversation about passwords!

If we dm the Jade bot in the discord server with the flag for the first challenge, it gives us this one.
flag: rtcp{awaken_winged_sun_dragon_of_ra}

## Survey! - 100
Wew a survey!!! Free points are always nice :3

Complete the survey, or if that's too simple find the flag in the survey page's source code.
flag: rtcp{th^nk5_f0r_p14y1ng}

# Forensics
## BTS-Crazed - 75
My friend made this cool remix, and it's pretty good, but everyone says there's a deeper meaning in the music. To be honest, I can't really tell - the second drop's 808s are just too epic.

We're given an mp3 file. If we use strings on the file, we find the flag in it.
flag: rtcp{j^cks0n_3ats_r1c3}

## Allergic College Application - 100
I was writing my common app essay in Mandarin when my cat got on my lap and sneezed. Being allergic, I sneezed with him, and when I blew my nose into a tissue, the text for my essay turned really weird! Get out, Bad Kitty!

We're given a text file that seems to be garbage. However, some text editors seem to be able to read it. If we look at the github repo for the ctf, it appears as Chinese.
flag: rtcp{我_只_修改_了_两_次}

## cat-chat - 125
nyameowmeow nyameow nyanya meow purr nyameowmeow nyameow nyanya meow purr nyameowmeow nyanyanyanya nyameow meow purr meow nyanyanyanya nya purr nyanyanyanya nya meownyameownya meownyameow purr nyanya nyanyanya purr meowmeownya meowmeowmeow nyanya meownya meowmeownya purr meowmeowmeow meownya purr nyanyanyanya nya nyameownya nya !!!!

It turns out this is actually morse code. The hint tells us to check the cat-chat channel on the discord, so I encoded rtcp to nyameownya meow meownyameownya nyameowmeownya and found the matching message in the channel. After that, it's just a matter of decoding it.
flag: rtcp{th15_1z_a_c4t_ch4t_n0t_a_m3m3_ch4t}

# Binary/Excecutable
## print(f) to Pay Respects - 100
Lulu recently began to collect rice granules, she needs so many! (like over 9999) Jake says it might be a cure to Lulu's disease. Go help her get enough by throwing rice at the portal, print(f) to pay respects.

There are some program files given here. They turned out to be a pain to set up, so I just used cutter and was able to find the flag in the strings extracted from the dll file.
flag: rtcp{s0m3t1m35_0n1y_s0m3tImEz_sn^k3z_ar3_u5EfuL}

# Web
## Robots. Yeah, I know, pretty obvious. - 25
So, we know that Delphine is a cook. A wonderful one, at that. But did you know that GIANt used to make robots? Yeah, GIANt robots.

We check the robots.txt file of the page and find 2 disallowed files. We get rickrolled by the file named "flag", then find the flag in the other file, "robot-nurses"
flag: rtcp{r0b0t5_4r3_g01ng_t0_t4k3_0v3r_4nd_w3_4r3_s0_scr3w3d}

## No Sleep - 100
Jess doesn't get enough sleep, since he's such a gamer so in this challenge, you'll be staying up with him until 4:00 in the morning :D on a Monday! Let's go, gamers!

We go to the website and find a countdown timer, and a cookie named "gamerfuel" that seems to contain the date and time it's counting down too. Editing this cookie to contain the current time reveals the flag.
flag: rtcp{w0w_d1d_u_st4y_up?}

## Phishing for Flags - 105
I got a bunch of emails from people across the galaxy... some are more interesting than others.

We get a bunch of apparent phishing emails to look through. Most of the links in them don't exist, but we find one for riceteacatpanda.wtf/phishingemail that does. We find the flag here.
flag: rtcp{r34d_b3f0rE_yOU_C1iCk}

## Uwu? - 125
ᵘʷᵘ oh no ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ hecc sorry guys ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ sorry im dropping ᵘʷᵘ my uwus all over the ᵘʷᵘ place ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ oh no I lost one ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ ᵘʷᵘ

ah, Jake, you idiot

If we follow the link listed, it quickly flips through a series of pages with a bunch of text on them. I simply watched the page names and sent GET requests to each one so I could take as long as needed to look through them.
flag: rtcp{uwu_,_1_f0und_y0u}

## What's in The Box?! - 200

The problem contains a box image that, when clicked, call a javascript function spawnCat. This places a cat gif in the browser window. If we take a look at the gif, the flag is split into pieces throughout the file.
flag: rtcp{k4wA1I_kitT3nz_4_tH3_w1N!!_41232345}

## growls at the chicken - 1000
grrrrrrR
big chicken, i hisS At you!!!

This one was pretty fun. Given in the problem are an RSA public key, private key, and message. That's straighforward enough, so we decrypt this and get "unknown-123-246-470-726.herokuapp.com" as the message. Going to this URL, we find a page with some talk about a drawer in the console and two strings hidden in the html: "9 20 30 15 16 5 14 19 30 27 29 8 20 13 12 28" and "abcdefghijklmnopqrstuvwxyz[]. ". If we look at the characters in the second string based on the indices in the first, we get the message "it opens [.html]". From this, I took a guess and tried opening drawer.html, which held the flag.
flag: rtcp{ch1ck3n_4nd_th3_3gg}

# General Skills
## Come Eat Grandma - 25
Oh, my bad, this spreadsheet appears to be missing its commas.

There is a link to a slightly chaotic google spreadsheet that everyone can edit. It turns out the flag is in an older version of the sheet.
flag: rtcp{D0n't_E^t_Gr4NDmA_734252}

## Basic C4 - 30
If you use that bomb, you might cause an Avalanche...
Let's not destroy my IO, ok?

After a bit of digging, I found that C4 is an algorithm that calculates an sha512 hash and encodes it in base 58. We just need to do this with the given text file and submit that.
flag: rtcp{c42CW3TbiGhvptM36RJJ9ScctgkskjvZPo6dG8JexzZRvzQR6hwovZJLDkYK5pZ6cq9e7fX1ShUiYUdM7H1Uuqj64G}

## Sticks and Stones - 50
may break my bones but words could never hurt me

There is a link to a massive text file here. Using ctrl-f and searching for rtcp proves useless, as there are thousands of hits. However, if we search for an underscore, it turns out only the real flag conatins any.
flag: rtcp{w0Rd5_HuRt_,_d0n'T_Bu11y_,_k1Dz}

## Types of Rice and Cookies, Because Those Definitely Go Together Well - 100
It's important to know all the different kinds of rice. After all, what kind of cook would Delphine be if she couldn't identify the different types? But GIANt needs to learn too. So Delphine is having him research different kinds of cookies. She wants him to find the cookie that help websites remember her information and settings when she visit them in the future. Creepy? Yes. Important? Also yes.

Just answer the question.
flag: rtcp{persistent_cookies}

## Grandma's Recipes - 100
So Delphine and the GIANt wanted to make a recipe that Delphine's grandma passed down to her. The problem is, her grandma is extremely tech-savvy. In fact, she likes using a Certain Website on the endless Inter-Webs. She says it's very useful for storing her recipes. It'll be kinda hard for Delphine and the GIANt to git her recipes though; they don't know her username. Oh well. But hey, they know that she likes naming things after the Holy Rice Goddess.

I wonder what recipe Delphine and GIANt are making. . .

We have to search for "holy rice goddess" on github, and find a repository containing the flag.
flag: rtcp{ju5t_l1k3_gr4ndm45_m34tl04f_1029837} 

## pandamonium - 100
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
91 7 10 D 95 42 28 A 

This is a bit of an obscure cipher. "amonium" in the title seems to be a hint, but I just figured it out by searching with the form of the ciphertext - it turns out this is a periodic table cipher.
flag: rtcp{PANNED_AMMONIA}

# Cryptography
## HOOOOOOOOOOMEEEEEE RUNNNNNNNNNNNNN!!!!! - 50
AND JAKE IS ROUNDING THE BASES
HE PASSES BASE 32!!!
HE ROUNDS BASE 64!!!!!!!
WE'RE WITNESSING A MIRACLE!!!!!!!!!!!!!

Just one more base to go ;D

We get a string that turns out to be encoded in base 85. We decode it to get the flag.
flag: rtcp{uH_JAk3_w3REn't_y0u_4t_Th3_uWust0r4g3}

## Don't Give The GIANt a COOKie - 100
It was just a typical day in the bakery for Delphine. She was preparing her famous chocolate cake, when all of a sudden a GIANt burst through the doors of her establishment and demanded a cookie. Being the strong-willed girl she was, Delphine refused and promptly threw her rolling pin at the GIANt. Doing what any sensible being would do when faced with projectiles, the GIANt let out a shriek and ran out of the shop. Delphine smiled to herself, it was another day well done.

But oh? What's this? It seems the GIANt dropped this behind while he was screaming and scrambling out of the shop.

69acad26c0b7fa29d2df023b4744bf07

The value given is an md5 hash. We can just use an online hash cracker to find the flag.
flag: rtcp{chocolate_mmm}

## 15 - 100
Lhzdwt eceowwl: Dhtnwt Pcln Eaao Qwoohvw

Okw qsyo okcln bah'i fslo cl baht Dhtnwt Pcln dhtnwt cy yazwalw'y eaao ehlnhy. Dho sy co ohtly aho, okso zcnko dw fkso bah nwo. S 4vksllwt hmqasiwi s mkaoa slalbzahyqb oa okw ycow ykafvsycln kcy ewwo cl s mqsyocv dcl ae qwoohvw, fcok okw yosowzwlo: "Okcy cy okw qwoohvw bah wso so Dhtnwt Pcln." Sizcoowiqb, kw ksi ykawy al. Dho okso'y wgwl fatyw.

Okw mayo fwlo qcgw so 11:38 MZ al Xhqb 16, sli s zwtw ofwlob zclhowy qsowt, okw Dhtnwt Pcln cl rhwyocal fsy sqwtowi oa okw tanhw wzmqabww. So qwsyo, C kamw kw'y tanhw. Kaf ici co ksmmwl? Fwqq, okw DP wzmqabww ksil'o twzagwi okw WJCE isos etaz okw hmqasiwi mkaoa, fkcvk yhnnwyowi okw vhqmtco fsy yazwfkwtw cl Zsbecwqi Kwcnkoy, Akca. Okcy fsy so 11:47. Oktww zclhowy qsowt so 11:50, okw Dhtnwt Pcln dtslvk siitwyy fsy mayowi fcok fcykwy ae ksmmb hlwzmqabzwlo. Ecgw zclhowy qsowt, okw lwfy yosocal fsy valosvowi db slaokwt 4vksllwt. Sli oktww zclhowy qsowt, so 11:58, s qclp fsy mayowi: DP'y "Owqq hy sdaho hy" alqclw eathz. Okw eaao mkaoa, aokwtfcyw plafl sy wjkcdco S, fsy soosvkwi. Vqwgwqsli Yvwlw Zsnsuclw valosvowi okw DP cl rhwyocal okw lwjo isb. Fkwl rhwyocalwi, okw dtwspesyo ykceo zslsnwt ysci "Ak, C plaf fka okso cy. Kw'y nwoocln ectwi." Zbyowtb yaqgwi, db 4vksl. Laf fw vsl sqq na dsvp oa wsocln aht esyo eaai cl mwsvw.

tovm{v4T3Ehq_f1oK_3J1e_i4O4}

With this much text, it's likely to be a substitution cipher, and that turns out to be correct. An online decoder can easily solve it.
flag: RTCP{c4R3Ful_w1tH_3X1f_d4T4}

## notice me senpai - 100
uwu...senpai placed this note on my desk before class but i cant wead what it says!!!!!! can you hewp me????????? uwu tysm

tlyrc_o_0pnvhu}{137rmi__i_omwm

Looking at this, it seems like it might be some sort of transposition cipher. It turns out to be a rail fence cipher, and the amount of punctuation is a hint about the key. I couldn't quite get it to work, but decrypting with a key of 6 gave me trp{im_1ncl_v3_wi7hoy_ur_mom}0. This was close enough that I managed to rearrange the last few characters.
flag: rtcp{im_1n_lov3_wi7h_y0ur_mom}

## Wrong Way - 150
Did you know that you've been going the wrong way entire time?

E7Rq<G:Kǒ

From the hint, perhaps we need to encrypt this rather than decrypt it... It turns out that we get the flag by encoding the string in base 64.
flag: rtcp{UnEXPEcTED_pLAceS}

## That's Some Interesting Tea(rs)....... - 175
You know, the tears of one's enemies works lovely in tea. Turns out, there's tons of different bases for tea. In fact, I think I heard Delphine talk about this chef website she used for her tea base combinations. . .

Oh! Speaking of which, GIANt wants Delphine to make him tea. . . all he has is the tea leaves and the cup though. Maybe you can help Delphine, since she's really busy with cooking other things?

O53GG4CSJRHEWQT2GJ5HC4CGOM4VKY3SOZGECZ2YNJTXO6LROV3DIR3CK4ZEMWCDHFMTOWSXGRSHU23DLJVTS5BXOQZXMU3ONJSFKRCVO5BEGVSELJSGUNSYLI2XQ32UOI3FKWDYMJQWOMKQOJ4XIU2WN5KTKWT2INUW44SZONGUUN2BMFRTQQJYKM3WGSSUNVXGEU3THFIFUSDHIVWVEQ3LJVUXEMSXK5MXSZ3TG5JXORKTMZRFIVQ=

The problem seems to suggest we should try using cyberchef to repeatedly decrypt from different bases. It turns out that decoding from base 32, then base 58, then base 62, then base 64, and finally base 85 reveals the flag.
flag: rtcp{th4t5_50m3_54lty_t34_1_bl4m3_4ll_th0s3_t34rs}

## Pandas Like Salads - 350
Did you know a new panda was added to the Washington DC zoo recently? Yep, apparently she really like salads. Interesting, yeah? Also, the panda keepers of the zoo said that the key to happiness in life is a little CUTENESS every day. You know, all the keepers who are on the panda's rotation all said the same thing to me. Very interesting.

This one takes a few layers of decryption. To start, we're given a picture of a flag encoded in a pigpen cipher. Decoding this, we get ysay{hjkahr_qqgdia_unr_kw_yrq_pm_nnfb}. The references to salad, a keyword, and rotation seem to suggest there might be a caesar or vigenere cipher here. After some experimentation, a caesar shift of 21 followed by decoding with a vigenere cipher with keyword "cuteness" gives us the flag.
flag: rtcp{pandas_should_not_be_put_in_pens}
