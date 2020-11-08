---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004601"
---
# Get-AzDeploymentManagerRollout

## Synopsis
Ruft den Rollout ab.

## Syntax

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

## Beschreibung
Das Cmdlet " **Get-AzDeploymentManagerRollout** " Ruft ein Rollout ab und gibt ein Objekt zurück, das diesen Rollout mit allen detaillierten Informationen zum Fortschritt des Rollouts darstellt.
Geben Sie den Rollout nach dem Namen und dem Namen der Ressourcengruppe an. Alternativ können Sie das Rollout-Objekt oder die "Resourcen-Nr" bereitstellen.

Das zurückgegebene Rollout-Objekt enthält die Dienste, Dienst Einheiten und Schritte, die bereitgestellt wurden und die in Bearbeitung sind. Diejenigen, die noch bereitgestellt werden, sind nicht in der Antwort.

## Beispiele

### Beispiel 1 Abrufen des Rollouts
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup. 

### Beispiel 2 Abrufen und Anzeigen der Rollout Details
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup. Der-verbose-Schalter zeigt alle Rollout-Details hierarchisch an; zeigt die Dienste, die ServiceUnits und die Schritte unter den einzelnen Serviceunit sowie Kontextinformationen für die einzelnen Schritte für eine ganzheitliche Ansicht des Rollouts an.

### Beispiel 3: Abrufen eines Rollouts mit dem Ressourcenbezeichner
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Dieser Befehl ruft ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup.

### Beispiel 4: Abrufen eines Rollouts mithilfe des Rollout-Objekts.
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

Dieser Befehl ruft ein Rollout ab, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $rolloutObject entsprechen.

## Parameter

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

### -Inputobject
Rollout-Objekt.

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

### -Resourcen-Nr
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### Microsoft. Azure. Commands. deploymentmanager. Models. PSRollout

## Ausgaben

### Microsoft. Azure. Commands. deploymentmanager. Models. PSRollout

## Notizen

## Verwandte Links
