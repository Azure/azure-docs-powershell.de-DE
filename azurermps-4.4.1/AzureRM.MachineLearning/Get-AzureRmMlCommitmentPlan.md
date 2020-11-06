---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 9f9789d288773b16b2003e23b00674c12ca08738
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500009"
---
# Get-AzureRmMlCommitmentPlan

## Synopsis
Ruft die Zusammenfassungsinformationen für einen oder mehrere Verpflichtungs Pläne ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Ruft Informationen zum Verpflichtungs Plan ab.
Je nach paramenters gibt das Cmdlet einen bestimmten Zustellungs Plan, eine Sammlung von Verpflichtungs Plänen für eine bestimmte Ressourcengruppe innerhalb des aktuellen Abonnements oder eine Sammlung von Verpflichtungs Plänen innerhalb des aktuellen Abonnements zurück.

## Beispiele

### --------------------------Beispiel 1: Abrufen eines bestimmten Verpflichtungs Plans--------------------------
@ {Paragraph = PS C: \\ \> }





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### --------------------------Beispiel 2: Abrufen aller Ressourcen für den obligoplan im aktuellen Abonnement--------------------------
@ {Paragraph = PS C: \\ \> }





```
Get-AzureRmMlCommitmentPlan
```

### --------------------------Beispiel 3: Abrufen aller Verpflichtungs Pläne im aktuellen Abonnement und in der angegebenen Ressourcengruppe--------------------------
@ {Paragraph = PS C: \\ \> }





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## Parameter

### -Name
Der Name des obligoplan.

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

### -ResourceGroupName
Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.

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

## Ausgaben

### Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan
Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []

## Notizen
Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml

## Verwandte Links

