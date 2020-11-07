---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 6cc3b0f066f267b51a90c0cb0c56d1972ec92f5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826063"
---
# Get-AzSqlServerKeyVaultKey

## Synopsis
Ruft die schlüsseltresor Schlüssel von SQL Server ab.

## Syntax

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Get-AzSqlServerKeyVaultKey-Cmdlet ruft Informationen zu den schlüsseltresor Schlüsseln auf einem SQL Server ab.
Sie können alle Schlüssel auf einem Server anzeigen oder einen bestimmten Schlüssel anzeigen, indem Sie den KeyId bereitstellen.

## Beispiele

### Beispiel 1: Abrufen aller schlüsseltresor-Schlüssel
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

Dieser Befehl ruft alle schlüsseltresor Schlüssel auf einem SQL Server ab.
ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Fingerabdruck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey2_01234567890123456789012345678901 Typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Fingerabdruck: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 Uhr

### Beispiel 2: Abrufen eines bestimmten Key Vault-Schlüssels
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

Dieser Befehl ruft den Schlüssel Vault-Schlüssel mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ab und speichert ihn dann in der $MyServerKeyVaultKey-Variablen.
Sie können die Eigenschaften von $MyServerKeyVaultKey überprüfen, um Details zum schlüsseltresor abzurufen.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyId
Der Azure Key Vault-KeyId

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servername
Der Azure SQL Server-Name.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel

## Notizen

## Verwandte Links

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)
