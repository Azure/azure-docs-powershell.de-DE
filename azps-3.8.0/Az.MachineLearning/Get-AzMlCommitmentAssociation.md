---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002994"
---
# <span data-ttu-id="2bd65-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="2bd65-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="2bd65-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bd65-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd65-103">Ruft die Zusammenfassungsinformationen für eine oder mehrere zubindungs Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="2bd65-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="2bd65-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bd65-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bd65-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bd65-105">DESCRIPTION</span></span>
<span data-ttu-id="2bd65-106">Ruft Informationen zu Bindungs Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="2bd65-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="2bd65-107">Je nach den übergebenen Parametern gibt das Cmdlet eine bestimmte zubindungs Zuordnung oder eine Sammlung von zubindungs Zuordnungen für den angegebenen Verpflichtungs Plan zurück.</span><span class="sxs-lookup"><span data-stu-id="2bd65-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="2bd65-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bd65-108">EXAMPLES</span></span>

### <span data-ttu-id="2bd65-109">Beispiel 1: Abrufen einer bestimmten Verpflichtungs Zuordnung</span><span class="sxs-lookup"><span data-stu-id="2bd65-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="2bd65-110">Beispiel 2: Abrufen aller zubindungs Zuordnungen für den angegebenen obligoplan</span><span class="sxs-lookup"><span data-stu-id="2bd65-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="2bd65-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bd65-111">PARAMETERS</span></span>

### <span data-ttu-id="2bd65-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="2bd65-112">-CommitmentPlanName</span></span>
<span data-ttu-id="2bd65-113">Der Name des Azure-ml-obligoplan, der eine oder mehrere zubindungs Zuordnungen enthält.</span><span class="sxs-lookup"><span data-stu-id="2bd65-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="2bd65-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd65-114">-DefaultProfile</span></span>
<span data-ttu-id="2bd65-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2bd65-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2bd65-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2bd65-116">-Name</span></span>
<span data-ttu-id="2bd65-117">Der Name der Azure ml Commitment Association.</span><span class="sxs-lookup"><span data-stu-id="2bd65-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="2bd65-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd65-118">-ResourceGroupName</span></span>
<span data-ttu-id="2bd65-119">Der Name der Ressourcengruppe für die Azure ml Commitment Association.</span><span class="sxs-lookup"><span data-stu-id="2bd65-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="2bd65-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd65-120">CommonParameters</span></span>
<span data-ttu-id="2bd65-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd65-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd65-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd65-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd65-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bd65-123">INPUTS</span></span>

### <span data-ttu-id="2bd65-124">Keine</span><span class="sxs-lookup"><span data-stu-id="2bd65-124">None</span></span>

## <span data-ttu-id="2bd65-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bd65-125">OUTPUTS</span></span>

### <span data-ttu-id="2bd65-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="2bd65-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="2bd65-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bd65-127">NOTES</span></span>
<span data-ttu-id="2bd65-128">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="2bd65-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2bd65-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bd65-129">RELATED LINKS</span></span>
