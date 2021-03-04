---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 5bf59cb766d82e2fc50bdc75c0a072e2b8d17a69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925787"
---
# Get-AzDeploymentManagerStep

## SYNOPSIS
Ruft den Schritt ab.

## SYNTAX

### Interaktiv (Standard)
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Get-AzDeploymentManagerStep** ruft einen Schritt ab und gibt ein -Objekt zurück, das diesen Schritt darstellt.
Geben Sie den Schritt nach dem Namen und dem Ressourcengruppennamen an. Alternativ können Sie das Step-Objekt oder die ResourceId bereitstellen.

Sie können dieses Objekt lokal ändern und dann Änderungen auf die Artefaktquelle anwenden, indem Sie das cmdlet Set-AzDeploymentManagerStep verwenden.

## BEISPIELE

### Beispiel 1: Einen Schritt erhalten
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

Dieser Befehl ruft einen Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup ab.

### Beispiel 2: Einen Schritt mit dem Ressourcenbezeichner
### Beispiel 1
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

Dieser Befehl ruft einen Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup ab.

### Beispiel 3: Einen Schritt mit einem von der Anwendung zurückgegebenen Objekt New-AzDeploymentManagerStep
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 Dieser Befehl ruft einen Schritt ab, dessen Name und Ressourcengruppe den Eigenschaften Name und ResourceGroupName des $stepObject entsprechen.

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
Das Schrittressourcenobjekt.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name des Schritts.

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

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource

## AUSGABEN

### Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource

## NOTIZEN

## VERWANDTE LINKS
