---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: 1fe6476836622445337ea0b4741b361504a57302
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504890"
---
# New-AzureRmMlWebService

## Synopsis
Erstellt einen neuen Webdienst.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Erstellen Sie einen neuen Azure ml-Webservice aus einer JSON-Definition-Datei.
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Erstellen Sie einen neuen Azure-ml-Webservice aus einer Webservice-Instanzen Definition.
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Erstellt einen Azure Machine Learning-Webdienst in einer vorhandenen Ressourcengruppe.
Wenn ein Webdienst mit demselben Namen in der Ressourcengruppe vorhanden ist, fungiert der Anruf als Aktualisierungsvorgang, und der vorhandene Webdienst wird überschrieben.

## Beispiele

### --------------------------Beispiel 1: Erstellen eines neuen Diensts aus einer JSON-dateibasierten Definition--------------------------
@ {Paragraph = PS C: \\ \> }





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Erstellt einen neuen Azure Machine Learning-Webdienst mit dem Namen "mywebservicename" in der Gruppe "myresourcegroup" und der Region Süd-Zentralamerika, basierend auf der in der referenzierten JSON-Datei vorhandenen Definition.

### --------------------------Beispiel 2: Erstellen eines neuen Diensts aus einer Objektinstanz--------------------------
@ {Paragraph = PS C: \\ \> }





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Sie können eine Webdienst-Objektinstanz abrufen, um Sie vor der Veröffentlichung als Ressource mithilfe des Import-AzureRmMlWebService-Cmdlets anzupassen.

## Parameter

### -Definitions-Nr.
Gibt an der Pfad zu der Datei, die die JSON-Formatdefinition des Webdiensts enthält.
Die neueste Spezifikation für die Webdienstdefinition finden Sie in der Prahlerei-Spezifikation unter https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

```yaml
Type: System.String
Parameter Sets: Create a new Azure ML webservice from a JSON definiton file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Keine Bestätigung anfordern.

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

### -Standort
Der Bereich des Webdiensts.
Geben Sie einen Azure Data Center-Bereich ein, beispielsweise "West USA" oder "Südostasien".
Sie können einen Webdienst in jeder Region platzieren, die Ressourcen dieses Typs unterstützt.
Der Webdienst muss sich nicht im gleichen Bereich Ihres Azure-Abonnements oder der gleichen Region wie seine Ressourcengruppe befinden.
Ressourcengruppen können Webdienste aus verschiedenen Regionen enthalten.
Wenn Sie ermitteln möchten, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Sie die Get-AzureRmResourceProvider mit dem Cmdlet ProviderNamespace-Parameter.

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
Die Definition für den neuen Webdienst, die alle Eigenschaften enthält, aus denen sich der Dienst besteht.
Dieser Parameter ist erforderlich und stellt eine Instanz der Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService-Klasse dar.
Die neueste Spezifikation für die Webdienstdefinition finden Sie in der Prahlerei-Spezifikation unter https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe, in der der Webdienst platziert werden soll.
Geben Sie einen Azure Data Center-Bereich ein, beispielsweise "West USA" oder "Südostasien".
Sie können einen Webdienst in jeder Region platzieren, die Ressourcen dieses Typs unterstützt.
Der Webdienst muss sich nicht im gleichen Bereich Ihres Azure-Abonnements oder der gleichen Region wie seine Ressourcengruppe befinden.
Ressourcengruppen können Webdienste aus verschiedenen Regionen enthalten.
Wenn Sie ermitteln möchten, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Sie die Get-AzureRmResourceProvider mit dem Cmdlet ProviderNamespace-Parameter.

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
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Webservice
Der Parameter "NewWebServiceDefinition" akzeptiert den Wert vom Typ "Webservice" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService
Eine zusammenfassende Beschreibung des Azure Machine Learning-Webdiensts.
Ähnlich wie die Beschreibung, die durch Aufrufen des Get-AzureRmMlWebService-Cmdlets für einen vorhandenen Webdienst zurückgegeben wird.
Diese Beschreibung enthält keine vertraulichen Eigenschaften wie die Anmeldeinformationen des speicherkontos und die Zugriffstasten des Diensts.

## Notizen
Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml

## Verwandte Links

