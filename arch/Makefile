package: link
	@makepkg -sr

install: link
	@makepkg -sri

link: ../fl
	@if [ ! -f fl ]; then ln -s ../fl; fi

clean:
	@rm -rf pkg src
	@for file in fancylists*.tar.xz fl; do\
		if [ -f $$file ]; then rm $$file; fi; done
