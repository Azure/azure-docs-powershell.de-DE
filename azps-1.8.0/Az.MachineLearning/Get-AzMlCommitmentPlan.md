---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 0b66c75c3230754656b14e15eda66a4fb2912c4d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819215"
---
# <span data-ttu-id="6e3ae-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="6e3ae-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="6e3ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e3ae-102">SYNOPSIS</span></span>
<span data-ttu-id="6e3ae-103">Ruft die Zusammenfassungsinformationen für einen oder mehrere Verpflichtungs Pläne ab.</span><span class="sxs-lookup"><span data-stu-id="6e3ae-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="6e3ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e3ae-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e3ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e3ae-105">DESCRIPTION</span></span>
<span data-ttu-id="6e3ae-106">Ruft Informationen zum Verpflichtungs Plan ab.</span><span class="sxs-lookup"><span data-stu-id="6e3ae-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="6e3ae-107">Je nach paramenters gibt das Cmdlet einen bestimmten Zustellungs Plan, eine Sammlung von Verpflichtungs Plänen für eine bestimmte Ressourcengruppe innerhalb des aktuellen Abonnements oder eine Sammlung von Verpflichtungs Plänen innerhalb des aktuellen Abonnements zurück.</span><span class="sxs-lookup"><span data-stu-id="6e3ae-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="6e3ae-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e3ae-108">EXAMPLES</span></span>

### <span data-ttu-id="6e3ae-109">Beispiel 1: Abrufen eines bestimmten Verpflichtungs Plans</span><span class="sxs-lookup"><span data-stu-id="6e3ae-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="6e3ae-110">Beispiel 2: Abrufen aller Ressourcen für den obligoplan im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6e3ae-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="6e3ae-111">Beispiel 3: Abrufen aller Verpflichtungs Pläne im aktuellen Abonnement und in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6e3ae-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="6e3ae-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e3ae-112">PARAMETERS</span></span>

### <span data-ttu-id="6e3ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e3ae-113">-DefaultProfile</span></span>
<span data-ttu-id="6e3ae-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6e3ae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e3ae-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6e3ae-115">-Name</span></span>
<span data-ttu-id="6e3ae-116">Der Name des obligoplan.</span><span class="sxs-lookup"><span data-stu-id="6e3ae-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="6e3ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e3ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="6e3ae-118">Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="6e3ae-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6e3ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e3ae-119">CommonParameters</span></span>
<span data-ttu-id="6e3ae-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e3ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e3ae-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e3ae-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e3ae-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e3ae-122">INPUTS</span></span>

### <span data-ttu-id="6e3ae-123">Keine</span><span class="sxs-lookup"><span data-stu-id="6e3ae-123">None</span></span>

## <span data-ttu-id="6e3ae-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e3ae-124">OUTPUTS</span></span>

### <span data-ttu-id="6e3ae-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="6e3ae-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="6e3ae-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e3ae-126">NOTES</span></span>
<span data-ttu-id="6e3ae-127">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="6e3ae-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6e3ae-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e3ae-128">RELATED LINKS</span></span>
