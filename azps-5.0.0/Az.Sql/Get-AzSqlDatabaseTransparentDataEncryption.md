---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 632b7710a6055f40c6cdc6d87d4b2cf8e3e17eeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296697"
---
# Get-AzSqlDatabaseTransparentDataEncryption

## Synopsis
Ruft den Status "DSA" für eine Datenbank ab.

## Syntax

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzSqlDatabaseTransparentDataEncryption** " Ruft den Zustand der transparenten Datenverschlüsselung (DSA) für eine Azure SQL-Datenbank ab.
Weitere Informationen finden Sie unter transparente Datenverschlüsselung mit Azure SQL-Datenbank https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) in der Microsoft Developer-Netzwerkbibliothek.
Dieses Cmdlet ruft den aktuellen Status von "DSA" ab, aber sowohl die Verschlüsselung als auch die Entschlüsselung können Vorgänge mit langer Laufzeit sein.
Führen Sie das Get-AzSqlDatabaseTransparentDataEncryptionActivity-Cmdlet aus, um den Status des Verschlüsselungs Scans anzuzeigen.
Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.

## Beispiele

### Beispiel 1: Abrufen des DSA-Status für eine Datenbank
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

Dieser Befehl ruft den Status von "DSA" für die Datenbank mit dem Namen "database01" auf dem Server mit dem Namen "Server01" ab.

## Parameter

### -DatabaseName
Gibt den Namen der Datenbank an, für die dieses Cmdlet den DSA-Status erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.

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
Gibt den Namen des Servers an, der die Datenbank hostet, für die dieses Cmdlet den DSA-Status erhält.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel

## Notizen

## Verwandte Links

[Get-AzSqlDatabaseTransparentDataEncryptionActivity](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[Satz-AzSqlDatabaseTransparentDataEncryption](./Set-AzSqlDatabaseTransparentDataEncryption.md)
