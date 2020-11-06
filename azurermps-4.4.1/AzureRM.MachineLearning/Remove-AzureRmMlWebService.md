---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: f05d4142efab5a95cfef43fbc44cf57d0e1e2cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500005"
---
# <span data-ttu-id="2e8d7-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="2e8d7-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="2e8d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e8d7-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8d7-103">Löscht einen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e8d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e8d7-104">SYNTAX</span></span>

### <span data-ttu-id="2e8d7-105">Entfernen Sie eine Azure-ml-Webdienst-Resouce nach Name und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-105">Remove an Azure ML web service resouce by name and resource group.</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e8d7-106">Entfernen eines als Objekt angegebenen Azure ml-Webdiensts</span><span class="sxs-lookup"><span data-stu-id="2e8d7-106">Remove an Azure ML web service specified as an object.</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e8d7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e8d7-107">DESCRIPTION</span></span>
<span data-ttu-id="2e8d7-108">Löscht einen Azure Machine Learning-Webdienst, auf den nach Ressourcengruppe und Name verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="2e8d7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e8d7-109">EXAMPLES</span></span>

### <span data-ttu-id="2e8d7-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2e8d7-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="2e8d7-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="2e8d7-111">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="2e8d7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e8d7-112">PARAMETERS</span></span>

### <span data-ttu-id="2e8d7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2e8d7-113">-Force</span></span>
<span data-ttu-id="2e8d7-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2e8d7-115">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="2e8d7-115">-MlWebService</span></span>
<span data-ttu-id="2e8d7-116">Der Webdienst, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-116">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Remove an Azure ML web service specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e8d7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2e8d7-117">-Name</span></span>
<span data-ttu-id="2e8d7-118">Der Name des Webdiensts, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-118">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e8d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="2e8d7-120">Die Ressourcengruppe des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-120">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e8d7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2e8d7-121">-Confirm</span></span>
<span data-ttu-id="2e8d7-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e8d7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e8d7-123">-WhatIf</span></span>
<span data-ttu-id="2e8d7-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e8d7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e8d7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e8d7-126">-DefaultProfile</span></span>
<span data-ttu-id="2e8d7-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e8d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8d7-128">CommonParameters</span></span>
<span data-ttu-id="2e8d7-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e8d7-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e8d7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8d7-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e8d7-131">INPUTS</span></span>

### <span data-ttu-id="2e8d7-132">Webservice</span><span class="sxs-lookup"><span data-stu-id="2e8d7-132">WebService</span></span>
<span data-ttu-id="2e8d7-133">Der Parameter "MlWebService" akzeptiert den Wert vom Typ "Webservice" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e8d7-133">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="2e8d7-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e8d7-134">OUTPUTS</span></span>

### <span data-ttu-id="2e8d7-135">Keine</span><span class="sxs-lookup"><span data-stu-id="2e8d7-135">None</span></span>

## <span data-ttu-id="2e8d7-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e8d7-136">NOTES</span></span>
<span data-ttu-id="2e8d7-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="2e8d7-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2e8d7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e8d7-138">RELATED LINKS</span></span>

