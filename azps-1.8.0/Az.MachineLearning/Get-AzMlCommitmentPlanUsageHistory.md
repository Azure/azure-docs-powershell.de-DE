---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 4d78d6e6a1b0ae5ea9f8815d537bca1496e24bbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819203"
---
# <span data-ttu-id="032d5-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="032d5-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="032d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="032d5-102">SYNOPSIS</span></span>
<span data-ttu-id="032d5-103">Ruft Nutzungs Verlaufsinformationen für einen angegebenen obligoplan ab.</span><span class="sxs-lookup"><span data-stu-id="032d5-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="032d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="032d5-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="032d5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="032d5-105">DESCRIPTION</span></span>
<span data-ttu-id="032d5-106">Ruft Nutzungs Verlaufsinformationen für einen angegebenen obligoplan ab, einschließlich der verwendeten Ressourcen und der im Plan verbleibenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="032d5-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="032d5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="032d5-107">EXAMPLES</span></span>

### <span data-ttu-id="032d5-108">Beispiel 1: Abrufen des Verwendungs Verlaufs für einen bestimmten Verpflichtungs Plan</span><span class="sxs-lookup"><span data-stu-id="032d5-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="032d5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="032d5-109">PARAMETERS</span></span>

### <span data-ttu-id="032d5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="032d5-110">-DefaultProfile</span></span>
<span data-ttu-id="032d5-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="032d5-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="032d5-112">-Name</span><span class="sxs-lookup"><span data-stu-id="032d5-112">-Name</span></span>
<span data-ttu-id="032d5-113">Der Name des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="032d5-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="032d5-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="032d5-114">-ResourceGroupName</span></span>
<span data-ttu-id="032d5-115">Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="032d5-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="032d5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="032d5-116">CommonParameters</span></span>
<span data-ttu-id="032d5-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="032d5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="032d5-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="032d5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="032d5-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="032d5-119">INPUTS</span></span>

### <span data-ttu-id="032d5-120">Keine</span><span class="sxs-lookup"><span data-stu-id="032d5-120">None</span></span>

## <span data-ttu-id="032d5-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="032d5-121">OUTPUTS</span></span>

### <span data-ttu-id="032d5-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="032d5-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="032d5-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="032d5-123">NOTES</span></span>
<span data-ttu-id="032d5-124">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="032d5-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="032d5-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="032d5-125">RELATED LINKS</span></span>
