---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 1c3c7d0dce441ecc6048e9ab98d56bf79b90020e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665197"
---
# <span data-ttu-id="4bf09-101">New-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="4bf09-101">New-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="4bf09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bf09-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf09-103">Erstellt einen neuen Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="4bf09-103">Creates a new commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bf09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bf09-104">SYNTAX</span></span>

```
New-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bf09-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bf09-105">DESCRIPTION</span></span>
<span data-ttu-id="4bf09-106">Erstellt einen Azure Machine Learning-Verpflichtungs Plan in einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4bf09-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="4bf09-107">Wenn in der Ressourcengruppe ein zusageplan mit demselben Namen vorhanden ist, fungiert der Anruf als Aktualisierungsvorgang, und der vorhandene obligoplan wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="4bf09-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="4bf09-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bf09-108">EXAMPLES</span></span>

### <span data-ttu-id="4bf09-109">--------------------------Beispiel 1: Erstellen eines neuen obligoplan--------------------------</span><span class="sxs-lookup"><span data-stu-id="4bf09-109">--------------------------  Example 1: Create a new commitment plan  --------------------------</span></span>
```
New-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="4bf09-110">Erstellt einen neuen Azure Machine Learning Commitment Plan mit dem Namen "MyCommitmentPlanName" in der Gruppe "myresourcegroup" und in der Region Süd-Zentralamerika.</span><span class="sxs-lookup"><span data-stu-id="4bf09-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="4bf09-111">In diesem Beispiel wird die SKU-DevTest/-Standard verwendet, was bedeutet, dass die vom obligoplan bereitgestellten Ressourcen durch die Grenzen von DevTest/Standard abgerechnet werden.</span><span class="sxs-lookup"><span data-stu-id="4bf09-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be definied by the limits of DevTest/Standard.</span></span> <span data-ttu-id="4bf09-112">Das SkuCapacity in diesem Beispiel ist 1, was bedeutet, dass die Kosten des Plans 1X die Kosten von DevTest und die Ressourcen, die der Plan enthält, 1X sind, was DevTest bietet.</span><span class="sxs-lookup"><span data-stu-id="4bf09-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="4bf09-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bf09-113">PARAMETERS</span></span>

### <span data-ttu-id="4bf09-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf09-114">-DefaultProfile</span></span>
<span data-ttu-id="4bf09-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4bf09-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bf09-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4bf09-116">-Force</span></span>
<span data-ttu-id="4bf09-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="4bf09-117">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf09-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="4bf09-118">-Location</span></span>
<span data-ttu-id="4bf09-119">Der Speicherort des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="4bf09-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4bf09-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4bf09-120">-Name</span></span>
<span data-ttu-id="4bf09-121">Der Name des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="4bf09-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4bf09-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bf09-122">-ResourceGroupName</span></span>
<span data-ttu-id="4bf09-123">Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="4bf09-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4bf09-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4bf09-124">-SkuCapacity</span></span>
<span data-ttu-id="4bf09-125">Die Kapazität der SKU, die verwendet werden soll, wenn der Azure-ml-Verpflichtungs Plan bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4bf09-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf09-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4bf09-126">-SkuName</span></span>
<span data-ttu-id="4bf09-127">Der Name der SKU, die bei der Bereitstellung des Azure-ml-Obligo-Plans zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="4bf09-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4bf09-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4bf09-128">-SkuTier</span></span>
<span data-ttu-id="4bf09-129">Die Ebene der SKU, die bei der Bereitstellung des Azure-ml-Obligo-Plans zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="4bf09-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="4bf09-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4bf09-130">-Confirm</span></span>
<span data-ttu-id="4bf09-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4bf09-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bf09-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bf09-132">-WhatIf</span></span>
<span data-ttu-id="4bf09-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4bf09-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bf09-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bf09-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bf09-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf09-135">CommonParameters</span></span>
<span data-ttu-id="4bf09-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bf09-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf09-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bf09-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf09-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bf09-138">INPUTS</span></span>

### <span data-ttu-id="4bf09-139">Keine</span><span class="sxs-lookup"><span data-stu-id="4bf09-139">None</span></span>
<span data-ttu-id="4bf09-140">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4bf09-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4bf09-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bf09-141">OUTPUTS</span></span>

### <span data-ttu-id="4bf09-142">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="4bf09-142">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="4bf09-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bf09-143">NOTES</span></span>
<span data-ttu-id="4bf09-144">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="4bf09-144">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="4bf09-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bf09-145">RELATED LINKS</span></span>

