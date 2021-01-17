---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 632b7710a6055f40c6cdc6d87d4b2cf8e3e17eeb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458279"
---
# Get-AzSqlDatabaseTransparentDataEncryption

## SYNOPSIS
Ruft den Status "TDE" für eine Datenbank ab.

## SYNTAX

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzSqlDatabaseTransparentDataEncryption"** ruft den Status der transparenten Datenverschlüsselung (Transparent Data Encryption, TDE) für eine Azure SQL ab.
Weitere Informationen finden Sie unter "Transparente Datenverschlüsselung mit Azure SQL-Datenbank" https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (in der Microsoft Developer Network Library).
Dieses Cmdlet ruft den aktuellen Zustand von TDE ab, aber sowohl die Verschlüsselung als auch die Entschlüsselung können Vorgänge mit langer Dauer sein.
Um den Fortschritt des Verschlüsselungsscans zu sehen, führen Sie das Get-AzSqlDatabaseTransparentDataEncryptionActivity aus.
Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.

## BEISPIELE

### Beispiel 1: Erhalten des Status "TDE" für eine Datenbank
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

Dieser Befehl ruft den Status "TDE" für die Datenbank mit dem Namen "Database01" auf dem Server mit dem Namen "server01" ab.

## PARAMETERS

### -DatabaseName
Gibt den Namen der Datenbank an, für die dieses Cmdlet den Status "TDE" erhält.

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -ServerName
Gibt den Namen des Servers an, der die Datenbank hostet, für die dieses Cmdlet den STATUS "TDE" erhält.

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

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzSqlDatabaseTransparentDataEncryptionActivity](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[Set-AzSqlDatabaseTransparentDataEncryption](./Set-AzSqlDatabaseTransparentDataEncryption.md)
