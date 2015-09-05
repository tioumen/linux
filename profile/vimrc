" VIM Configuration
"thanks @willdurand and @fabienpomerol

runtime bundle/pathogen/autoload/pathogen.vim
call pathogen#infect()
call pathogen#helptags()

"""""""""""""""""""""
" General
"""""""""""""""""""""

" not compatible with VI 
set nocompatible

" Enable filetype plugins
filetype on
filetype plugin on
filetype indent on

" Set to auto read when a file is changed from the outside
set autoread

" With a map leader it's possible to do extra key combinations
" like <leader>w saves the current file
let mapleader = ","
let g:mapleader = ","

" Fast saving
nmap <leader>w :w!<CR>

"""""""""""""""""""""
" VIM user interface
"""""""""""""""""""""

" line numbers
set number

set laststatus=2
set showcmd                         " Display incomplete commands
set ruler                           " Show cursor position
set langmenu=en_US.UTF-8
set lazyredraw                      " make plugins smoother


" Turn on the WiLd menu
set wildmenu

"Always show current position
set ruler

" Show trailing whitespace:
:set list listchars=tab:>-,trail:.,extends:>

" A buffer becomes hidden when it is abandoned
set hid

" Configure backspace so it acts as it should act
set backspace=eol,start,indent
set whichwrap+=<,>,h,l

" Ignore case when searching
set ignorecase

" When searching try to be smart about cases 
set smartcase

" Highlight search results
set hlsearch

" Makes search act like search in modern browsers
set incsearch

" Don't redraw while executing maCRos (good performance config)
set lazyredraw

" For regular expressions turn magic on
set magic

" Show matching brackets when text indicator is over them
set showmatch
" How many tenths of a second to blink when matching brackets
set mat=2

" No annoying sound on errors
set noerrorbells
set novisualbell
set t_vb=
set tm=500


"""""""""""""""""""""
" Color and font 
"""""""""""""""""""""

" Enable syntax highlighting
syntax enable

" set guifont=Consolas:h12 for windows
set guifont=Monaco\ for\ Powerline "for mvim, for vim siwth the Terminal font itself

" set background=dark

" Set extra options when running in GUI mode
if has("gui_running")
    set guioptions-=T
    set guioptions+=e
    set t_Co=256
    set guitablabel=%M\ %t
endif

" Set utf8 as standard encoding and en_US as the standard language
set encoding=utf8

" Use Unix as the standard file type
set ffs=unix,dos,mac

"""""""""""""""""""""
" Files, backups and undo
"""""""""""""""""""""
" Turn backup off, since most stuff is in SVN, git et.c anyway...
set nobackup
set nowb
set noswapfile


"""""""""""""""""""""
" Text, tab and indent related
"""""""""""""""""""""

" Use spaces instead of tabs
set expandtab

" Be smart when using tabs ;)
set smarttab

" 1 tab == 2 spaces
set shiftwidth=2
set tabstop=2

" Linebreak on 500 characters
set lbr
set tw=500

set ai "Auto indent
set si "Smart indent
set wrap "Wrap lines

"""""""""""""""""""""
" Moving around, tabs, windows and buffers
"""""""""""""""""""""

" Map <Space> to / (search) and Ctrl-<Space> to ? (backwards search)
map <space> /
map <c-space> ?

" Disable highlight when <leader><CR> is pressed
map <silent> <leader><CR> :noh<CR>

" Explore next/previous buffers
nnoremap <tab> :bn<CR>
nnoremap <S-tab> :bp<CR>


"""""""""""""""""""""
" Spell checking
"""""""""""""""""""""
" Pressing ,ss will toggle and untoggle spell checking
map <leader>ss :setlocal spell!<CR>

" Shortcuts using <leader>
map <leader>sn ]s
map <leader>sp [s
map <leader>sa zg
map <leader>s? z=


"""""""""""""""""""""
" Misc
"""""""""""""""""""""
" Remove the Windows ^M - when the encodings gets messed up
noremap <Leader>m mmHmt:%s/<C-V><CR>//ge<CR>'tzt'm


"""""""""""""""""""""
" Plugin 
"""""""""""""""""""""

"Bbye
:nnoremap <Leader>q :Bdelete<CR>
:nnoremap <Leader>q! :Bdelete!<CR>
" Airline`
au VimEnter * AirlineTheme solarized
" let g:airline_theme = 'solarized' the above line replace this one in Windows

let g:airline#extensions#tabline#enabled = 1
let g:airline_powerline_fonts = 1
let g:airline_solarized_bg = 'light'
set noshowmode

" Syntastic
set statusline+=%#warningmsg#
set statusline+=%{SyntasticStatuslineFlag()}
set statusline+=%*

let g:syntastic_always_populate_loc_list = 1
let g:syntastic_auto_loc_list = 1
let g:syntastic_check_on_open = 1
let g:syntastic_check_on_wq = 0

" GitGutter
let g:gitgutter_sign_column_always = 1
" see: https://github.com/airblade/vim-gitgutter#faq
highlight SignColumn        ctermbg=235
highlight GitGutterAdd      guifg=#009900 guibg=NONE ctermfg=2 ctermbg=235
highlight GitGutterChange   guifg=#bbbb00 guibg=NONE ctermfg=3 ctermbg=235
highlight GitGutterDelete   guifg=#ff2222 guibg=NONE ctermfg=1 ctermbg=235
set encoding=utf-8

" NERDTree
noremap <leader>n :NERDTreeToggle<CR>

autocmd vimenter * if !argc() | NERDTree | endif
autocmd bufenter * if (winnr("$") == 1 && exists("b:NERDTreeType") && b:NERDTreeType == "primary") | q | endif
