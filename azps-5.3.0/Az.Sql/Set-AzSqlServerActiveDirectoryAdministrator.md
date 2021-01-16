---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468035"
---
# Set-AzSqlServerActiveDirectoryAdministrator

## SYNOPSIS
Bereitstellung eines Azure AD-Administrators für SQL Server.

## SYNTAX

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzSqlServerActiveDirectoryAdministrator** stellt im aktuellen Abonnement einen Azure Active Directory (Azure AD)-Administrator für AzureSQL Server bereit.
Sie können immer nur einen Administrator gleichzeitig bereitstellen.
Die folgenden Mitglieder von Azure AD können als Administrator bereitgestellt SQL Server werden:
- Native Mitglieder von Azure AD 
- Verbundmitglieder von Azure AD 
- Importierte Mitglieder aus anderen Azure ADs, die native Mitglieder oder Partnermitglieder sind 
- Azure AD-Gruppen, die als Sicherheitsgruppen für Microsoft-Konten erstellt wurden, z. B. in den Domänen Outlook.com, Hotmail.com oder Live.com, werden als Administratoren nicht unterstützt.
Andere Gastkonten, z. B. in Gmail.com oder Yahoo.com, werden als Administratoren nicht unterstützt.
Es wird empfohlen, eine dedizierte Azure AD-Gruppe als Administrator bereitstellen.

## BEISPIELE

### Beispiel 1: Bereitstellen einer Administratorgruppe für einen Server
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

Mit diesem Befehl wird eine Azure AD-Administratorgruppe namens DBAs für den Server "Server01" bereitgestellt.
Dieser Server ist der Ressourcengruppe "ResourceGroup01" zugeordnet.

### Beispiel 2: Bereitstellen eines Administratorbenutzers für einen Server
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

Mit diesem Befehl wird ein Azure AD-Benutzer als Administrator für den Server "Server01" bereitgestellt.

### Beispiel 3: Bereitstellen einer Administratorgruppe durch Angabe der ID
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

Mit diesem Befehl wird eine Azure AD-Administratorgruppe namens DBAs für den Server "Server01" bereitgestellt.
Der Befehl gibt eine ID für den *Parameter ObjectId* an.
Dadurch wird sichergestellt, dass der Befehl auch dann erfolgreich ist, wenn der Anzeigename der Gruppe nicht eindeutig ist.

## PARAMETERS

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

### -DisplayName
Gibt den Anzeigenamen des Azure AD-Administrators an, der von diesem Cmdlet bereitgestellt wird.

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

### -ObjectId
Gibt die eindeutige ID des Azure AD-Administrators an, die von diesem Cmdlet bereitgestellt wird.
Wenn der Anzeigename nicht eindeutig ist, müssen Sie einen Wert für diesen Parameter angeben.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.

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
Gibt den Namen des SQL Server, für das dieses Cmdlet einen Administrator eingibt.

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

### System.Guid

## AUSGABEN

### Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzSqlServerActiveDirectoryAdministrator](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[Remove-AzSqlServerActiveDirectoryAdministrator](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[Disable-AzSqlServerActiveDirectoryOnlyAuthentication](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[SQL Datenbankdokumentation](https://docs.microsoft.com/azure/sql-database/)


