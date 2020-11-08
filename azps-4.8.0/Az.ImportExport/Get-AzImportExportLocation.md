---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172955"
---
# Get-AzImportExportLocation

## Synopsis
Gibt die Details zu einem Speicherort zurück, an den Sie die Datenträger senden können, die einem Import-oder Exportauftrag zugeordnet sind.
Eine Position ist ein Azure-Bereich.

## Syntax

### Liste (Standard)
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Erhalten
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Beschreibung
Gibt die Details zu einem Speicherort zurück, an den Sie die Datenträger senden können, die einem Import-oder Exportauftrag zugeordnet sind.
Eine Position ist ein Azure-Bereich.

## Beispiele

### Beispiel 1: Abrufen aller Azure Region-Standortdetails mit dem Standardkontext
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

Mit diesem Cmdlet werden alle Standortdetails des Azure-Bereichs mit dem Standardkontext abgerufen.

### Beispiel 2: Abrufen der Standortdetails des Azure-Bereichs nach dem Standortnamen
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

Dieses Cmdlet ruft die Details des Azure Region-Standorts nach dem Standortnamen ab.

### Beispiel 3: Abrufen von Details zum Azure Region-Standort nach Identität
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

In diesen Cmdlet-Listen werden Standortdetails für Azure-Region nach Identität abgerufen.

## Parameter

### -AcceptLanguage
Gibt die bevorzugte Sprache für die Antwort an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name des Standorts.
Beispielsweise West-US oder westus.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. IImportExportIdentity

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. Api20161101. ILocation

## Notizen

Aliase

komplexe Parameter Eigenschaften

Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.


Inputobject <IImportExportIdentity> : Identity-Parameter
  - `[Id <String>]`: Ressourcen Identitäts Pfad
  - `[JobName <String>]`: Der Name des Import/Export-Auftrags.
  - `[LocationName <String>]`: Der Name des Standorts. Beispielsweise West-US oder westus.
  - `[ResourceGroupName <String>]`: Der Name der Ressourcengruppe identifiziert die Ressourcengruppe eindeutig innerhalb des Benutzer Abonnements.
  - `[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.

## Verwandte Links

