---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300171"
---
# <span data-ttu-id="f708a-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="f708a-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="f708a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f708a-102">SYNOPSIS</span></span>
<span data-ttu-id="f708a-103">Ruft Informationen zum Nutzungsverlauf für einen angegebenen Verpflichtungsplan ab.</span><span class="sxs-lookup"><span data-stu-id="f708a-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="f708a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f708a-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f708a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f708a-105">DESCRIPTION</span></span>
<span data-ttu-id="f708a-106">Ruft Informationen zum Nutzungsverlauf für einen bestimmten Verpflichtungsplan ab, einschließlich der verwendeten Ressourcen und der im Plan verbleibenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="f708a-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="f708a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f708a-107">EXAMPLES</span></span>

### <span data-ttu-id="f708a-108">Beispiel 1: Nutzungsverlauf für einen bestimmten Verpflichtungsplan erhalten</span><span class="sxs-lookup"><span data-stu-id="f708a-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="f708a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f708a-109">PARAMETERS</span></span>

### <span data-ttu-id="f708a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f708a-110">-DefaultProfile</span></span>
<span data-ttu-id="f708a-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f708a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f708a-112">-Name</span><span class="sxs-lookup"><span data-stu-id="f708a-112">-Name</span></span>
<span data-ttu-id="f708a-113">Der Name des Azure ML-Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="f708a-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f708a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f708a-114">-ResourceGroupName</span></span>
<span data-ttu-id="f708a-115">Der Name der Ressourcengruppe für den Azure ML-Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="f708a-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f708a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f708a-116">CommonParameters</span></span>
<span data-ttu-id="f708a-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f708a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f708a-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f708a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f708a-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f708a-119">INPUTS</span></span>

### <span data-ttu-id="f708a-120">Keine</span><span class="sxs-lookup"><span data-stu-id="f708a-120">None</span></span>

## <span data-ttu-id="f708a-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f708a-121">OUTPUTS</span></span>

### <span data-ttu-id="f708a-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="f708a-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="f708a-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f708a-123">NOTES</span></span>
<span data-ttu-id="f708a-124">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f708a-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f708a-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f708a-125">RELATED LINKS</span></span>
