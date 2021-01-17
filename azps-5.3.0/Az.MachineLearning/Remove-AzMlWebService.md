---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385914"
---
# <span data-ttu-id="0563f-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="0563f-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="0563f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0563f-102">SYNOPSIS</span></span>
<span data-ttu-id="0563f-103">Löscht einen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="0563f-103">Deletes a web service.</span></span>

## <span data-ttu-id="0563f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0563f-104">SYNTAX</span></span>

### <span data-ttu-id="0563f-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0563f-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0563f-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="0563f-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0563f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0563f-107">DESCRIPTION</span></span>
<span data-ttu-id="0563f-108">Löscht einen Azure Machine Learning-Webdienst, auf den von Ressourcengruppe und -name verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0563f-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="0563f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0563f-109">EXAMPLES</span></span>

### <span data-ttu-id="0563f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0563f-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="0563f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0563f-111">PARAMETERS</span></span>

### <span data-ttu-id="0563f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0563f-112">-DefaultProfile</span></span>
<span data-ttu-id="0563f-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0563f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0563f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="0563f-114">-Force</span></span>
<span data-ttu-id="0563f-115">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="0563f-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0563f-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="0563f-116">-MlWebService</span></span>
<span data-ttu-id="0563f-117">Der Webdienst, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0563f-117">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0563f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0563f-118">-Name</span></span>
<span data-ttu-id="0563f-119">Der Name des Webdiensts, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0563f-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="0563f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0563f-120">-ResourceGroupName</span></span>
<span data-ttu-id="0563f-121">Die Ressourcengruppe des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="0563f-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="0563f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0563f-122">-Confirm</span></span>
<span data-ttu-id="0563f-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0563f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0563f-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0563f-124">-WhatIf</span></span>
<span data-ttu-id="0563f-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0563f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0563f-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0563f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0563f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0563f-127">CommonParameters</span></span>
<span data-ttu-id="0563f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0563f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0563f-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0563f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0563f-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0563f-130">INPUTS</span></span>

### <span data-ttu-id="0563f-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="0563f-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="0563f-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0563f-132">OUTPUTS</span></span>

### <span data-ttu-id="0563f-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="0563f-133">System.Void</span></span>

## <span data-ttu-id="0563f-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0563f-134">NOTES</span></span>
<span data-ttu-id="0563f-135">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="0563f-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0563f-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0563f-136">RELATED LINKS</span></span>
