---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175623"
---
# Remove-AzFunctionAppPlan

## Synopsis
Löscht einen Funktions-APP-Plan.

## Syntax

### ByName (Standard)
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Beschreibung
Löscht einen Funktions-APP-Plan.

## Beispiele

### Beispiel 1: Rufen Sie einen Funktions-APP-Plan nach Namen ab, und löschen Sie ihn.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

Dieser Befehl ruft einen Funktions-APP-Plan nach Name ab und löscht ihn.

### Beispiel 2: Löschen eines Funktions-APP-Plans nach Name
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Dieser Befehl löscht einen Funktions-APP-Plan nach Namen.

## Parameter

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

### -Force
Erzwingt, dass das Cmdlet den Funktions-APP-Plan entfernt, ohne die Bestätigung zu bestätigen.

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

### -Name
Der Name der Funktions-APP.

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

### -PassThru
Gibt "true" zurück, wenn der Befehl erfolgreich ist.

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

### System. Boolean

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

