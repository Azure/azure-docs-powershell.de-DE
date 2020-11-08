---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: c3218141e495bb92216e254830ddaa7dd7a0a0c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003984"
---
# Get-AzTenantDeployment

## Synopsis
Abrufen der Bereitstellung im MANDANTENBEREICH

## Syntax

### GetByDeploymentName (Standard)
```
Get-AzTenantDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzTenantDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Get-AzTenantDeployment werden** die Bereitstellungen im MANDANTENBEREICH abgerufen.
Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.
Standardmäßig ruft **Get-AzTenantDeployment** alle Bereitstellungen im MANDANTENBEREICH ab.

## Beispiele

### Beispiel 1: Abrufen aller Bereitstellungen im MANDANTENBEREICH
```
PS C:\>Get-AzTenantDeployment
```

Dieser Befehl ruft alle Bereitstellungen im aktuellen MANDANTENBEREICH ab.

### Beispiel 2: Abrufen einer Bereitstellung nach Name
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

Mit diesem Befehl wird die "Deploy01"-Bereitstellung im aktuellen MANDANTENBEREICH abgerufen.
Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzTenantDeployment** erstellen.
Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.

### Beispiel 3: Abrufen einer Bereitstellung nach ID
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

Mit diesem Befehl wird die "Deploy01"-Bereitstellung im MANDANTENBEREICH abgerufen.

## Parameter

### -ApiVersion
Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.
Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ID
Die vollqualifizierte Ressourcen-ID der Bereitstellung.
Beispiel:/Providers/Microsoft.Resources/Deployments/{deploymentName}

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der Bereitstellung.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
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

### Keine

## Ausgaben

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## Notizen

## Verwandte Links
