---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 5404cf82308c63a5ba6fe07ef4ac01101f44c48c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664650"
---
# <span data-ttu-id="ecdc4-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ecdc4-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="ecdc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecdc4-102">SYNOPSIS</span></span>
<span data-ttu-id="ecdc4-103">Ruft die Zusammenfassungsinformationen für einen oder mehrere Verpflichtungs Pläne ab.</span><span class="sxs-lookup"><span data-stu-id="ecdc4-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecdc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecdc4-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecdc4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecdc4-105">DESCRIPTION</span></span>
<span data-ttu-id="ecdc4-106">Ruft Informationen zum Verpflichtungs Plan ab.</span><span class="sxs-lookup"><span data-stu-id="ecdc4-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="ecdc4-107">Je nach paramenters gibt das Cmdlet einen bestimmten Zustellungs Plan, eine Sammlung von Verpflichtungs Plänen für eine bestimmte Ressourcengruppe innerhalb des aktuellen Abonnements oder eine Sammlung von Verpflichtungs Plänen innerhalb des aktuellen Abonnements zurück.</span><span class="sxs-lookup"><span data-stu-id="ecdc4-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="ecdc4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecdc4-108">EXAMPLES</span></span>

### <span data-ttu-id="ecdc4-109">--------------------------Beispiel 1: Abrufen eines bestimmten Verpflichtungs Plans--------------------------</span><span class="sxs-lookup"><span data-stu-id="ecdc4-109">--------------------------  Example 1: Get a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="ecdc4-110">--------------------------Beispiel 2: Abrufen aller Ressourcen für den obligoplan im aktuellen Abonnement--------------------------</span><span class="sxs-lookup"><span data-stu-id="ecdc4-110">--------------------------  Example 2: Get all commitment plan resources in current subscription  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="ecdc4-111">--------------------------Beispiel 3: Abrufen aller Verpflichtungs Pläne im aktuellen Abonnement und in der angegebenen Ressourcengruppe--------------------------</span><span class="sxs-lookup"><span data-stu-id="ecdc4-111">--------------------------  Example 3: Get all commitment plans in the current subscription and given resource group  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="ecdc4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecdc4-112">PARAMETERS</span></span>

### <span data-ttu-id="ecdc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecdc4-113">-DefaultProfile</span></span>
<span data-ttu-id="ecdc4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ecdc4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdc4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ecdc4-115">-Name</span></span>
<span data-ttu-id="ecdc4-116">Der Name des obligoplan.</span><span class="sxs-lookup"><span data-stu-id="ecdc4-116">The name of the commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdc4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecdc4-117">-ResourceGroupName</span></span>
<span data-ttu-id="ecdc4-118">Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="ecdc4-118">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdc4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecdc4-119">CommonParameters</span></span>
<span data-ttu-id="ecdc4-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecdc4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecdc4-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecdc4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecdc4-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecdc4-122">INPUTS</span></span>

### <span data-ttu-id="ecdc4-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ecdc4-123">None</span></span>
<span data-ttu-id="ecdc4-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ecdc4-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ecdc4-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecdc4-125">OUTPUTS</span></span>

### <span data-ttu-id="ecdc4-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ecdc4-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="ecdc4-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="ecdc4-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="ecdc4-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecdc4-128">NOTES</span></span>
<span data-ttu-id="ecdc4-129">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ecdc4-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ecdc4-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecdc4-130">RELATED LINKS</span></span>

