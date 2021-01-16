---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301288"
---
# Update-AzFunctionAppPlan

## SYNOPSIS
Aktualisiert einen Funktions-App-Serviceplan.

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
Aktualisiert einen Funktions-App-Serviceplan.

## BEISPIELE

### Beispiel 1: Aktualisieren eines App-Serviceplans auf eine EP2-SKU mit maximal 20 Mitarbeitern.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Mit diesem Befehl wird ein App-Service-Plan auf eine EP2-SKU mit maximal 20 Mitarbeitern aktualisiert.

## PARAMETERS

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
Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.

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
Die maximale Anzahl von Mitarbeitern für den App-Serviceplan.

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
Die Mindestanzahl von Mitarbeitern für den App-Serviceplan.

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
Name des App-Service-Plans.

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
Die SKU des Plans.
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

### -Confirm
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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## HINWEISE

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften. Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.


INPUTOBJECT <IAppServicePlan> : 
  - `Location <String>`: Ressourcenspeicherort.
  - `[Kind <String>]`: Ressourcentyp.
  - `[Tag <IResourceTags>]`: Ressourcentags.
    - `[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.
  - `[Capacity <Int32?>]`: Die aktuelle Anzahl von Instanzen, die der Ressource zugeordnet sind.
  - `[FreeOfferExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem das kostenlose Angebot für die Serverfarm abläuft.
  - `[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.
  - `[HyperV <Boolean?>]`: Wenn andernfalls der Hyper-V-Container-App-Dienstplan <code>true</code> <code>false</code> verwendet wird.
  - `[IsSpot <Boolean?>]`: <code>true</code> Falls, besitzt dieser App-Serviceplan Spotinstanzen.
  - `[IsXenon <Boolean?>]`: Veraltet: Wenn andernfalls der Hyper-V-Container-App-Dienstplan <code>true</code> <code>false</code> verwendet wird.
  - `[MaximumElasticWorkerCount <Int32?>]`: Maximal zulässige Anzahl von Arbeitskräften für diesen Serviceplan der App "ScaleEnabled"
  - `[PerSiteScaling <Boolean?>]`: <code>true</code> Falls, können Apps, die diesem App Service Plan zugewiesen sind, unabhängig skaliert werden.         Wenn <code>false</code> diesem App -Service-Plan zugewiesene Apps auf alle Instanzen des Plans skaliert werden.
  - `[Reserved <Boolean?>]`: Wenn Linux-App-Dienstplan <code>true</code> , <code>false</code> andernfalls.
  - `[SkuCapability <ICapability[]>]`: Funktionen der SKU, z. B. aktivierter Datenverkehrs-Manager?
    - `[Name <String>]`: Name der SKU-Funktion.
    - `[Reason <String>]`: Grund der SKU-Funktion.
    - `[Value <String>]`: Wert der SKU-Funktion.
  - `[SkuCapacityDefault <Int32?>]`: Standardanzahl von Mitarbeitern für diese App Service Plan-SKU.
  - `[SkuCapacityMaximum <Int32?>]`: Maximale Anzahl von Mitarbeitern für diese App Service Plan-SKU.
  - `[SkuCapacityMinimum <Int32?>]`: Mindestanzahl von Mitarbeitern für diese App Service Plan-SKU.
  - `[SkuCapacityScaleType <String>]`: Verfügbare Skalierungskonfigurationen für einen App-Service-Plan.
  - `[SkuFamily <String>]`: Familiencode der Ressourcen-SKU.
  - `[SkuLocation <String[]>]`: Speicherorte der SKU.
  - `[SkuName <String>]`: Name der Ressourcen-SKU.
  - `[SkuSize <String>]`: Größenbezeichner der Ressourcen-SKU.
  - `[SkuTier <String>]`: Dienstebene der Ressourcen-SKU.
  - `[SpotExpirationTime <DateTime?>]`: Der Zeitpunkt, zu dem die Serverfarm abläuft. Nur gültig, wenn es sich um eine Spotserverfarm handelt.
  - `[TargetWorkerCount <Int32?>]`: Anzahl der Skalierungsmitarbeiter
  - `[TargetWorkerSizeId <Int32?>]`: Skalierungs-Worker-Größen-ID.
  - `[WorkerTierName <String>]`: Dem App -Dienstplan zugewiesene Zielworkerebene.

## LINKS ZU VERWANDTEN THEMEN

