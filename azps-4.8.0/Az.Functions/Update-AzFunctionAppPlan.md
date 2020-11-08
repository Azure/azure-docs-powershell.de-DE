---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008473"
---
# Update-AzFunctionAppPlan

## Synopsis
Aktualisiert einen Funktions-APP-Service Plan.

## Syntax

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

## Beschreibung
Aktualisiert einen Funktions-APP-Service Plan.

## Beispiele

### Beispiel 1: Aktualisieren eines App-Service-Plans auf ep2 SKU mit maximal zwanzig Mitarbeitern.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Mit diesem Befehl wird ein App-Service Plan auf ep2 SKU mit zwanzig maximalen Arbeitskräften aktualisiert.

## Parameter

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

### -Inputobject
Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.

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
Die maximale Anzahl von Arbeitskräften für den App-Service Plan.

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
Die Mindestanzahl von Arbeitskräften für den App-Service Plan.

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
Name des App-Service Plans

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

### -Nowait
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
Der Name der Ressourcengruppe, zu der die Ressource gehört.

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

### -SKU
Die Plan-SKU.
Gültige Eingaben sind: EP1, ep2, EP3

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

### -Abonnement-Nr
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
Ressourcenkategorien.

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
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IAppServicePlan

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IAppServicePlan

## Notizen

Aliase

komplexe Parameter Eigenschaften

Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.


Inputobject <IAppServicePlan> : 
  - `Location <String>`: Ressourcen Standort.
  - `[Kind <String>]`: Art der Ressource.
  - `[Tag <IResourceTags>]`: Ressourcenkategorien.
    - `[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.
  - `[Capacity <Int32?>]`: Aktuelle Anzahl der Instanzen, die der Ressource zugeordnet sind.
  - `[FreeOfferExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem das ﻿kostenlose Angebot der Serverfarm abläuft.
  - `[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der APP-Dienstumgebung.
  - `[HyperV <Boolean?>]`: Wenn der Hyper-V-Container-App-Service Plan <code>true</code> , <code>false</code> andernfalls.
  - `[IsSpot <Boolean?>]`: Wenn <code>true</code> dieser APP-Service Plan über Spot-Instances verfügt.
  - `[IsXenon <Boolean?>]`: Veraltet: Wenn der Hyper-V-Container-App-Service Plan <code>true</code> , <code>false</code> andernfalls.
  - `[MaximumElasticWorkerCount <Int32?>]`: Maximale Anzahl der insgesamt für diesen ElasticScaleEnabled-App-Service Plan zulässigen Arbeitskräfte
  - `[PerSiteScaling <Boolean?>]`: Wenn <code>true</code> apps, die diesem app-Service Plan zugewiesen sind, unabhängig voneinander skaliert werden können.         Wenn <code>false</code> die diesem app-Service Plan zugewiesenen apps auf alle Instanzen des Plans skaliert werden.
  - `[Reserved <Boolean?>]`: Wenn der Linux-APP <code>true</code> -Service Plan, <code>false</code> andernfalls.
  - `[SkuCapability <ICapability[]>]`: Funktionen der SKU, beispielsweise ist Traffic Manager aktiviert?
    - `[Name <String>]`: Name der SKU-Funktion.
    - `[Reason <String>]`: Grund für die SKU-Funktion.
    - `[Value <String>]`: Wert der SKU-Funktion.
  - `[SkuCapacityDefault <Int32?>]`: Standardanzahl von Arbeitskräften für diese APP-Service Plan-SKU.
  - `[SkuCapacityMaximum <Int32?>]`: Maximale Anzahl von Arbeitskräften für diese APP-Service Plan-SKU.
  - `[SkuCapacityMinimum <Int32?>]`: Mindestanzahl von Arbeitskräften für diese APP-Service Plan-SKU.
  - `[SkuCapacityScaleType <String>]`: Verfügbare Skalierungs Konfigurationen für einen app-Service Plan.
  - `[SkuFamily <String>]`: Familiencode der Ressourcen-SKU.
  - `[SkuLocation <String[]>]`: Speicherorte der SKU.
  - `[SkuName <String>]`: Name der Ressourcen-SKU.
  - `[SkuSize <String>]`: Size-Bezeichner der Ressourcen-SKU.
  - `[SkuTier <String>]`: Dienstebene der Ressourcen-SKU.
  - `[SpotExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem die Serverfarm abläuft. Nur gültig, wenn es sich um eine Spot Serverfarm handelt.
  - `[TargetWorkerCount <Int32?>]`: Skalieren der Worker-Anzahl
  - `[TargetWorkerSizeId <Int32?>]`: Skalierung der Worker-Größen-ID.
  - `[WorkerTierName <String>]`: Zielarbeitsebene, die dem App-Service Plan zugewiesen ist.

## Verwandte Links

