---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 1db46630ea4f864e1658eea8b789a79e6050fbbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008261"
---
# Get-AzResourceGroupDeployment

## Synopsis
Ruft die Bereitstellungen in einer Ressourcengruppe ab.

## Syntax

### GetByResourceGroupDeploymentName (Standard)
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzResourceGroupDeployment** " Ruft die Bereitstellungen in einer Azure-Ressourcengruppe ab.
Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.
Standardmäßig ruft **Get-AzResourceGroupDeployment** alle Bereitstellungen für eine angegebene Ressourcengruppe ab.
Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank oder eine Website.
Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.
Bei einer Bereitstellung handelt es sich um den Vorgang, der die Ressourcen in der Ressourcengruppe zur Verwendung zur Verfügung stellt.
Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzResourceGroup-Cmdlet.
Sie können dieses Cmdlet für die Nachverfolgung verwenden.
Verwenden Sie zum Debuggen dieses Cmdlet mit dem Cmdlet "Get-AzLog".

## Beispiele

### Beispiel 1: Abrufen aller Bereitstellungen für eine Ressourcengruppe
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Dieser Befehl ruft alle Bereitstellungen für die ContosoLabsRG-Ressourcengruppe ab.
Die Ausgabe zeigt eine Bereitstellung für einen WordPress-Blog, in dem eine Katalogvorlage verwendet wird.

### Beispiel 2: Abrufen einer Bereitstellung nach Name
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Dieser Befehl ruft die DeployWebsite01-Bereitstellung der ContosoLabsRG-Ressourcengruppe ab.
Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzResourceGroup** oder **New-AzResourceGroupDeployment** erstellen.
Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.

### Beispiel 3: Abrufen der Bereitstellungen aller Ressourcengruppen
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Dieser Befehl ruft mithilfe des Get-AzResourceGroup-Cmdlets alle Ressourcengruppen in Ihrem Abonnement ab.
Der Befehl übergibt die Ressourcengruppen mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet ruft alle Bereitstellungen aller Ressourcengruppen im Abonnement ab und übergibt die Ergebnisse an das Format-Table-Cmdlet, um deren **ResourceGroupName** -, **deploymentname** -und **ProvisioningState** -Eigenschaftenwerte anzuzeigen.

## Parameter

### -ApiVersion
Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.
Sie können eine andere Version als die Standard Version angeben.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -ID
Gibt die ID der Ressourcengruppen Bereitstellung an, die abgerufen werden soll.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Bereitstellung an, die abgerufen werden soll.
Platzhalterzeichen sind nicht zulässig.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.

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
Gibt den Namen einer Ressourcengruppe an.
Das Cmdlet ruft die Bereitstellungen für die Ressourcengruppe ab, die dieser Parameter angibt.
Platzhalterzeichen sind nicht zulässig.
Dieser Parameter ist erforderlich, und Sie können in jedem Befehl nur eine Ressourcengruppe angeben.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceGroupDeployment

## Notizen

## Verwandte Links

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[Neu – AzResourceGroup](./New-AzResourceGroup.md)

[Neu – AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stopp-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Test-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


