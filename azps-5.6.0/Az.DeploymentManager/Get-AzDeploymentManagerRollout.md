---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: 53458d53dd6d8b3f698dc51fc6b1463c9a9134e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925795"
---
# Get-AzDeploymentManagerRollout

## SYNOPSIS
Ruft das Rollout ab.

## SYNTAX

### Interaktiv (Standard)
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzDeploymentManagerRollout-Cmdlet** ruft ein Rollout ab und gibt ein -Objekt zurück, das dieses Rollout mit allen detaillierten Informationen zum Fortschritt des Rollouts darstellt.
Geben Sie das Rollout nach dem Namen und dem Namen der Ressourcengruppe an. Alternativ können Sie das Rolloutobjekt oder die ResourceId bereitstellen.

Das zurückgegebene Rolloutobjekt enthält die Dienste, Diensteinheiten und Schritte, die bereitgestellt wurden und die in Bearbeitung sind. Diejenigen, die noch bereitgestellt werden müssen, befinden sich nicht in der Antwort.

## BEISPIELE

### Beispiel 1 Rollout
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup ab. 

### Beispiel 2 : Informationen zum Rollout erhalten und anzeigen
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup ab. Der Schalter -Verbose zeigt alle Rolloutdetails hierarchisch an. zeigt die Dienste, die ServiceUnits und die Schritte unter den einzelnen ServiceUnit- und Kontextinformationen für jeden Schritt für eine holistische Ansicht des Rollouts an.

### Beispiel 3: Rollout mithilfe des Ressourcenbezeichners
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup ab.

### Beispiel 4: Ein Rollout mithilfe des Rolloutobjekts.
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

Dieser Befehl ruft ein Rollout ab, dessen Name und Ressourcengruppe den Eigenschaften Name und ResourceGroupName des $rolloutObject entsprechen.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -InputObject
Rolloutobjekt.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name des Rollouts.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Der Ressourcenbezeichner.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetryAttempt
Der Wiederholungsversuch des Rollouts.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

### Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout

## AUSGABEN

### Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout

## NOTIZEN

## VERWANDTE LINKS
