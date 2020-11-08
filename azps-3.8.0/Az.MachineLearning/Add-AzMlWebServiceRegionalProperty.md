---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: c9d7f205da9adbe199f2c8e33685612fd547feb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003001"
---
# <span data-ttu-id="74281-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="74281-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="74281-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74281-102">SYNOPSIS</span></span>
<span data-ttu-id="74281-103">Erstellt regionale Webdiensteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="74281-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="74281-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74281-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74281-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74281-105">DESCRIPTION</span></span>
<span data-ttu-id="74281-106">Erstellt Azure Machine Learning-Regions Eigenschaften für einen vorhandenen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="74281-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="74281-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74281-107">EXAMPLES</span></span>

### <span data-ttu-id="74281-108">Beispiel 1: Hinzufügen neuer regionaler Eigenschaften für West Central US</span><span class="sxs-lookup"><span data-stu-id="74281-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="74281-109">Dieser Beispielbefehl erstellt eine regionale Eigenschaft für einen Webdienst in der Region "West Central US".</span><span class="sxs-lookup"><span data-stu-id="74281-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="74281-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="74281-110">PARAMETERS</span></span>

### <span data-ttu-id="74281-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74281-111">-DefaultProfile</span></span>
<span data-ttu-id="74281-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="74281-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74281-113">-Force</span><span class="sxs-lookup"><span data-stu-id="74281-113">-Force</span></span>
<span data-ttu-id="74281-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="74281-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="74281-115">-Name</span><span class="sxs-lookup"><span data-stu-id="74281-115">-Name</span></span>
<span data-ttu-id="74281-116">Der Name für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="74281-116">The name for the web service.</span></span>

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

### <span data-ttu-id="74281-117">-Region</span><span class="sxs-lookup"><span data-stu-id="74281-117">-Region</span></span>
<span data-ttu-id="74281-118">Der Bereich, in dem die Webdiensteigenschaften erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="74281-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="74281-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74281-119">-ResourceGroupName</span></span>
<span data-ttu-id="74281-120">Die Ressourcengruppe, zu der der Webdienst gehört.</span><span class="sxs-lookup"><span data-stu-id="74281-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="74281-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74281-121">-Confirm</span></span>
<span data-ttu-id="74281-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74281-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74281-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74281-123">-WhatIf</span></span>
<span data-ttu-id="74281-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74281-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74281-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74281-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74281-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74281-126">CommonParameters</span></span>
<span data-ttu-id="74281-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74281-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74281-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74281-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74281-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74281-129">INPUTS</span></span>

### <span data-ttu-id="74281-130">System. String</span><span class="sxs-lookup"><span data-stu-id="74281-130">System.String</span></span>

## <span data-ttu-id="74281-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74281-131">OUTPUTS</span></span>

### <span data-ttu-id="74281-132">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="74281-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="74281-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="74281-133">NOTES</span></span>
<span data-ttu-id="74281-134">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="74281-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="74281-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74281-135">RELATED LINKS</span></span>
