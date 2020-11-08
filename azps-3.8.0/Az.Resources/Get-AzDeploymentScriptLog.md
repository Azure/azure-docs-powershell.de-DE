---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 855127362fbcbf906755affde0bec6de5e7f2698
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004525"
---
# Get-AzDeploymentScriptLog

## Synopsis
Ruft das Protokoll einer Bereitstellung-Skriptausführung ab.

## Syntax

### GetDeploymentScriptLogByName (Standard)
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetDeploymentScriptLogByResourceId
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetDeploymentScriptLogByInputObject
```
Get-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzDeploymentScriptLog** " Ruft das Protokoll einer Bereitstellungsskript Ausführung ab.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

Ruft das Protokoll eines Bereitstellungsskripts mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG.

### Beispiel 2
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

Der erste Befehl ruft ein Bereitstellungsskript mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG.
Der zweite Befehl ruft das Protokoll des angegebenen Bereitstellungsskripts ab.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentScriptInputObject
Das PowerShell-Objekt des Bereitstellungsskripts.

```yaml
Type: PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeploymentScriptResourceId
Die vollqualifizierte Ressourcen-ID des Bereitstellungsskripts.
Beispiel:/Subscriptions/{subId}/resourceGroups/{rgName}/Providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name des Bereitstellungsskripts.

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.
Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript

## Ausgaben

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog

## Notizen

## Verwandte Links
