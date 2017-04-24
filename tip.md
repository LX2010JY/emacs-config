#1. 第一步，添加一个插件库的网址，这样 通过 alt+x   list-package 可以获得近4000个插件，可直接 package-install 下载
(require 'package)  
(setq package-archives  
      '(("gnu" . "http://elpa.gnu.org/packages/")  
        ;;("marmalade" . "http://marmalade-repo.org/packages/")  
        ("melpa" . "http://melpa.milkbox.net/packages/")))  
(package-initialize) 
# 在这里第一个下载的插件为 package-install [ret] elpy-enable [ret] 这是用于 python补全的插件 ctrl + c ctrl +c 可执行py文件
# 需要pip安装一些python模块，具体 忘了 
(elpy-enable)

#2. 第二步，安装主题插件
(add-to-list 'load-path "C:/Users/yuan/AppData/Roaming/.emacs.d/color/")
(require 'color-theme)
;;(color-theme-initialize) ;;选择配色方案
;;(color-theme-classic)

;;添加molokai主题
(add-to-list 'custom-theme-load-path "C:/Users/yuan/AppData/Roaming/.emacs.d/color/themes/")
(load-theme 'molokai t);;使用第三方配色 必须加的部分，使得打开emacs自动加载主题配色
(setq molokai-theme-kit t)



#第三步，安装auto-complete,总共两个插件 auto-complete和popup
;;使用auto-complete
(add-to-list 'load-path "C:/Users/yuan/AppData/Roaming/.emacs.d/auto-complete")
(add-to-list 'load-path "C:/Users/yuan/AppData/Roaming/.emacs.d/popup")
(require 'auto-complete-config)
(add-to-list 'ac-dictionary-directories "C:/Users/yuan/AppData/Roaming/.emacs.d/auto-complete/dict")
(ac-config-default)

(require 'popup)
(setq ac-quick-help-prefer-pos-tip t)

;;去掉欢迎界面
(setq inhibit-startup-message t)
(setq gnus-inhibit-startup-message t)

;;显示行数
(global-linum-mode t)
(column-number-mode t)

;;去掉工具栏
(tool-bar-mode 0)
;;(menu-bar-mode 0)

;;helm添加，缺少 autoload 

(add-to-list 'load-path "C:/Users/yuan/AppData/Roaming/.emacs.d/helm/")
;;(require 'helm-config)
;;(helm-mode 1)


;;修改光标形状 bar为竖线 box为方块
(setq-default cursor-type 'bar)


