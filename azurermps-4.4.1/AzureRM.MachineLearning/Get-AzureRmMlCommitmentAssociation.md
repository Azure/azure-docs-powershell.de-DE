---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 63c0184b9104b939073c4d58313777e8940d0f93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500010"
---
# <span data-ttu-id="d8b5e-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="d8b5e-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="d8b5e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b5e-103">Ruft die Zusammenfassungsinformationen für eine oder mehrere zubindungs Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8b5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8b5e-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8b5e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8b5e-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b5e-106">Ruft Informationen zu Bindungs Zuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="d8b5e-107">Je nach paramenters gibt das Cmdlet eine bestimmte zubindungs Zuordnung oder eine Sammlung von zubindungs Zuordnungen für den angegebenen Verpflichtungs Plan zurück.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="d8b5e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8b5e-108">EXAMPLES</span></span>

### <span data-ttu-id="d8b5e-109">--------------------------Beispiel 1: Abrufen einer bestimmten Verpflichtungs Zuordnung--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8b5e-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
<span data-ttu-id="d8b5e-110">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="d8b5e-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="d8b5e-111">--------------------------Beispiel 2: Abrufen aller zubindungs Zuordnungen für den angegebenen obligoplan--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8b5e-111">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
<span data-ttu-id="d8b5e-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="d8b5e-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="d8b5e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8b5e-113">PARAMETERS</span></span>

### <span data-ttu-id="d8b5e-114">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="d8b5e-114">-CommitmentPlanName</span></span>
<span data-ttu-id="d8b5e-115">Der Name des Azure-ml-obligoplan, der eine oder mehrere zubindungs Zuordnungen enthält.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-115">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="d8b5e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d8b5e-116">-Name</span></span>
<span data-ttu-id="d8b5e-117">Der Name der Azure ml Commitment Association.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="d8b5e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b5e-118">-ResourceGroupName</span></span>
<span data-ttu-id="d8b5e-119">Der Name der Ressourcengruppe für die Azure ml Commitment Association.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="d8b5e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b5e-120">-DefaultProfile</span></span>
<span data-ttu-id="d8b5e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8b5e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b5e-122">CommonParameters</span></span>
<span data-ttu-id="d8b5e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b5e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b5e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b5e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b5e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8b5e-125">INPUTS</span></span>

## <span data-ttu-id="d8b5e-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8b5e-126">OUTPUTS</span></span>

### <span data-ttu-id="d8b5e-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d8b5e-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="d8b5e-128">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="d8b5e-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="d8b5e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8b5e-129">NOTES</span></span>
<span data-ttu-id="d8b5e-130">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d8b5e-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d8b5e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8b5e-131">RELATED LINKS</span></span>

