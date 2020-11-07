---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: dd61700c5f064a7bc1db84286252a57c18a212db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663438"
---
# Get-AzureRmResourceGroupDeployment

## Synopsis
Ruft die Bereitstellungen in einer Ressourcengruppe ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### GetByResourceGroupDeploymentName (Standard)
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmResourceGroupDeployment** " Ruft die Bereitstellungen in einer Azure-Ressourcengruppe ab.
Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.
Standardmäßig ruft **Get-AzureRmResourceGroupDeployment** alle Bereitstellungen für eine angegebene Ressourcengruppe ab.

Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank oder eine Website.
Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.

Bei einer Bereitstellung handelt es sich um den Vorgang, der die Ressourcen in der Ressourcengruppe zur Verwendung zur Verfügung stellt.
Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzureRmResourceGroup-Cmdlet.

Sie können dieses Cmdlet für die Nachverfolgung verwenden.
Verwenden Sie zum Debuggen dieses Cmdlet mit dem Cmdlet "Get-AzureRmLog".

## Beispiele

### Beispiel 1: Abrufen aller Bereitstellungen für eine Ressourcengruppe
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Dieser Befehl ruft alle Bereitstellungen für die ContosoLabsRG-Ressourcengruppe ab.
Die Ausgabe zeigt eine Bereitstellung für einen WordPress-Blog, in dem eine Katalogvorlage verwendet wird.

### Beispiel 2: Abrufen einer Bereitstellung nach Name
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Dieser Befehl ruft die DeployWebsite01-Bereitstellung der ContosoLabsRG-Ressourcengruppe ab.
Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzureRmResourceGroup** oder **New-AzureRmResourceGroupDeployment** erstellen.
Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.

### Beispiel 3: Abrufen der Bereitstellungen aller Ressourcengruppen
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Dieser Befehl ruft mithilfe des Get-AzureRmResourceGroup-Cmdlets alle Ressourcengruppen in Ihrem Abonnement ab.
Der Befehl übergibt die Ressourcengruppen mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet ruft alle Bereitstellungen aller Ressourcengruppen im Abonnement ab und übergibt die Ergebnisse an das Format-Table-Cmdlet, um deren **ResourceGroupName** -, **deploymentname** -und **ProvisioningState** -Eigenschaftenwerte anzuzeigen.

## Parameter

### -ApiVersion
Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.
Sie können eine andere Version als die Standard Version angeben.

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Gibt die ID der Ressourcengruppen Bereitstellung an, die abgerufen werden soll.

```yaml
Type: String
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
Type: String
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
Type: SwitchParameter
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
Type: String
Parameter Sets: GetByResourceGroupDeploymentName
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

### Keine

## Ausgaben

### Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroupDeployment
Das Cmdlet gibt Ressourcengruppen Bereitstellungen zurück.

## Notizen

## Verwandte Links

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[Neu – AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Neu – AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroupDeployment](./Remove-AzureRmResourceGroupDeployment.md)

[Stopp-AzureRmResourceGroupDeployment](./Stop-AzureRmResourceGroupDeployment.md)

[Test-AzureRmResourceGroupDeployment](./Test-AzureRmResourceGroupDeployment.md)


