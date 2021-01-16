---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293675"
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
Wenn in der Ressourcengruppe ein Webdienst mit demselben Namen vorhanden ist, fungiert der Aufruf als Aktualisierungsvorgang, und der vorhandene Webdienst wird überschrieben.

## BEISPIELE

### Beispiel 1: Erstellen eines neuen Diensts aus einer Json-Datei-basierten Definition
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Erstellt einen neuen Azure Machine Learning-Webdienst mit dem Namen "mywebservicename" in der Gruppe "myresourcegroup" und der Region "USA, Süd-Mitte", basierend auf der Definition in der json-Datei, auf die verwiesen wird.

### Beispiel 2: Erstellen eines neuen Diensts aus einer Objektinstanz
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Sie können eine Webdienstobjektinstanz abrufen, die Sie vor der Veröffentlichung als Ressource anpassen möchten, indem Sie das cmdlet Import-AzMlWebService verwenden.

## PARAMETERS

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
Gibt den Pfad zu der Datei an, die die Definition des JSON-Formats des Webdiensts enthält.
Die neueste Spezifikation für die Webdienstdefinition finden Sie in der "swagger"-Spezifikation https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning unter.

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

### -Force
Fordern Sie keine Bestätigung an.

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
Geben Sie eine Region für das Azure-Rechenzentrum ein, z. B. "Usa, Westen" oder "Südostasien".
Sie können einen Webdienst in einer beliebigen Region platzieren, die Ressourcen dieses Typs unterstützt.
Der Webdienst muss sich nicht in derselben Region wie Ihr Abonnement oder in derselben Region wie die Ressourcengruppe der Gruppe der Ressourcen enthalten.
Ressourcengruppen können Webdienste aus unterschiedlichen Regionen enthalten.
Um festzustellen, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Sie die Get-AzResourceProvider mit dem Cmdlet für den ProviderNamespace-Parameter.

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
Der Name des Webdiensts.
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
Die Definition für den neuen Webdienst, die alle Eigenschaften enthält, aus denen der Dienst wird.
Dieser Parameter ist erforderlich und stellt eine Instanz der Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService-Klasse dar.
Die neueste Spezifikation für die Webdienstdefinition finden Sie in der "swagger"-Spezifikation https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json unter.

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
Die Ressourcengruppe, in der der Webdienst platzieren werden soll.
Geben Sie eine Region für das Azure-Rechenzentrum ein, z. B. "Usa, Westen" oder "Südostasien".
Sie können einen Webdienst in einer beliebigen Region platzieren, die Ressourcen dieses Typs unterstützt.
Der Webdienst muss sich nicht in derselben Region wie Ihr Abonnement oder in derselben Region wie die Ressourcengruppe der Gruppe der Ressourcen enthalten.
Ressourcengruppen können Webdienste aus unterschiedlichen Regionen enthalten.
Um festzustellen, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Sie die Get-AzResourceProvider mit dem Cmdlet für den ProviderNamespace-Parameter.

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

### -Confirm
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

### -Waswenn
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## AUSGABEN

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## HINWEISE
Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml

## LINKS ZU VERWANDTEN THEMEN
