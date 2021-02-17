---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147572"
---
# <span data-ttu-id="871e8-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="871e8-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="871e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="871e8-102">SYNOPSIS</span></span>
<span data-ttu-id="871e8-103">Ruft die zusammenfassenden Informationen für einen oder mehrere Verpflichtungspläne ab.</span><span class="sxs-lookup"><span data-stu-id="871e8-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="871e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="871e8-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="871e8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="871e8-105">DESCRIPTION</span></span>
<span data-ttu-id="871e8-106">Ruft Informationen zum Verpflichtungsplan ab.</span><span class="sxs-lookup"><span data-stu-id="871e8-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="871e8-107">Je nach den übergebenen Parametern gibt das Cmdlet einen bestimmten Verpflichtungsplan, eine Sammlung von Verpflichtungsplänen für eine bestimmte Ressourcengruppe im aktuellen Abonnement oder eine Sammlung von Verpflichtungsplänen im aktuellen Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="871e8-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="871e8-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="871e8-108">EXAMPLES</span></span>

### <span data-ttu-id="871e8-109">Beispiel 1: Erhalten eines bestimmten Verpflichtungsplans</span><span class="sxs-lookup"><span data-stu-id="871e8-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="871e8-110">Beispiel 2: Alle Ressourcen des Verpflichtungsplans im aktuellen Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="871e8-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="871e8-111">Beispiel 3: Alle Verpflichtungspläne im aktuellen Abonnement und der angegebenen Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="871e8-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="871e8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="871e8-112">PARAMETERS</span></span>

### <span data-ttu-id="871e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871e8-113">-DefaultProfile</span></span>
<span data-ttu-id="871e8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="871e8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="871e8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="871e8-115">-Name</span></span>
<span data-ttu-id="871e8-116">Der Name des Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="871e8-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="871e8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="871e8-117">-ResourceGroupName</span></span>
<span data-ttu-id="871e8-118">Der Name der Ressourcengruppe für den Azure ML-Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="871e8-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="871e8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871e8-119">CommonParameters</span></span>
<span data-ttu-id="871e8-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="871e8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871e8-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="871e8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871e8-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="871e8-122">INPUTS</span></span>

### <span data-ttu-id="871e8-123">Keine</span><span class="sxs-lookup"><span data-stu-id="871e8-123">None</span></span>

## <span data-ttu-id="871e8-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="871e8-124">OUTPUTS</span></span>

### <span data-ttu-id="871e8-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="871e8-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="871e8-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="871e8-126">NOTES</span></span>
<span data-ttu-id="871e8-127">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="871e8-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="871e8-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="871e8-128">RELATED LINKS</span></span>
