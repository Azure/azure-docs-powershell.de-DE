---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 134a236a8259a3197abed3b033c86904a9389643
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298119"
---
# Get-AzDataLakeAnalyticsCatalogItemAclEntry

## Synopsis
Ruft einen Eintrag in der ACL eines Katalog-oder Katalogelements in Data Lake Analytics ab.

## Syntax

### GetCatalogAclEntry (Standard)
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetCatalogAclEntryForUserOwner
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogAclEntryForGroupOwner
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogItemAclEntry
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogItemAclEntryForUserOwner
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogItemAclEntryForGroupOwner
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzDataLakeAnalyticsCatalogItemAclEntry** " Ruft eine Liste von Einträgen (ACEs) in der Zugriffssteuerungsliste (ACL) eines Katalog-oder Katalogelements in Data Lake Analytics ab.

## Beispiele

### Beispiel 1: Abrufen der ACL für einen Katalog
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

Mit diesem Befehl wird die ACL für den Katalog des angegebenen Data Lake Analytics-Kontos abgerufen.

### Beispiel 2: Abrufen des ACL-Eintrags des Benutzer Besitzers für einen Katalog
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

Dieser Befehl ruft die ACL-Eingabe des Benutzer Besitzers für den Katalog des angegebenen Data Lake Analytics-Kontos ab.

### Beispiel 3: Abrufen des ACL-Eintrags des Gruppen Besitzers für einen Katalog
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

Dieser Befehl ruft die ACL-Eingabe des Gruppen Besitzers für den Katalog des angegebenen Data Lake Analytics-Kontos ab.

### Beispiel 4: Abrufen der ACL für eine Datenbank
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

Mit diesem Befehl wird die ACL für die Datenbank des angegebenen Data Lake Analytics-Kontos abgerufen.

### Beispiel 5: Abrufen des ACL-Eintrags des Benutzer Besitzers für eine Datenbank
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

Mit diesem Befehl wird der ACL-Eintrag des Benutzer Besitzers für die Datenbank des angegebenen Data Lake Analytics-Kontos abgerufen.

### Beispiel 6: Abrufen des ACL-Eintrags des Gruppen Besitzers für eine Datenbank
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

Mit diesem Befehl wird der ACL-Eintrag des Gruppen Besitzers für die Datenbank des angegebenen Data Lake Analytics-Kontos abgerufen.

## Parameter

### -Konto
Gibt den Namen des Daten Lake Analytics-Kontos an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -GroupOwner
Abrufen des ACL-Eintrags des Katalogs für den Gruppenbesitzer

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ItemType
Gibt den Typ des Katalogs oder des Katalogelements an. Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Katalog
- Datenbank

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Gibt den Daten See-Analysepfad eines Katalog-oder Katalogelements an.
Die Teile des Pfads sollten durch einen Punkt (.) getrennt werden.

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserOwner
Abrufen des ACL-Eintrags des Katalogs für den Benutzer Besitzer

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance

## Ausgaben

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl

## Notizen

## Verwandte Links

[U-SQL bietet jetzt Zugriffssteuerung auf Datenbankebene](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[Remove-AzDataLakeAnalyticsCatalogItemAclEntry](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[Satz-AzDataLakeAnalyticsCatalogItemAclEntry](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
