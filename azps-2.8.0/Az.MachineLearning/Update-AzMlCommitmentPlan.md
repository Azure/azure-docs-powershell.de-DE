---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: c1aa160d7a0773569255f425f3993de0b47d552a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650655"
---
# <span data-ttu-id="75336-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="75336-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="75336-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75336-102">SYNOPSIS</span></span>
<span data-ttu-id="75336-103">Aktualisiert Eigenschaften einer vorhandenen Commitment Plan-Ressource.</span><span class="sxs-lookup"><span data-stu-id="75336-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="75336-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75336-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75336-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75336-105">DESCRIPTION</span></span>
<span data-ttu-id="75336-106">Aktualisiert eine vorhandene Commitment Plan-Ressource.</span><span class="sxs-lookup"><span data-stu-id="75336-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="75336-107">Beachten Sie, dass die meisten Eigenschaften des Verpflichtungs Plans unveränderlich sind und nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="75336-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="75336-108">Zu den Eigenschaften, die geändert werden können, gehören SKU (mit dem Sie den Verpflichtungs Plan von einer SKU zu einer anderen migrieren können) und Kategorien.</span><span class="sxs-lookup"><span data-stu-id="75336-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="75336-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75336-109">EXAMPLES</span></span>

### <span data-ttu-id="75336-110">Beispiel 1: Aktualisieren eines Verpflichtungs Plans</span><span class="sxs-lookup"><span data-stu-id="75336-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="75336-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="75336-111">PARAMETERS</span></span>

### <span data-ttu-id="75336-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75336-112">-DefaultProfile</span></span>
<span data-ttu-id="75336-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="75336-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75336-114">-Force</span><span class="sxs-lookup"><span data-stu-id="75336-114">-Force</span></span>
<span data-ttu-id="75336-115">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="75336-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="75336-116">-Name</span><span class="sxs-lookup"><span data-stu-id="75336-116">-Name</span></span>
<span data-ttu-id="75336-117">Der Name des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="75336-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="75336-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75336-118">-ResourceGroupName</span></span>
<span data-ttu-id="75336-119">Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="75336-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="75336-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="75336-120">-SkuCapacity</span></span>
<span data-ttu-id="75336-121">Die Kapazität der SKU, die bei der Aktualisierung des Azure-ml-Verpflichtungs Plans zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="75336-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="75336-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="75336-122">-SkuName</span></span>
<span data-ttu-id="75336-123">Der Name der SKU, die beim Aktualisieren des Azure-ml-Verpflichtungs Plans zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="75336-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="75336-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="75336-124">-SkuTier</span></span>
<span data-ttu-id="75336-125">Die Ebene der SKU, die bei der Aktualisierung des Azure-ml-Verpflichtungs Plans zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="75336-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="75336-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="75336-126">-Tag</span></span>
<span data-ttu-id="75336-127">Tags für die obligoplan-Ressource.</span><span class="sxs-lookup"><span data-stu-id="75336-127">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="75336-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75336-128">-Confirm</span></span>
<span data-ttu-id="75336-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75336-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75336-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75336-130">-WhatIf</span></span>
<span data-ttu-id="75336-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75336-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75336-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75336-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75336-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75336-133">CommonParameters</span></span>
<span data-ttu-id="75336-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75336-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75336-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75336-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75336-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75336-136">INPUTS</span></span>

### <span data-ttu-id="75336-137">Keine</span><span class="sxs-lookup"><span data-stu-id="75336-137">None</span></span>

## <span data-ttu-id="75336-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75336-138">OUTPUTS</span></span>

### <span data-ttu-id="75336-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="75336-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="75336-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="75336-140">NOTES</span></span>
<span data-ttu-id="75336-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="75336-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="75336-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75336-142">RELATED LINKS</span></span>
