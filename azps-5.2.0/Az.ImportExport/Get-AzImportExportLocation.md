---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290981"
---
# Get-AzImportExportLocation

## SYNOPSIS
Gibt die Details zu einem Speicherort zurück, an den Sie die einem Import- oder Exportauftrag zugeordneten Datenträger versenden können.
Ein Speicherort ist eine Azure-Region.

## SYNTAX

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

## BESCHREIBUNG
Gibt die Details zu einem Speicherort zurück, an den Sie die einem Import- oder Exportauftrag zugeordneten Datenträger versenden können.
Ein Speicherort ist eine Azure-Region.

## BEISPIELE

### Beispiel 1: Alle Details zum Standort der Region Azure mit Standardkontext erhalten
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

Dieses Cmdlet ruft alle Details zum Standort der Region Azure mit dem Standardkontext ab.

### Beispiel 2: Erhalten von Standortdetails für die Region Azure nach Standortname
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

Dieses Cmdlet ruft Standortdetails für die Region Azure nach Standortname ab.

### Beispiel 3: Erhalten von Standortdetails für die Region Azure nach Identität
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

Diese Cmdletlisten ruft Standortdetails für die Region Azure nach Identität ab.

## PARAMETERS

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

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
Der Name des Speicherorts.
Beispielsweise "USA, Westen" oder "Westus".

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation

## HINWEISE

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften. Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.


INPUTOBJECT <IImportExportIdentity> : Identity Parameter
  - `[Id <String>]`: Ressourcenidentitätspfad
  - `[JobName <String>]`: Der Name des Import-/Exportauftrags.
  - `[LocationName <String>]`: Der Name des Speicherorts. Beispielsweise "USA, Westen" oder "Westus".
  - `[ResourceGroupName <String>]`: Der Ressourcengruppenname identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.
  - `[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.

## LINKS ZU VERWANDTEN THEMEN

