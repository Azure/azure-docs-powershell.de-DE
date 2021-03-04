---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 1a48438d6cec1621361a00cefa2bfead28117b97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922896"
---
# New-AzMlWebService

## SYNOPSIS
Erstellt einen neuen Webdienst.

## SYNTAX

### CreateFromFile
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromInstance
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Erstellt einen Azure Machine Learning-Webdienst in einer vorhandenen Ressourcengruppe.
Wenn ein Webdienst mit demselben Namen in der Ressourcengruppe vorhanden ist, fungiert der Aufruf als Aktualisierungsvorgang, und der vorhandene Webdienst wird überschrieben.

## BEISPIELE

### Beispiel 1: Erstellen eines neuen Diensts aus einer Json-dateibasierten Definition
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Erstellt einen neuen Azure Machine Learning-Webdienst mit dem Namen "mywebservicename" in der Gruppe "myresourcegroup" und der Region "South Central US", basierend auf der Definition, die in der json-Datei auf referenziert ist.

### Beispiel 2: Erstellen eines neuen Diensts aus einer Objektinstanz
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Sie können eine Webdienstobjektinstanz abrufen, die Sie vor der Veröffentlichung als Ressource anpassen möchten, indem Sie das cmdlet Import-AzMlWebService verwenden.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -DefinitionFile
Gibt den Pfad zu der Datei an, der die JSON-Formatdefinition des Webdiensts enthält.
Die neueste Spezifikation für die Webdienstdefinition finden Sie in der Swaggerspezifikation unter https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Erzwingen
Bitten Sie nicht um Bestätigung.

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

### -Location
Die Region des Webdiensts.
Geben Sie eine Azure-Rechenzentrumsregion ein, z. B. "West US" oder "Südostasien".
Sie können einen Webdienst in einer beliebigen Region platzieren, die Ressourcen dieses Typs unterstützt.
Der Webdienst muss sich nicht in derselben Region wie Ihr Azure-Abonnement oder in derselben Region wie seine Ressourcengruppe enthalten.
Ressourcengruppen können Webdienste aus verschiedenen Regionen enthalten.
Um zu ermitteln, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Get-AzResourceProvider mit dem Cmdlet für den ProviderNamespace-Parameter.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name für den Webdienst.
Der Name muss in der Ressourcengruppe eindeutig sein.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewWebServiceDefinition
Die Definition für den neuen Webdienst, die alle Eigenschaften enthält, aus denen der Dienst ist.
Dieser Parameter ist erforderlich und stellt eine Instanz der Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService-Klasse dar.
Die neueste Spezifikation für die Webdienstdefinition finden Sie in der Swaggerspezifikation unter https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe, in der der Webdienst zu platzieren ist.
Geben Sie eine Azure-Rechenzentrumsregion ein, z. B. "West US" oder "Südostasien".
Sie können einen Webdienst in einer beliebigen Region platzieren, die Ressourcen dieses Typs unterstützt.
Der Webdienst muss sich nicht in derselben Region wie Ihr Azure-Abonnement oder in derselben Region wie seine Ressourcengruppe enthalten.
Ressourcengruppen können Webdienste aus verschiedenen Regionen enthalten.
Um zu ermitteln, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Get-AzResourceProvider mit dem Cmdlet für den ProviderNamespace-Parameter.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
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

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## AUSGABEN

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## NOTIZEN
Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml

## VERWANDTE LINKS
