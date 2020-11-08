---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166373"
---
# <span data-ttu-id="b7b87-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b7b87-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="b7b87-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7b87-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b87-103">Ruft die Zusammenfassungsinformationen für einen oder mehrere Verpflichtungs Pläne ab.</span><span class="sxs-lookup"><span data-stu-id="b7b87-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="b7b87-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7b87-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7b87-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7b87-105">DESCRIPTION</span></span>
<span data-ttu-id="b7b87-106">Ruft Informationen zum Verpflichtungs Plan ab.</span><span class="sxs-lookup"><span data-stu-id="b7b87-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="b7b87-107">Je nach den übergebenen Parametern gibt das Cmdlet einen bestimmten Zustellungs Plan, eine Sammlung von Verpflichtungs Plänen für eine bestimmte Ressourcengruppe innerhalb des aktuellen Abonnements oder eine Sammlung von Zusage Plänen innerhalb des aktuellen Abonnements zurück.</span><span class="sxs-lookup"><span data-stu-id="b7b87-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="b7b87-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7b87-108">EXAMPLES</span></span>

### <span data-ttu-id="b7b87-109">Beispiel 1: Abrufen eines bestimmten Verpflichtungs Plans</span><span class="sxs-lookup"><span data-stu-id="b7b87-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="b7b87-110">Beispiel 2: Abrufen aller Ressourcen für den obligoplan im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="b7b87-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="b7b87-111">Beispiel 3: Abrufen aller Verpflichtungs Pläne im aktuellen Abonnement und in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b7b87-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="b7b87-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7b87-112">PARAMETERS</span></span>

### <span data-ttu-id="b7b87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b87-113">-DefaultProfile</span></span>
<span data-ttu-id="b7b87-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b7b87-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7b87-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b7b87-115">-Name</span></span>
<span data-ttu-id="b7b87-116">Der Name des obligoplan.</span><span class="sxs-lookup"><span data-stu-id="b7b87-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="b7b87-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7b87-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7b87-118">Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="b7b87-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b7b87-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b87-119">CommonParameters</span></span>
<span data-ttu-id="b7b87-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b87-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b87-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b87-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b87-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7b87-122">INPUTS</span></span>

### <span data-ttu-id="b7b87-123">Keine</span><span class="sxs-lookup"><span data-stu-id="b7b87-123">None</span></span>

## <span data-ttu-id="b7b87-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7b87-124">OUTPUTS</span></span>

### <span data-ttu-id="b7b87-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b7b87-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="b7b87-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7b87-126">NOTES</span></span>
<span data-ttu-id="b7b87-127">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="b7b87-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b7b87-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7b87-128">RELATED LINKS</span></span>
