# ativ3
#!/bin/bash


SOURCE_DIR="/caminho/para/diretorio/origem"

# Diretório de destino onde o backup será salvo
DEST_DIR="/caminho/para/diretorio/backup"


CURRENT_DATE=$(date +%F)


BACKUP_FILE="backup-$CURRENT_DATE.tar.gz"


BACKUP_PATH="$DEST_DIR/$BACKUP_FILE"


tar -czf "$BACKUP_PATH" -C "$SOURCE_DIR" .


if [ $? -eq 0 ]; then
  echo "Backup realizado com sucesso: $BACKUP_PATH"
else
  echo "Erro ao realizar o backup"
fi
