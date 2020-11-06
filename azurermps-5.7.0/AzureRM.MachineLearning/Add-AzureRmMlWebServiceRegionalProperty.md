---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/add-azurermmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 8b2f881b57639a83227c2f590ffd260b78509a54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503742"
---
# <span data-ttu-id="546e1-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="546e1-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="546e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="546e1-102">SYNOPSIS</span></span>
<span data-ttu-id="546e1-103">Erstellt regionale Webdiensteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="546e1-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="546e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="546e1-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="546e1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="546e1-105">DESCRIPTION</span></span>
<span data-ttu-id="546e1-106">Erstellt Azure Machine Learning-Regions Eigenschaften für einen vorhandenen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="546e1-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="546e1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="546e1-107">EXAMPLES</span></span>

### <span data-ttu-id="546e1-108">--------------------------Beispiel 1: Hinzufügen neuer regionaler Eigenschaften für West Central US--------------------------</span><span class="sxs-lookup"><span data-stu-id="546e1-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="546e1-109">Dieser Beispielbefehl erstellt eine regionale Eigenschaft für einen Webdienst in der Region "West Central US".</span><span class="sxs-lookup"><span data-stu-id="546e1-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="546e1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="546e1-110">PARAMETERS</span></span>

### <span data-ttu-id="546e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546e1-111">-DefaultProfile</span></span>
<span data-ttu-id="546e1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="546e1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="546e1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="546e1-113">-Force</span></span>
<span data-ttu-id="546e1-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="546e1-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="546e1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="546e1-115">-Name</span></span>
<span data-ttu-id="546e1-116">Der Name für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="546e1-116">The name for the web service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546e1-117">-Region</span><span class="sxs-lookup"><span data-stu-id="546e1-117">-Region</span></span>
<span data-ttu-id="546e1-118">Der Bereich, in dem die Webdiensteigenschaften erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="546e1-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="546e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="546e1-120">Die Ressourcengruppe, zu der der Webdienst gehört.</span><span class="sxs-lookup"><span data-stu-id="546e1-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546e1-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="546e1-121">-Confirm</span></span>
<span data-ttu-id="546e1-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="546e1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="546e1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="546e1-123">-WhatIf</span></span>
<span data-ttu-id="546e1-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="546e1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="546e1-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="546e1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="546e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546e1-126">CommonParameters</span></span>
<span data-ttu-id="546e1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="546e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546e1-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="546e1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546e1-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="546e1-129">INPUTS</span></span>

### <span data-ttu-id="546e1-130">Keine</span><span class="sxs-lookup"><span data-stu-id="546e1-130">None</span></span>
<span data-ttu-id="546e1-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="546e1-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="546e1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="546e1-132">OUTPUTS</span></span>

### <span data-ttu-id="546e1-133">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="546e1-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="546e1-134">Eine zusammenfassende Beschreibung des Azure Machine Learning-Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="546e1-134">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="546e1-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="546e1-135">NOTES</span></span>
<span data-ttu-id="546e1-136">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="546e1-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="546e1-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="546e1-137">RELATED LINKS</span></span>

