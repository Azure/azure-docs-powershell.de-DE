---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/move-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 2bd650e86a1a4b59694dc88dc915da0fd7713e5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505497"
---
# <span data-ttu-id="120ac-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="120ac-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="120ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="120ac-102">SYNOPSIS</span></span>
<span data-ttu-id="120ac-103">Verschiebt eine zubindungs Zuordnung von einem obligoplan in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="120ac-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="120ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="120ac-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="120ac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="120ac-105">DESCRIPTION</span></span>
<span data-ttu-id="120ac-106">Verschiebt eine Obligo-Zuordnungs Ressource aus dem übergeordneten obligoplan in einen anderen Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="120ac-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="120ac-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="120ac-107">EXAMPLES</span></span>

### <span data-ttu-id="120ac-108">--------------------------Beispiel 1: Verschieben einer Verpflichtungs Zuordnung--------------------------</span><span class="sxs-lookup"><span data-stu-id="120ac-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="120ac-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="120ac-109">PARAMETERS</span></span>

### <span data-ttu-id="120ac-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="120ac-110">-CommitmentPlanName</span></span>
<span data-ttu-id="120ac-111">Der Name des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="120ac-111">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120ac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="120ac-112">-DefaultProfile</span></span>
<span data-ttu-id="120ac-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="120ac-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="120ac-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="120ac-114">-DestinationPlanId</span></span>
<span data-ttu-id="120ac-115">Die Azure-Ressourcen-ID des Ziels Azure ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="120ac-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120ac-116">-Name</span><span class="sxs-lookup"><span data-stu-id="120ac-116">-Name</span></span>
<span data-ttu-id="120ac-117">Der Name der Azure ml Commitment Association.</span><span class="sxs-lookup"><span data-stu-id="120ac-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120ac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="120ac-118">-ResourceGroupName</span></span>
<span data-ttu-id="120ac-119">Der Name der Ressourcengruppe für die Azure ml Commitment Association.</span><span class="sxs-lookup"><span data-stu-id="120ac-119">The name of the resource group for the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120ac-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="120ac-120">-Confirm</span></span>
<span data-ttu-id="120ac-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="120ac-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120ac-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="120ac-122">-WhatIf</span></span>
<span data-ttu-id="120ac-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="120ac-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="120ac-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="120ac-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120ac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120ac-125">CommonParameters</span></span>
<span data-ttu-id="120ac-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="120ac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120ac-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="120ac-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120ac-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="120ac-128">INPUTS</span></span>

### <span data-ttu-id="120ac-129">Keine</span><span class="sxs-lookup"><span data-stu-id="120ac-129">None</span></span>
<span data-ttu-id="120ac-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="120ac-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="120ac-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="120ac-131">OUTPUTS</span></span>

### <span data-ttu-id="120ac-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="120ac-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="120ac-133">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="120ac-133">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="120ac-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="120ac-134">NOTES</span></span>
<span data-ttu-id="120ac-135">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="120ac-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="120ac-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="120ac-136">RELATED LINKS</span></span>

