# TP_shell
test emelie
test sergio
test eric

#lien_tokens
https://github.com/settings/tokens

#!/bin/sh

restoreData() {
    # Vérifier que le fichier de backup existe
    if [ -f tasks_backup.txt ]; then
        # Copier le backup vers tasks.txt
        cp tasks_backup.txt tasks.txt
        echo "Base restaurée depuis la sauvegarde"

        # Commit Git
        git add tasks.txt
        git commit -m "feat: ajout fonction restaurer_base"
    else
        echo "Aucune sauvegarde disponible"
    fi
}
