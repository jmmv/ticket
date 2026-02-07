# Doom Emacs setup

```elisp
;;; In ~/.doom.d/packages.el
(package! ticket
  :recipe (:host github :repo "jmmv/ticket" :branch "emacs"
           :files ("emacs/ticket.el")))

;;; In ~/.doom.d/config.el
(use-package! ticket
  :config
  (map! :leader
        (:prefix ("k" . "ticket")
         :desc "List open tickets" "l" #'ticket-browser
         :desc "List all tickets"  "L" #'ticket-browser-all
         :desc "Ticket actions"    "k" #'ticket-transient)))
```
