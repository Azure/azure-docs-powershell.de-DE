---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 20a9abc5cfc2ad2cc35bbedcf976daac286abb92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928811"
---
# Get-AzTimeSeriesInsightsAccessPolicy

## SYNOPSIS
Ruft die Zugriffsrichtlinie mit dem angegebenen Namen in der angegebenen Umgebung ab.

## SYNTAX

### Liste (Standard)
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Erhalten
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Ruft die Zugriffsrichtlinie mit dem angegebenen Namen in der angegebenen Umgebung ab.

## BEISPIELE

### Beispiel 1: Auflisten aller Zugriffsrichtlinien in einer angegebenen Umgebung
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

Mit diesem Befehl werden alle Zugriffsrichtlinien unter einer angegebenen Umgebung aufgeführt.

### Beispiel 2: Erhalten einer angegebenen Zugriffsrichtlinie nach Name
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

Dieser Befehl ruft eine angegebene Zugriffsrichtlinie ab.

### Beispiel 3: Erhalten einer angegebenen Zugriffsrichtlinie nach Objekt
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

Dieser Befehl ruft eine angegebene Zugriffsrichtlinie ab.

## PARAMETER

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

### -EnvironmentName
Der Name der Zeitreiheneinblickumgebung, die der angegebenen Ressourcengruppe zugeordnet ist.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name der Time Series Insights-Zugriffsrichtlinie, die der angegebenen Umgebung zugeordnet ist.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Name einer Azure-Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure-Abonnement-ID.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource

## NOTIZEN

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält. Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.


INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identitätsparameter
  - `[AccessPolicyName <String>]`: Name der Zugriffsrichtlinie.
  - `[EnvironmentName <String>]`: Name der Umgebung
  - `[EventSourceName <String>]`: Der Name der Time Series Insights-Ereignisquelle, die der angegebenen Umgebung zugeordnet ist.
  - `[Id <String>]`: Ressourcenidentitätspfad
  - `[ReferenceDataSetName <String>]`: Name des Bezugsdatensets.
  - `[ResourceGroupName <String>]`: Name einer Azure-Ressourcengruppe.
  - `[SubscriptionId <String>]`: Azure-Abonnement-ID.

## VERWANDTE LINKS

