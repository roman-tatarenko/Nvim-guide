Файл описує як налаштувати редактор nvim
в якості IDE для Python.
========================

Теорія: nvim використовує lsp by Microsoft LLC - 
	language server protocol.
	Тобто це технологія, яка і дозволяє писати на python
	в nvim.
	Редактор коду через lsp-протокол викликає сервер.
	Для того щоб все працювало, nvim повинен бути версії
	v. >= 0.5.1 

Встановлення nvim для MAC на процесорі m1:
	brew install nvim

Встановлення lsp-сервера для Python:
	цих серверів є багато, використовуємо pyright
	для того щоб встановити pyright потрібно встановити
	- zshrc-оболонку;
	- node.js;
	- nvm - nvm is a version manager for node.js,
		designed to be installed per-user, and invoked per-shell;
	- npm;

	Використовуй ці команди:
	curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
	source .zshrc
	nvm install node
	nvm use node
	node -v
	npm -v
	npm install -g pyright
	pyright --version

Створюємо директорію, в якій буде зберігатися конфіг для nvim.
	
	Викорстовуй ці команди:
	cd ~
	mkdir -p ~/.config/nvim/
	nvim ~/.config/nvim/init.vim

В якості менеджера плагінів будемо використовувати vim-plug
	
	Використовуй цю команду з розділі Instll for Neovim, з оф. репозиторію github:
	sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'

	Доступні плагіни описані в репозиторії.

У файл з конфігом напишемо:
	

# nvim-config
