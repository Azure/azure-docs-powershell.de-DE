---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 8b645154e9aaa011fccf1fa01624481e44b4eebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918792"
---
# <span data-ttu-id="fc7a9-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="fc7a9-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="fc7a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="fc7a9-103">Erstellt regionale Webdiensteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fc7a9-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="fc7a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc7a9-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc7a9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc7a9-105">DESCRIPTION</span></span>
<span data-ttu-id="fc7a9-106">Erstellt regionale Azure Machine Learning-Eigenschaften für einen vorhandenen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="fc7a9-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="fc7a9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc7a9-107">EXAMPLES</span></span>

### <span data-ttu-id="fc7a9-108">Beispiel 1: Hinzufügen neuer regionaler Eigenschaften für West Central US</span><span class="sxs-lookup"><span data-stu-id="fc7a9-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="fc7a9-109">Mit diesem Beispielbefehl wird eine regionale Eigenschaft für einen Webdienst in der Region "West Central US" erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc7a9-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="fc7a9-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fc7a9-110">PARAMETERS</span></span>

### <span data-ttu-id="fc7a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7a9-111">-DefaultProfile</span></span>
<span data-ttu-id="fc7a9-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fc7a9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc7a9-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="fc7a9-113">-Force</span></span>
<span data-ttu-id="fc7a9-114">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="fc7a9-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fc7a9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fc7a9-115">-Name</span></span>
<span data-ttu-id="fc7a9-116">Der Name für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="fc7a9-116">The name for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc7a9-117">-Region</span><span class="sxs-lookup"><span data-stu-id="fc7a9-117">-Region</span></span>
<span data-ttu-id="fc7a9-118">Der Bereich, in dem die Webdiensteigenschaften erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fc7a9-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="fc7a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc7a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc7a9-120">Die Ressourcengruppe, zu der der Webdienst gehört.</span><span class="sxs-lookup"><span data-stu-id="fc7a9-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc7a9-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc7a9-121">-Confirm</span></span>
<span data-ttu-id="fc7a9-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc7a9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc7a9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc7a9-123">-WhatIf</span></span>
<span data-ttu-id="fc7a9-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc7a9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc7a9-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc7a9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc7a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7a9-126">CommonParameters</span></span>
<span data-ttu-id="fc7a9-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc7a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7a9-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc7a9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7a9-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc7a9-129">INPUTS</span></span>

### <span data-ttu-id="fc7a9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fc7a9-130">System.String</span></span>

## <span data-ttu-id="fc7a9-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc7a9-131">OUTPUTS</span></span>

### <span data-ttu-id="fc7a9-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="fc7a9-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="fc7a9-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fc7a9-133">NOTES</span></span>
<span data-ttu-id="fc7a9-134">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="fc7a9-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="fc7a9-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fc7a9-135">RELATED LINKS</span></span>
