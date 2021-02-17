---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 1ac0ab153177caaf080e5aa9144020ea253b8438
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172074"
---
# Get-AzResourceGroupDeploymentOperation

## SYNOPSIS
Ruft den Bereitstellungsvorgang der Ressourcengruppe ab.

## SYNTAX

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzResourceGroupDeploymentOperation"** listet alle Vorgänge auf, die Teil einer Bereitstellung waren, um Sie bei der Identifizierung und Bereitstellung genauerer Informationen zu den genauen Vorgängen zu unterstützen, die bei einer bestimmten Bereitstellung fehlgeschlagen sind.
Sie kann auch die Antwort und den Anforderungsinhalt für jeden Bereitstellungsvorgang anzeigen.
Dies sind die gleichen Informationen, die in den Bereitstellungsdetails des Portals bereitgestellt werden.
Um die Anforderung und den Antwortinhalt zu erhalten, aktivieren Sie die Einstellung beim Übermitteln einer Bereitstellung über **"New-AzResourceGroupDeployment".**
Es kann potenziell geheime Daten protokollieren und verfügbar machen, z. B. Kennwörter, die in den Ressourceneigenschafts- oder listKeys-Vorgängen verwendet werden, die beim Abrufen der **Bereitstellungsvorgänge** zurückgegeben werden.
Weitere Informationen zu dieser Einstellung und deren Aktivierung finden Sie unter New-AzResourceGroupDeployment und Debuggen ARM Vorlagenbereitstellungen.

## BEISPIELE

### Beispiel 1: Get1
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

Ruft den Bereitstellungsvorgang mit dem Namen "test" unter "Test" der Ressourcengruppe ab

## PARAMETERS

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

### -DeploymentName
Der Bereitstellungsname.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.

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
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionId
Das zu verwendende Abonnement.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## AUSGABEN

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEploymentOperation

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
