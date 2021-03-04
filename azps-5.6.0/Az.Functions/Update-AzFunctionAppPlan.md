---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: 522de6721d92b76938843b28322b94b5cc6ce481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924136"
---
# Update-AzFunctionAppPlan

## SYNOPSIS
Aktualisiert einen Funktions-App-Dienstplan.

## SYNTAX

### ByName (Standard)
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESCHREIBUNG
Aktualisiert einen Funktions-App-Dienstplan.

## BEISPIELE

### Beispiel 1: Aktualisieren eines App-Dienstplans auf EP2-Sku mit maximal zwanzig Mitarbeitern.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Mit diesem Befehl wird ein App-Dienstplan mit 20 maximalen Mitarbeitern auf EP2-Sku aktualisiert.

## PARAMETER

### -AsJob
Führen Sie den Befehl als Auftrag aus.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile


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
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumWorkerCount
Die maximale Anzahl von Mitarbeitern für den App-Dienstplan.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumWorkerCount
Die Mindestanzahl von Mitarbeitern für den App-Dienstplan.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name des App Service-Plans.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Führen Sie den Befehl asynchron aus.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe, zu der die Ressource gehört.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sku
Die Sku des Plans.
Gültige Eingaben sind: EP1, EP2, EP3

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

### -SubscriptionId
Die Azure-Abonnement-ID.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Ressourcentags.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## NOTIZEN

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält. Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.


INPUTOBJECT <IAppServicePlan> : 
  - `Location <String>`: Ressourcenspeicherort.
  - `[Kind <String>]`: Art der Ressource.
  - `[Tag <IResourceTags>]`: Ressourcentags.
    - `[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.
  - `[Capacity <Int32?>]`: Aktuelle Anzahl der der Ressource zugewiesenen Instanzen.
  - `[FreeOfferExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem das kostenlose Angebot für die Serverfarm abläuft.
  - `[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.
  - `[HyperV <Boolean?>]`: Wenn Hyper-V-Container-App-Dienstplan <code>true</code> , <code>false</code> andernfalls.
  - `[IsSpot <Boolean?>]`: Wenn <code>true</code> , besitzt dieser App Service Plan Spotinstanzen.
  - `[IsXenon <Boolean?>]`: Veraltet: Wenn Hyper-V-Container-App-Dienstplan <code>true</code> , <code>false</code> andernfalls.
  - `[MaximumElasticWorkerCount <Int32?>]`: Maximale Anzahl der für diesen Serviceplan für die FlexibleScaleEnabled-App zulässigen Mitarbeiter
  - `[PerSiteScaling <Boolean?>]`: Wenn diesem App Service-Plan zugewiesene Apps <code>true</code> unabhängig skaliert werden können.         Wenn <code>false</code> apps assigned to this App Service plan will scale to all instances of the plan.
  - `[Reserved <Boolean?>]`: Wenn linux app service plan <code>true</code> , <code>false</code> andernfalls.
  - `[SkuCapability <ICapability[]>]`: Funktionen der SKU, z. B. ist Traffic Manager aktiviert?
    - `[Name <String>]`: Name der SKU-Funktion.
    - `[Reason <String>]`: Grund für die SKU-Funktion.
    - `[Value <String>]`: Wert der SKU-Funktion.
  - `[SkuCapacityDefault <Int32?>]`: Standardanzahl der Mitarbeiter für diese App Service Plan SKU.
  - `[SkuCapacityMaximum <Int32?>]`: Maximale Anzahl von Mitarbeitern für diese App Service Plan SKU.
  - `[SkuCapacityMinimum <Int32?>]`: Mindestanzahl von Mitarbeitern für diese App Service Plan SKU.
  - `[SkuCapacityScaleType <String>]`: Verfügbare Skalierungskonfigurationen für einen App Service-Plan.
  - `[SkuFamily <String>]`: Familiencode der Ressourcen-SKU.
  - `[SkuLocation <String[]>]`: Speicherorte der SKU.
  - `[SkuName <String>]`: Name der Ressourcen-SKU.
  - `[SkuSize <String>]`: Größenbezeichner der Ressourcen-SKU.
  - `[SkuTier <String>]`: Dienstebene der Ressourcen-SKU.
  - `[SpotExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem die Serverfarm abläuft. Gültig nur, wenn es sich um eine Spotserverfarm handelt.
  - `[TargetWorkerCount <Int32?>]`: Skalierung der Workeranzahl.
  - `[TargetWorkerSizeId <Int32?>]`: Skalierung der Mitarbeitergröße ID.
  - `[WorkerTierName <String>]`: Zielarbeiterebene, die dem App Service-Plan zugewiesen ist.

## VERWANDTE LINKS

