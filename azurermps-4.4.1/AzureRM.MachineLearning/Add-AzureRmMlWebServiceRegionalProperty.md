---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 24f12a0e95ab7c233a08ec1ad0f4dc330583dd3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505901"
---
# <span data-ttu-id="9b990-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="9b990-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="9b990-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b990-102">SYNOPSIS</span></span>
<span data-ttu-id="9b990-103">Erstellt regionale Webdiensteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9b990-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b990-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b990-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b990-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b990-105">DESCRIPTION</span></span>
<span data-ttu-id="9b990-106">Erstellt Azure Machine Learning-Regions Eigenschaften für einen vorhandenen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="9b990-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="9b990-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b990-107">EXAMPLES</span></span>

### <span data-ttu-id="9b990-108">--------------------------Beispiel 1: Hinzufügen neuer regionaler Eigenschaften für West Central US--------------------------</span><span class="sxs-lookup"><span data-stu-id="9b990-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>
<span data-ttu-id="9b990-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="9b990-109">@{paragraph=PS C:\\\>}</span></span>



```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="9b990-110">Dieser Beispielbefehl erstellt eine regionale Eigenschaft für einen Webdienst in der Region "West Central US".</span><span class="sxs-lookup"><span data-stu-id="9b990-110">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="9b990-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b990-111">PARAMETERS</span></span>

### <span data-ttu-id="9b990-112">-Force</span><span class="sxs-lookup"><span data-stu-id="9b990-112">-Force</span></span>
<span data-ttu-id="9b990-113">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="9b990-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9b990-114">-Name</span><span class="sxs-lookup"><span data-stu-id="9b990-114">-Name</span></span>
<span data-ttu-id="9b990-115">Der Name für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="9b990-115">The name for the web service.</span></span>

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

### <span data-ttu-id="9b990-116">-Region</span><span class="sxs-lookup"><span data-stu-id="9b990-116">-Region</span></span>
<span data-ttu-id="9b990-117">Der Bereich, in dem die Webdiensteigenschaften erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b990-117">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="9b990-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b990-118">-ResourceGroupName</span></span>
<span data-ttu-id="9b990-119">Die Ressourcengruppe, zu der der Webdienst gehört.</span><span class="sxs-lookup"><span data-stu-id="9b990-119">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="9b990-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b990-120">-Confirm</span></span>
<span data-ttu-id="9b990-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b990-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b990-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b990-122">-WhatIf</span></span>
<span data-ttu-id="9b990-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b990-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b990-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b990-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b990-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b990-125">-DefaultProfile</span></span>
<span data-ttu-id="9b990-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b990-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b990-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b990-127">CommonParameters</span></span>
<span data-ttu-id="9b990-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b990-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b990-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b990-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b990-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b990-130">INPUTS</span></span>

## <span data-ttu-id="9b990-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b990-131">OUTPUTS</span></span>

### <span data-ttu-id="9b990-132">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="9b990-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="9b990-133">Eine zusammenfassende Beschreibung des Azure Machine Learning-Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="9b990-133">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="9b990-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b990-134">NOTES</span></span>
<span data-ttu-id="9b990-135">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="9b990-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="9b990-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b990-136">RELATED LINKS</span></span>

