---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469736"
---
# Remove-AzFunctionAppPlan

## SYNOPSIS
Löscht einen Funktions-App-Plan.

## SYNTAX

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

## BESCHREIBUNG
Löscht einen Funktions-App-Plan.

## BEISPIELE

### Beispiel 1: Einen Funktions-App-Plan nach Name erhalten und löschen.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

Dieser Befehl ruft einen Funktions-App-Plan nach Name ab und löscht ihn.

### Beispiel 2: Löschen eines Funktions-App-Plans nach Name.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Mit diesem Befehl wird ein Funktions-App-Plan nach Name gelöscht.

## PARAMETERS

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

### -Force
Erzwingt das Cmdlet, den Funktions-App-Plan ohne Bestätigungsaufforderung zu entfernen.

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

### -Name
Der Name der Funktions-App.

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

### System.Boolean

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

