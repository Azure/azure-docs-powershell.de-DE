---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: e7c296c74aad7e733659930aea9487cf2a73aef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663314"
---
# <span data-ttu-id="622ca-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="622ca-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="622ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="622ca-102">SYNOPSIS</span></span>
<span data-ttu-id="622ca-103">Aktualisiert Eigenschaften einer vorhandenen Commitment Plan-Ressource.</span><span class="sxs-lookup"><span data-stu-id="622ca-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="622ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="622ca-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tags <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="622ca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="622ca-105">DESCRIPTION</span></span>
<span data-ttu-id="622ca-106">Aktualisiert eine vorhandene Commitment Plan-Ressource.</span><span class="sxs-lookup"><span data-stu-id="622ca-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="622ca-107">Beachten Sie, dass die meisten Eigenschaften des Verpflichtungs Plans unveränderlich sind und nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="622ca-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="622ca-108">Zu den Eigenschaften, die geändert werden können, gehören SKU (mit dem Sie den Verpflichtungs Plan von einer SKU zu einer anderen migrieren können) und Kategorien.</span><span class="sxs-lookup"><span data-stu-id="622ca-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="622ca-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="622ca-109">EXAMPLES</span></span>

### <span data-ttu-id="622ca-110">--------------------------Beispiel 1: Aktualisieren eines Obligo-Plans--------------------------</span><span class="sxs-lookup"><span data-stu-id="622ca-110">--------------------------  Example 1: Update a commitment plan  --------------------------</span></span>
<span data-ttu-id="622ca-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="622ca-111">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="622ca-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="622ca-112">PARAMETERS</span></span>

### <span data-ttu-id="622ca-113">-Force</span><span class="sxs-lookup"><span data-stu-id="622ca-113">-Force</span></span>
<span data-ttu-id="622ca-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="622ca-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="622ca-115">-Name</span><span class="sxs-lookup"><span data-stu-id="622ca-115">-Name</span></span>
<span data-ttu-id="622ca-116">Der Name des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="622ca-116">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="622ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="622ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="622ca-118">Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="622ca-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="622ca-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="622ca-119">-SkuCapacity</span></span>
<span data-ttu-id="622ca-120">Die Kapazität der SKU, die bei der Aktualisierung des Azure-ml-Verpflichtungs Plans zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="622ca-120">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="622ca-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="622ca-121">-SkuName</span></span>
<span data-ttu-id="622ca-122">Der Name der SKU, die beim Aktualisieren des Azure-ml-Verpflichtungs Plans zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="622ca-122">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="622ca-123">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="622ca-123">-SkuTier</span></span>
<span data-ttu-id="622ca-124">Die Ebene der SKU, die bei der Aktualisierung des Azure-ml-Verpflichtungs Plans zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="622ca-124">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="622ca-125">-Tags</span><span class="sxs-lookup"><span data-stu-id="622ca-125">-Tags</span></span>
<span data-ttu-id="622ca-126">Tags für die obligoplan-Ressource.</span><span class="sxs-lookup"><span data-stu-id="622ca-126">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="622ca-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="622ca-127">-Confirm</span></span>
<span data-ttu-id="622ca-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="622ca-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="622ca-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="622ca-129">-WhatIf</span></span>
<span data-ttu-id="622ca-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="622ca-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="622ca-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="622ca-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="622ca-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622ca-132">-DefaultProfile</span></span>
<span data-ttu-id="622ca-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="622ca-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="622ca-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622ca-134">CommonParameters</span></span>
<span data-ttu-id="622ca-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="622ca-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622ca-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622ca-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622ca-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="622ca-137">INPUTS</span></span>

## <span data-ttu-id="622ca-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="622ca-138">OUTPUTS</span></span>

### <span data-ttu-id="622ca-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="622ca-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="622ca-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="622ca-140">NOTES</span></span>
<span data-ttu-id="622ca-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="622ca-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="622ca-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="622ca-142">RELATED LINKS</span></span>

