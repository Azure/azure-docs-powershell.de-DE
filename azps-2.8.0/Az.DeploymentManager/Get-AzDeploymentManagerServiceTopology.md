---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 54a48a025dff2bba2c1ad620237d0a84aacf7d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651368"
---
# Get-AzDeploymentManagerServiceTopology

## Synopsis
Ruft die Dienst Topologie ab.

## Syntax

### Interaktiv (Standard)
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzDeploymentManagerServiceTopology** " Ruft eine Dienst Topologie ab.

Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzDeploymentManagerServiceTopology-Cmdlets Änderungen an der Topologie vornehmen.
Geben Sie die Dienst Topologie nach dem Namen und dem Namen der Ressourcengruppe an. Alternativ können Sie das ServiceTopology-Objekt oder die resourcecode-Objekt bereitstellen.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

Dieser Befehl ruft eine Dienst Topologie mit dem Namen ContosoServiceTopology in der ContosoResourceGroup.

### Beispiel 2: Abrufen einer Dienst Topologie mithilfe des Ressourcenbezeichners.
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

Dieser Befehl ruft eine Dienst Topologie mit dem Namen ContosoServiceTopology in der ContosoResourceGroup.

### Beispiel 3: Abrufen einer Dienst Topologie mithilfe des Dienst Topologie-Objekts.
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

Dieser Befehl ruft eine Dienst Topologie ab, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $serviceTopologyObject entsprechen.

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
Ressourcenobjekt der Dienst Topologie.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name der Dienst Topologie.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource

## Ausgaben

### Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource

## Notizen

## Verwandte Links
