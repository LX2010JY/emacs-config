#1. ��һ�������һ����������ַ������ ͨ�� alt+x   list-package ���Ի�ý�4000���������ֱ�� package-install ����
(require 'package)  
(setq package-archives  
      '(("gnu" . "http://elpa.gnu.org/packages/")  
        ;;("marmalade" . "http://marmalade-repo.org/packages/")  
        ("melpa" . "http://melpa.milkbox.net/packages/")))  
(package-initialize) 
# �������һ�����صĲ��Ϊ package-install [ret] elpy-enable [ret] �������� python��ȫ�Ĳ�� ctrl + c ctrl +c ��ִ��py�ļ�
# ��Ҫpip��װһЩpythonģ�飬���� ���� 
(elpy-enable)

#2. �ڶ�������װ������
(add-to-list 'load-path "C:/Users/yuan/AppData/Roaming/.emacs.d/color/")
(require 'color-theme)
;;(color-theme-initialize) ;;ѡ����ɫ����
;;(color-theme-classic)

;;���molokai����
(add-to-list 'custom-theme-load-path "C:/Users/yuan/AppData/Roaming/.emacs.d/color/themes/")
(load-theme 'molokai t);;ʹ�õ�������ɫ ����ӵĲ��֣�ʹ�ô�emacs�Զ�����������ɫ
(setq molokai-theme-kit t)



#����������װauto-complete,�ܹ�������� auto-complete��popup
;;ʹ��auto-complete
(add-to-list 'load-path "C:/Users/yuan/AppData/Roaming/.emacs.d/auto-complete")
(add-to-list 'load-path "C:/Users/yuan/AppData/Roaming/.emacs.d/popup")
(require 'auto-complete-config)
(add-to-list 'ac-dictionary-directories "C:/Users/yuan/AppData/Roaming/.emacs.d/auto-complete/dict")
(ac-config-default)

(require 'popup)
(setq ac-quick-help-prefer-pos-tip t)

;;ȥ����ӭ����
(setq inhibit-startup-message t)
(setq gnus-inhibit-startup-message t)

;;��ʾ����
(global-linum-mode t)
(column-number-mode t)

;;ȥ��������
(tool-bar-mode 0)
;;(menu-bar-mode 0)

;;helm��ӣ�ȱ�� autoload 

(add-to-list 'load-path "C:/Users/yuan/AppData/Roaming/.emacs.d/helm/")
;;(require 'helm-config)
;;(helm-mode 1)


;;�޸Ĺ����״ barΪ���� boxΪ����
(setq-default cursor-type 'bar)


