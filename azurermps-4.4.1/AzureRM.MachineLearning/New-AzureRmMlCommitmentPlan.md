---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 984e1f9d75a7c5a56e6a9bda71a07b193df5be15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665027"
---
# <span data-ttu-id="2b375-101">New-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="2b375-101">New-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="2b375-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b375-102">SYNOPSIS</span></span>
<span data-ttu-id="2b375-103">Erstellt einen neuen Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="2b375-103">Creates a new commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b375-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b375-104">SYNTAX</span></span>

```
New-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b375-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b375-105">DESCRIPTION</span></span>
<span data-ttu-id="2b375-106">Erstellt einen Azure Machine Learning-Verpflichtungs Plan in einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2b375-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="2b375-107">Wenn in der Ressourcengruppe ein zusageplan mit demselben Namen vorhanden ist, fungiert der Anruf als Aktualisierungsvorgang, und der vorhandene obligoplan wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="2b375-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="2b375-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b375-108">EXAMPLES</span></span>

### <span data-ttu-id="2b375-109">--------------------------Beispiel 1: Erstellen eines neuen obligoplan--------------------------</span><span class="sxs-lookup"><span data-stu-id="2b375-109">--------------------------  Example 1: Create a new commitment plan  --------------------------</span></span>
<span data-ttu-id="2b375-110">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="2b375-110">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="2b375-111">Erstellt einen neuen Azure Machine Learning Commitment Plan mit dem Namen "MyCommitmentPlanName" in der Gruppe "myresourcegroup" und in der Region Süd-Zentralamerika.</span><span class="sxs-lookup"><span data-stu-id="2b375-111">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="2b375-112">In diesem Beispiel wird die SKU-DevTest/-Standard verwendet, was bedeutet, dass die vom obligoplan bereitgestellten Ressourcen durch die Grenzen von DevTest/Standard abgerechnet werden.</span><span class="sxs-lookup"><span data-stu-id="2b375-112">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be definied by the limits of DevTest/Standard.</span></span> <span data-ttu-id="2b375-113">Das SkuCapacity in diesem Beispiel ist 1, was bedeutet, dass die Kosten des Plans 1X die Kosten von DevTest und die Ressourcen, die der Plan enthält, 1X sind, was DevTest bietet.</span><span class="sxs-lookup"><span data-stu-id="2b375-113">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="2b375-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b375-114">PARAMETERS</span></span>

### <span data-ttu-id="2b375-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2b375-115">-Force</span></span>
<span data-ttu-id="2b375-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="2b375-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2b375-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="2b375-117">-Location</span></span>
<span data-ttu-id="2b375-118">Der Speicherort des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="2b375-118">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2b375-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2b375-119">-Name</span></span>
<span data-ttu-id="2b375-120">Der Name des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="2b375-120">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2b375-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b375-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b375-122">Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="2b375-122">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2b375-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2b375-123">-SkuCapacity</span></span>
<span data-ttu-id="2b375-124">Die Kapazität der SKU, die verwendet werden soll, wenn der Azure-ml-Verpflichtungs Plan bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2b375-124">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2b375-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2b375-125">-SkuName</span></span>
<span data-ttu-id="2b375-126">Der Name der SKU, die bei der Bereitstellung des Azure-ml-Obligo-Plans zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="2b375-126">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2b375-127">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2b375-127">-SkuTier</span></span>
<span data-ttu-id="2b375-128">Die Ebene der SKU, die bei der Bereitstellung des Azure-ml-Obligo-Plans zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="2b375-128">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2b375-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b375-129">-Confirm</span></span>
<span data-ttu-id="2b375-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b375-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b375-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b375-131">-WhatIf</span></span>
<span data-ttu-id="2b375-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b375-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b375-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b375-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b375-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b375-134">-DefaultProfile</span></span>
<span data-ttu-id="2b375-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2b375-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b375-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b375-136">CommonParameters</span></span>
<span data-ttu-id="2b375-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b375-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b375-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b375-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b375-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b375-139">INPUTS</span></span>

## <span data-ttu-id="2b375-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b375-140">OUTPUTS</span></span>

### <span data-ttu-id="2b375-141">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="2b375-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="2b375-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b375-142">NOTES</span></span>
<span data-ttu-id="2b375-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="2b375-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2b375-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b375-144">RELATED LINKS</span></span>

