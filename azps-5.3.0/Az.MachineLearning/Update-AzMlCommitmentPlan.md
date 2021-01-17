---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 733f473ed09807c33355ac6bc22491a160e5481a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385901"
---
# <span data-ttu-id="6b6f6-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="6b6f6-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="6b6f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="6b6f6-103">Aktualisiert die Eigenschaften einer vorhandenen Verpflichtungsplanressource.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="6b6f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b6f6-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b6f6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b6f6-105">DESCRIPTION</span></span>
<span data-ttu-id="6b6f6-106">Aktualisiert eine vorhandene Verpflichtungsplanressource.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="6b6f6-107">Beachten Sie, dass die meisten Eigenschaften des Verpflichtungsplans unveränderlich sind und nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="6b6f6-108">Zu den Eigenschaften, die geändert werden können, gehören SKU (sodass Sie den Verpflichtungsplan von einer SKU zu einer anderen migrieren können) und Tags.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="6b6f6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b6f6-109">EXAMPLES</span></span>

### <span data-ttu-id="6b6f6-110">Beispiel 1: Aktualisieren eines Verpflichtungsplans</span><span class="sxs-lookup"><span data-stu-id="6b6f6-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="6b6f6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b6f6-111">PARAMETERS</span></span>

### <span data-ttu-id="6b6f6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6f6-112">-DefaultProfile</span></span>
<span data-ttu-id="6b6f6-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6b6f6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b6f6-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6b6f6-114">-Force</span></span>
<span data-ttu-id="6b6f6-115">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6f6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6b6f6-116">-Name</span></span>
<span data-ttu-id="6b6f6-117">Der Name des Azure ML-Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6b6f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b6f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="6b6f6-119">Der Name der Ressourcengruppe für den Azure ML-Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6b6f6-120">-Sku1</span><span class="sxs-lookup"><span data-stu-id="6b6f6-120">-SkuCapacity</span></span>
<span data-ttu-id="6b6f6-121">Die Kapazität der SKU, die beim Aktualisieren des Azure ML-Verpflichtungsplans verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6f6-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6b6f6-122">-SkuName</span></span>
<span data-ttu-id="6b6f6-123">Der Name der SKU, die beim Aktualisieren des Azure ML-Verpflichtungsplans verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6b6f6-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6b6f6-124">-SkuTier</span></span>
<span data-ttu-id="6b6f6-125">Die Stufe der SKU, die beim Aktualisieren des Azure ML-Verpflichtungsplans verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6b6f6-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b6f6-126">-Tag</span></span>
<span data-ttu-id="6b6f6-127">Tags für die Ressourcen des Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6f6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b6f6-128">-Confirm</span></span>
<span data-ttu-id="6b6f6-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b6f6-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6b6f6-130">-WhatIf</span></span>
<span data-ttu-id="6b6f6-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b6f6-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b6f6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6f6-133">CommonParameters</span></span>
<span data-ttu-id="6b6f6-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b6f6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b6f6-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b6f6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6f6-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b6f6-136">INPUTS</span></span>

### <span data-ttu-id="6b6f6-137">Keine</span><span class="sxs-lookup"><span data-stu-id="6b6f6-137">None</span></span>

## <span data-ttu-id="6b6f6-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b6f6-138">OUTPUTS</span></span>

### <span data-ttu-id="6b6f6-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="6b6f6-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="6b6f6-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6b6f6-140">NOTES</span></span>
<span data-ttu-id="6b6f6-141">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="6b6f6-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6b6f6-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6b6f6-142">RELATED LINKS</span></span>
