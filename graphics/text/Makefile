# textgen outputs these files which are included in the built WADs
# as lumps.
# m_pause.png is intentionally omitted.
TEXTGEN_GRAPHIC_LUMPS = \
  m_detail.png m_disopt.png m_disp.png   m_endgam.png m_epid.png m_epix.png\
  m_epi1.png   m_epi2.png   m_epi3.png   m_epi4.png   m_episod.png m_gdhigh.png \
  m_gdlow.png  m_hurt.png   m_jkill.png  m_lgttl.png  m_loadg.png  \
  m_messg.png  m_msens.png  m_msgoff.png m_msgon.png  m_musvol.png \
  m_newg.png   m_ngame.png  m_nmare.png  m_option.png m_optttl.png \
  m_quitg.png  m_rdthis.png m_rough.png  m_saveg.png  \
  m_scrnsz.png m_sfxvol.png m_sgttl.png  m_skill.png  m_svol.png   \
  m_about.png  m_accel.png  m_auto.png   m_chat.png   m_chatm.png  \
  m_compat.png m_demos.png  m_dmflag.png m_enem.png   m_etcopt.png \
  m_feat.png   m_generl.png m_gset.png   m_horsen.png m_hud.png    \
  m_joyset.png m_keybnd.png m_ldsv.png   m_loksen.png m_menus.png  \
  m_mess.png   m_mouse.png  m_multi.png  m_player.png m_serial.png \
  m_setup.png  m_sound.png  m_stat.png   m_status.png m_tcpip.png  \
  m_versen.png m_video.png  m_wad.png    m_wadopt.png m_weap.png   \
  m_crispy.png                                                     \
  prboom.png   t_fdemo.png  t_phase1.png t_phase2.png              \
  m_ultra.png  wibp1.png    wibp2.png    wibp3.png    wibp4.png    \
  wicolon.png  wienter.png  wif.png      wifrgs.png   wipcnt.png   \
  wiminus.png  wimstar.png  wimstt.png   wiostf.png   wiosti.png   \
  wiostk.png   wiosts.png   wiscrt2.png  wisucks.png  witime.png   \
  wip1.png     wip2.png     wip3.png     wip4.png     wipar.png    \
  winum0.png   winum1.png   winum2.png   winum3.png   winum4.png   \
  winum5.png   winum6.png   winum7.png   winum8.png   winum9.png   \
  dmwilv00.png dmwilv01.png dmwilv02.png dmwilv03.png dmwilv04.png \
  dmwilv05.png dmwilv06.png dmwilv07.png dmwilv08.png dmwilv09.png \
  dmwilv10.png dmwilv11.png dmwilv12.png dmwilv13.png dmwilv14.png \
  dmwilv15.png dmwilv16.png dmwilv17.png dmwilv18.png dmwilv19.png \
  dmwilv20.png dmwilv21.png dmwilv22.png dmwilv23.png dmwilv24.png \
  dmwilv25.png dmwilv26.png dmwilv27.png dmwilv28.png dmwilv29.png \
  dmwilv30.png dmwilv31.png                                        \
  cwilv00.png  cwilv01.png  cwilv02.png  cwilv03.png  cwilv04.png  \
  cwilv05.png  cwilv06.png  cwilv07.png  cwilv08.png  cwilv09.png  \
  cwilv10.png  cwilv11.png  cwilv12.png  cwilv13.png  cwilv14.png  \
  cwilv15.png  cwilv16.png  cwilv17.png  cwilv18.png  cwilv19.png  \
  cwilv20.png  cwilv21.png  cwilv22.png  cwilv23.png  cwilv24.png  \
  cwilv25.png  cwilv26.png  cwilv27.png  cwilv28.png  cwilv29.png  \
  cwilv30.png  cwilv31.png                                         \
  wilv00.png   wilv01.png   wilv02.png   wilv03.png   wilv04.png   \
  wilv05.png   wilv06.png   wilv07.png   wilv08.png   wilv10.png   \
  wilv11.png   wilv12.png   wilv13.png   wilv14.png   wilv15.png   \
  wilv16.png   wilv17.png   wilv18.png   wilv20.png   wilv21.png   \
  wilv22.png   wilv23.png   wilv24.png   wilv25.png   wilv26.png   \
  wilv27.png   wilv28.png   wilv30.png   wilv31.png   wilv32.png   \
  wilv33.png   wilv34.png   wilv35.png   wilv36.png   wilv37.png   \
  wilv38.png

# The full set of graphics outputted by textgen includes a couple of
# extra files that are just intermediates, and are not lumps to be
# incuded in the WADs:
TEXTGEN_GRAPHICS = $(TEXTGEN_GRAPHIC_LUMPS)                                \
  helpttl.png  freettl.png

all: text_strings help.png credit.png wikilrs.png wivctms.png titlepic

# Generate the menu and level strings
text_strings: config.py fontchars ../../lumps/dehacked/dehacked.txt
	./textgen
	cp $(TEXTGEN_GRAPHIC_LUMPS) ../

# Background for the help screen is a color shifted version of INTERPIC:
helpbg.png: ../interpic.png
	./tint.py ../interpic.png '#777777' helpbg.png

# Generate transparent image containing text for the HELP screen:
help.png: text_strings helpbg.png
	./smtextgen help.png 320x200                 \
	   -background "helpbg.png"                  \
	   2,2   "file:helpttl.png"                  \
	   10,22   "Weapons"                         \
	   26,34   "file:../../sprites/csawa0.png"   \
	   90,26   "file:../../sprites/shota0.png"   \
	   92,41   "file:../../sprites/sgn2a0.png"   \
	   150,18  "file:../../sprites/mguna0.png"   \
	   161,40  "file:../../sprites/launa0.png"   \
	   230,22  "file:../../sprites/plasa0.png"   \
	   240,35  "file:../../sprites/bfuga0.png"   \
	   10,61   "Backpack"                      \
	   26,70  "file:../../sprites/bpaka0.png"   \
	   90,61   "Ammo"                            \
	   105,72   "file:../../sprites/ammoa0.png"   \
	   100,78   "file:../../sprites/clipa0.png"   \
	   140,74  "file:../../sprites/sboxa0.png"   \
	   132,80  "file:../../sprites/shela0.png"   \
	   186,68   "file:../../sprites/broka0.png"   \
	   185,68   "file:../../sprites/rocka0.png"   \
	   260,68  "file:../../sprites/celpa0.png"   \
	   250,79  "file:../../sprites/cella0.png"   \
	   10,109  "Health"                          \
	   63,102  "file:../../sprites/bon1a0.png"   \
	   92,98  "file:../../sprites/media0.png"   \
	   83,114  "file:../../sprites/stima0.png"   \
	   128,101 "file:../../sprites/pstra0.png"   \
	   172,109 "Armour"                          \
	   280,97 "file:../../sprites/arm2a0.png"   \
	   242,94 "file:../../sprites/arm1a0.png"   \
	   226,101 "file:../../sprites/bon2b0.png"   \
	   145,133 "Map"                             \
	   175,121 "file:../../sprites/pmapa0.png"   \
	   10,133  "Big Boost"                       \
	   84,126  "file:../../sprites/soula0.png"   \
	   110,126 "file:../../sprites/megaa0.png"   \
	   10,154  "Light"                           \
	   48,151  "file:../../sprites/pvisa0.png"   \
	   34,176  "Cloak"                           \
	   80,160  "file:../../sprites/pinsa0.png"   \
	   119,176 "Invuln."                         \
	   174,165 "file:../../sprites/pinva0.png"   \
	   240,125 "Keys"                            \
	   276,125 "file:../../sprites/ykeya0.png"   \
	   290,125 "file:../../sprites/bkeya0.png"   \
	   254,135 "file:../../sprites/rkeya0.png"   \
	   240,181 "Objectives"                      \
	   274,148 "file:../../sprites/yskua0.png"   \
	   296,148 "file:../../sprites/bskua0.png"   \
	   238,158 "file:../../sprites/rskua0.png"   \
	   126,154 "Rescue suit"                     \
	   211,136 "file:../../sprites/suita0.png"   \
	   63,192  "https://libtech1.nfshost.com/"
	cp $@ ../


credit.png: text_strings helpbg.png credit.txt
	./smtextgen credit.png 320x200                \
	   -background "helpbg.png"                   \
	   120,5  "file:freettl.png"                  \
	   10,30  "include:credit.txt"
	cp $@ ../

wikilrs_horiz.png:
	./smtextgen $@ 49x7 \
	    0,0  killers

wikilrs.png: wikilrs_horiz.png
	./rotate wikilrs_horiz.png 270 $@
	cp $@ ../

wivctms.png:
	./smtextgen $@ 54x7 \
	    0,0  victims
	cp $@ ../

titlepic: fd1title.png fd2title.png fdmtitle.png fdotitle.png

fdotitle.png: text_strings ../titlepic/titlepic.png ../empty.png
	./create_caption ../titlepic/titlepic.png ../empty.png ../t_fdemo.png $@
	cp $@ ../

fd1title.png: text_strings ../titlepic/titlepic.png ../empty.png
	./create_caption ../titlepic/titlepic.png ../empty.png ../t_phase1.png $@
	cp $@ ../

fd2title.png: text_strings ../titlepic/titlepic.png ../empty.png
	./create_caption ../titlepic/titlepic.png ../empty.png ../t_phase2.png $@
	cp $@ ../

fdmtitle.png: ../titlepic/freedm_titlepic.png
	./create_caption $< $@
	cp $@ ../

clean:
	$(RM) $(TEXTGEN_GRAPHICS) helpbg.png help.png	            \
	    graphics.stamp *.pyc credtext.png	                    \
	    credtext.png credit.png dmwilv*.png wikilrs.png		    \
	    wivctms.png wikilrs_horiz.png ../credit.png ../help.png	\
	    ../wikilrs.png ../wivctms.png                           \
		fd1title.png fd2title.png fdmtitle.png fdotitle.png     \
	    ../fd1title.png ../fd2title.png ../fdmtitle.png ../fdotitle.png
	for graphic in $(TEXTGEN_GRAPHICS); do $(RM) ../$$graphic; done
	$(RM) __pycache__/*
	-rmdir __pycache__
