---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: 4d7365a2a7a8d11fc1032f182409bd462931be3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496505"
---
# <span data-ttu-id="f8aff-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="f8aff-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="f8aff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8aff-102">SYNOPSIS</span></span>
<span data-ttu-id="f8aff-103">Löscht einen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="f8aff-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8aff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8aff-104">SYNTAX</span></span>

### <span data-ttu-id="f8aff-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f8aff-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8aff-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="f8aff-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8aff-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8aff-107">DESCRIPTION</span></span>
<span data-ttu-id="f8aff-108">Löscht einen Azure Machine Learning-Webdienst, auf den nach Ressourcengruppe und Name verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f8aff-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="f8aff-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8aff-109">EXAMPLES</span></span>

### <span data-ttu-id="f8aff-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f8aff-110">--------------------------  Example 1  --------------------------</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="f8aff-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8aff-111">PARAMETERS</span></span>

### <span data-ttu-id="f8aff-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8aff-112">-DefaultProfile</span></span>
<span data-ttu-id="f8aff-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f8aff-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8aff-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f8aff-114">-Force</span></span>
<span data-ttu-id="f8aff-115">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="f8aff-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f8aff-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="f8aff-116">-MlWebService</span></span>
<span data-ttu-id="f8aff-117">Der Webdienst, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8aff-117">The web service to be removed.</span></span>

```yaml
Type: WebService
Parameter Sets: RemoveByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8aff-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f8aff-118">-Name</span></span>
<span data-ttu-id="f8aff-119">Der Name des Webdiensts, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8aff-119">The name of the web service to be removed.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8aff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8aff-120">-ResourceGroupName</span></span>
<span data-ttu-id="f8aff-121">Die Ressourcengruppe des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="f8aff-121">The resource group of the web service.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8aff-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8aff-122">-Confirm</span></span>
<span data-ttu-id="f8aff-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8aff-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8aff-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8aff-124">-WhatIf</span></span>
<span data-ttu-id="f8aff-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8aff-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8aff-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8aff-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8aff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8aff-127">CommonParameters</span></span>
<span data-ttu-id="f8aff-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8aff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8aff-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8aff-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8aff-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8aff-130">INPUTS</span></span>

### <span data-ttu-id="f8aff-131">Webservice</span><span class="sxs-lookup"><span data-stu-id="f8aff-131">WebService</span></span>
<span data-ttu-id="f8aff-132">Der Parameter "MlWebService" akzeptiert den Wert vom Typ "Webservice" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f8aff-132">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="f8aff-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8aff-133">OUTPUTS</span></span>

### <span data-ttu-id="f8aff-134">Keine</span><span class="sxs-lookup"><span data-stu-id="f8aff-134">None</span></span>

## <span data-ttu-id="f8aff-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8aff-135">NOTES</span></span>
<span data-ttu-id="f8aff-136">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f8aff-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f8aff-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8aff-137">RELATED LINKS</span></span>

