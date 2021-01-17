---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: c9d7f205da9adbe199f2c8e33685612fd547feb7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386110"
---
# <span data-ttu-id="963b1-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="963b1-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="963b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="963b1-102">SYNOPSIS</span></span>
<span data-ttu-id="963b1-103">Erstellt regionale Webdiensteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="963b1-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="963b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="963b1-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="963b1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="963b1-105">DESCRIPTION</span></span>
<span data-ttu-id="963b1-106">Erstellt regionale Azure Machine Learning-Eigenschaften für einen vorhandenen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="963b1-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="963b1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="963b1-107">EXAMPLES</span></span>

### <span data-ttu-id="963b1-108">Beispiel 1: Hinzufügen neuer regionaler Eigenschaften für "USA, Mitte, Westen"</span><span class="sxs-lookup"><span data-stu-id="963b1-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="963b1-109">Mit diesem Beispielbefehl wird eine regionale Eigenschaft für einen Webdienst in der Region "West Central US" erstellt.</span><span class="sxs-lookup"><span data-stu-id="963b1-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="963b1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="963b1-110">PARAMETERS</span></span>

### <span data-ttu-id="963b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="963b1-111">-DefaultProfile</span></span>
<span data-ttu-id="963b1-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="963b1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="963b1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="963b1-113">-Force</span></span>
<span data-ttu-id="963b1-114">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="963b1-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="963b1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="963b1-115">-Name</span></span>
<span data-ttu-id="963b1-116">Der Name des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="963b1-116">The name for the web service.</span></span>

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

### <span data-ttu-id="963b1-117">-Region</span><span class="sxs-lookup"><span data-stu-id="963b1-117">-Region</span></span>
<span data-ttu-id="963b1-118">Die Region, in der die Webdiensteigenschaften erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="963b1-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="963b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="963b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="963b1-120">Die Ressourcengruppe, zu der der Webdienst gehört.</span><span class="sxs-lookup"><span data-stu-id="963b1-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="963b1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="963b1-121">-Confirm</span></span>
<span data-ttu-id="963b1-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="963b1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="963b1-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="963b1-123">-WhatIf</span></span>
<span data-ttu-id="963b1-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="963b1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="963b1-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="963b1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="963b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="963b1-126">CommonParameters</span></span>
<span data-ttu-id="963b1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="963b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="963b1-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="963b1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="963b1-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="963b1-129">INPUTS</span></span>

### <span data-ttu-id="963b1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="963b1-130">System.String</span></span>

## <span data-ttu-id="963b1-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="963b1-131">OUTPUTS</span></span>

### <span data-ttu-id="963b1-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="963b1-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="963b1-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="963b1-133">NOTES</span></span>
<span data-ttu-id="963b1-134">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="963b1-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="963b1-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="963b1-135">RELATED LINKS</span></span>
