---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 84c1560cf4d97f7a40735d767c2c4d82fcd7d65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504893"
---
# <span data-ttu-id="3da31-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="3da31-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="3da31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3da31-102">SYNOPSIS</span></span>
<span data-ttu-id="3da31-103">Verschiebt eine zubindungs Zuordnung von einem obligoplan in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="3da31-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3da31-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3da31-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3da31-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3da31-105">DESCRIPTION</span></span>
<span data-ttu-id="3da31-106">Verschiebt eine Obligo-Zuordnungs Ressource aus dem übergeordneten obligoplan in einen anderen Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="3da31-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="3da31-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3da31-107">EXAMPLES</span></span>

### <span data-ttu-id="3da31-108">--------------------------Beispiel 1: Verschieben einer Verpflichtungs Zuordnung--------------------------</span><span class="sxs-lookup"><span data-stu-id="3da31-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
<span data-ttu-id="3da31-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="3da31-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="3da31-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3da31-110">PARAMETERS</span></span>

### <span data-ttu-id="3da31-111">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="3da31-111">-CommitmentPlanName</span></span>
<span data-ttu-id="3da31-112">Der Name des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="3da31-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3da31-113">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="3da31-113">-DestinationPlanId</span></span>
<span data-ttu-id="3da31-114">Die Azure-Ressourcen-ID des Ziels Azure ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="3da31-114">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3da31-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3da31-115">-Name</span></span>
<span data-ttu-id="3da31-116">Der Name der Azure ml Commitment Association.</span><span class="sxs-lookup"><span data-stu-id="3da31-116">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="3da31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3da31-117">-ResourceGroupName</span></span>
<span data-ttu-id="3da31-118">Der Name der Ressourcengruppe für die Azure ml Commitment Association.</span><span class="sxs-lookup"><span data-stu-id="3da31-118">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="3da31-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3da31-119">-Confirm</span></span>
<span data-ttu-id="3da31-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3da31-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3da31-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3da31-121">-WhatIf</span></span>
<span data-ttu-id="3da31-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3da31-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3da31-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3da31-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3da31-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da31-124">-DefaultProfile</span></span>
<span data-ttu-id="3da31-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3da31-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3da31-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da31-126">CommonParameters</span></span>
<span data-ttu-id="3da31-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3da31-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da31-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3da31-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da31-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3da31-129">INPUTS</span></span>

## <span data-ttu-id="3da31-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3da31-130">OUTPUTS</span></span>

### <span data-ttu-id="3da31-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3da31-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="3da31-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="3da31-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="3da31-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="3da31-133">NOTES</span></span>
<span data-ttu-id="3da31-134">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="3da31-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3da31-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3da31-135">RELATED LINKS</span></span>

