---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 8baf0e2af5ebc06e51c0f8b588fe04ff3106f892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947427"
---
# <span data-ttu-id="f9b14-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="f9b14-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="f9b14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9b14-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b14-103">Ruft Informationen zum Nutzungsverlauf für einen angegebenen Verpflichtungsplan ab.</span><span class="sxs-lookup"><span data-stu-id="f9b14-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="f9b14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9b14-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9b14-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9b14-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b14-106">Ruft Nutzungshistorieinformationen für einen angegebenen Verpflichtungsplan ab, einschließlich der verwendeten Ressourcen und der im Plan verbleibenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="f9b14-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="f9b14-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f9b14-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b14-108">Beispiel 1: Nutzungsverlauf für einen bestimmten Verpflichtungsplan erhalten</span><span class="sxs-lookup"><span data-stu-id="f9b14-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="f9b14-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f9b14-109">PARAMETERS</span></span>

### <span data-ttu-id="f9b14-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b14-110">-DefaultProfile</span></span>
<span data-ttu-id="f9b14-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f9b14-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9b14-112">-Name</span><span class="sxs-lookup"><span data-stu-id="f9b14-112">-Name</span></span>
<span data-ttu-id="f9b14-113">Der Name des Azure ML-Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="f9b14-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f9b14-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b14-114">-ResourceGroupName</span></span>
<span data-ttu-id="f9b14-115">Der Name der Ressourcengruppe für den Azure ML-Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="f9b14-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f9b14-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b14-116">CommonParameters</span></span>
<span data-ttu-id="f9b14-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b14-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b14-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9b14-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b14-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f9b14-119">INPUTS</span></span>

### <span data-ttu-id="f9b14-120">Keine</span><span class="sxs-lookup"><span data-stu-id="f9b14-120">None</span></span>

## <span data-ttu-id="f9b14-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f9b14-121">OUTPUTS</span></span>

### <span data-ttu-id="f9b14-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="f9b14-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="f9b14-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f9b14-123">NOTES</span></span>
<span data-ttu-id="f9b14-124">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f9b14-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f9b14-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f9b14-125">RELATED LINKS</span></span>
