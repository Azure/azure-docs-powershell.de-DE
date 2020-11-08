---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: c9d7f205da9adbe199f2c8e33685612fd547feb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174669"
---
# <span data-ttu-id="236bc-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="236bc-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="236bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="236bc-102">SYNOPSIS</span></span>
<span data-ttu-id="236bc-103">Erstellt regionale Webdiensteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="236bc-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="236bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="236bc-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="236bc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="236bc-105">DESCRIPTION</span></span>
<span data-ttu-id="236bc-106">Erstellt Azure Machine Learning-Regions Eigenschaften für einen vorhandenen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="236bc-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="236bc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="236bc-107">EXAMPLES</span></span>

### <span data-ttu-id="236bc-108">Beispiel 1: Hinzufügen neuer regionaler Eigenschaften für West Central US</span><span class="sxs-lookup"><span data-stu-id="236bc-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="236bc-109">Dieser Beispielbefehl erstellt eine regionale Eigenschaft für einen Webdienst in der Region "West Central US".</span><span class="sxs-lookup"><span data-stu-id="236bc-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="236bc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="236bc-110">PARAMETERS</span></span>

### <span data-ttu-id="236bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="236bc-111">-DefaultProfile</span></span>
<span data-ttu-id="236bc-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="236bc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="236bc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="236bc-113">-Force</span></span>
<span data-ttu-id="236bc-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="236bc-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="236bc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="236bc-115">-Name</span></span>
<span data-ttu-id="236bc-116">Der Name für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="236bc-116">The name for the web service.</span></span>

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

### <span data-ttu-id="236bc-117">-Region</span><span class="sxs-lookup"><span data-stu-id="236bc-117">-Region</span></span>
<span data-ttu-id="236bc-118">Der Bereich, in dem die Webdiensteigenschaften erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="236bc-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="236bc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="236bc-119">-ResourceGroupName</span></span>
<span data-ttu-id="236bc-120">Die Ressourcengruppe, zu der der Webdienst gehört.</span><span class="sxs-lookup"><span data-stu-id="236bc-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="236bc-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="236bc-121">-Confirm</span></span>
<span data-ttu-id="236bc-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="236bc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="236bc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="236bc-123">-WhatIf</span></span>
<span data-ttu-id="236bc-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="236bc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="236bc-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="236bc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="236bc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="236bc-126">CommonParameters</span></span>
<span data-ttu-id="236bc-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="236bc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="236bc-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="236bc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="236bc-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="236bc-129">INPUTS</span></span>

### <span data-ttu-id="236bc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="236bc-130">System.String</span></span>

## <span data-ttu-id="236bc-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="236bc-131">OUTPUTS</span></span>

### <span data-ttu-id="236bc-132">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="236bc-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="236bc-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="236bc-133">NOTES</span></span>
<span data-ttu-id="236bc-134">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="236bc-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="236bc-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="236bc-135">RELATED LINKS</span></span>
