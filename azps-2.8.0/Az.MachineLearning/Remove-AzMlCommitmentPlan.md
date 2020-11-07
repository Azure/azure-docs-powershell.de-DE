---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 1c022d8ae97ac9f1e51bbabaff15a9dec61f5d87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650668"
---
# <span data-ttu-id="7609a-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7609a-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="7609a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7609a-102">SYNOPSIS</span></span>
<span data-ttu-id="7609a-103">Löscht einen Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="7609a-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="7609a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7609a-104">SYNTAX</span></span>

### <span data-ttu-id="7609a-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7609a-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7609a-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="7609a-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7609a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7609a-107">DESCRIPTION</span></span>
<span data-ttu-id="7609a-108">Löscht einen Azure Machine Learning-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="7609a-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="7609a-109">Beachten Sie, dass Verpflichtungs Pläne mit Verpflichtungs Zuordnungen nicht gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="7609a-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="7609a-110">Zubindungs Zuordnungen können nur von der Zielressource gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="7609a-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="7609a-111">Wenn Sie beispielsweise einen Azure Machine Learning Web Service löschen, wird die Verpflichtungs Zuordnung, die den Webdienst einem obligoplan zuordnet, ebenfalls gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7609a-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="7609a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7609a-112">EXAMPLES</span></span>

### <span data-ttu-id="7609a-113">Beispiel 1: Löschen eines Verpflichtungs Plans</span><span class="sxs-lookup"><span data-stu-id="7609a-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="7609a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7609a-114">PARAMETERS</span></span>

### <span data-ttu-id="7609a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7609a-115">-DefaultProfile</span></span>
<span data-ttu-id="7609a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7609a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7609a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7609a-117">-Force</span></span>
<span data-ttu-id="7609a-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="7609a-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7609a-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7609a-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="7609a-120">Das Machine Learning Web Service-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7609a-120">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7609a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7609a-121">-Name</span></span>
<span data-ttu-id="7609a-122">Der Name des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="7609a-122">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7609a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7609a-123">-ResourceGroupName</span></span>
<span data-ttu-id="7609a-124">Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="7609a-124">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7609a-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7609a-125">-Confirm</span></span>
<span data-ttu-id="7609a-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7609a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7609a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7609a-127">-WhatIf</span></span>
<span data-ttu-id="7609a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7609a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7609a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7609a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7609a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7609a-130">CommonParameters</span></span>
<span data-ttu-id="7609a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7609a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7609a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7609a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7609a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7609a-133">INPUTS</span></span>

### <span data-ttu-id="7609a-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7609a-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="7609a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7609a-135">OUTPUTS</span></span>

### <span data-ttu-id="7609a-136">System. void</span><span class="sxs-lookup"><span data-stu-id="7609a-136">System.Void</span></span>

## <span data-ttu-id="7609a-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="7609a-137">NOTES</span></span>
<span data-ttu-id="7609a-138">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7609a-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7609a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7609a-139">RELATED LINKS</span></span>
