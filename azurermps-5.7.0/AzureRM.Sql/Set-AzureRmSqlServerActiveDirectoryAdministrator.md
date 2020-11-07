---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 43dbbe6ca4f24e98bcfc45703c387ccb5fb4db03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662714"
---
# Set-AzureRmSqlServerActiveDirectoryAdministrator

## Synopsis
Stellt einen Azure AD-Administrator für SQL Server vor.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmSqlServerActiveDirectoryAdministrator" stellt** einen Azure Active Directory (Azure AD)-Administrator für den AzureSQL-Server im aktuellen Abonnement dar.

Sie können jeweils nur einen Administrator bereitstellen.

Die folgenden Mitglieder von Azure AD können als SQL Server-Administrator bereitgestellt werden:

- Native Member von Azure AD 
- Verbundmitglieder von Azure AD 
- Importierte Mitglieder aus anderen Azure ADS, die native oder Federated-Mitglieder sind 
- Als Sicherheitsgruppen erstellte Azure Ad-Gruppen

Microsoft-Konten, wie Sie in den Outlook.com-, hotmail.com-oder Live.com-Domänen vorliegen, werden nicht als Administratoren unterstützt.
Andere Gastkonten, beispielsweise die in der gmail.com-oder Yahoo.com-Domäne, werden nicht als Administratoren unterstützt.

Wir empfehlen, dass Sie eine dedizierte Azure Ad-Gruppe als Administrator bereitstellen.

## Beispiele

### Beispiel 1: Bereitstelleneiner Administratorgruppe für einen Server
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

Dieser Befehl stellt eine Azure AD-Administratorgruppe namens DBAs für den Server mit dem Namen Server01 dar.
Dieser Server ist dem Ressourcengruppen-ResourceGroup01 zugeordnet.

### Beispiel 2: Bereitstellen eines Administratorbenutzers für einen Server
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

Mit diesem Befehl wird ein Azure AD-Benutzer als Administrator für den Server mit dem Namen "Server01" abgeregelt.

### Beispiel 3: Bereitstelleneiner Administratorgruppe durch Angabe der ID
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

Dieser Befehl stellt eine Azure AD-Administratorgruppe namens DBAs für den Server mit dem Namen Server01 dar.
Der Befehl gibt eine ID für den *objectID* -Parameter an.
Dadurch wird sichergestellt, dass der Befehl erfolgreich ausgeführt wird, auch wenn der Anzeigename der Gruppe nicht eindeutig ist.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Gibt den Anzeigenamen des Azure AD-Administrators an, der von diesem Cmdlet vorgesehen ist.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectID
Gibt die eindeutige ID des Azure AD-Administrators an, der von diesem Cmdlet abgeregelt wird.
Wenn der Anzeigename nicht eindeutig ist, müssen Sie einen Wert für diesen Parameter angeben.

```yaml
Type: Guid
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
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servername
Gibt den Namen des SQL-Servers an, für den ein Administrator von diesem Cmdlet vorgesehen ist.

```yaml
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel

## Notizen

## Verwandte Links

[Get-AzureRmSqlServerActiveDirectoryAdministrator](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[Remove-AzureRmSqlServerActiveDirectoryAdministrator](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)


