---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 81b05b8229530a8975be023a3b4a5e8c93d93c80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505085"
---
# <span data-ttu-id="56d52-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="56d52-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="56d52-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56d52-102">SYNOPSIS</span></span>
<span data-ttu-id="56d52-103">Entfernt eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="56d52-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56d52-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56d52-104">SYNTAX</span></span>

### <span data-ttu-id="56d52-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="56d52-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="56d52-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="56d52-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="56d52-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="56d52-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="56d52-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56d52-108">DESCRIPTION</span></span>
<span data-ttu-id="56d52-109">Das Remove-AzureRmDataFactoryV2IntegrationRuntime-Cmdlet entfernt eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="56d52-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="56d52-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56d52-110">EXAMPLES</span></span>

### <span data-ttu-id="56d52-111">Beispiel 1: Entfernen einer Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="56d52-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="56d52-112">Dieser Befehl entfernt die Integrationslaufzeit mit dem Namen "Test-reservierte-IR" aus der Data Factory mit dem Namen "Test-DF".</span><span class="sxs-lookup"><span data-stu-id="56d52-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="56d52-113">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="56d52-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="56d52-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="56d52-114">PARAMETERS</span></span>

### <span data-ttu-id="56d52-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="56d52-115">-DataFactoryName</span></span>
<span data-ttu-id="56d52-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="56d52-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d52-117">-Force</span><span class="sxs-lookup"><span data-stu-id="56d52-117">-Force</span></span>
<span data-ttu-id="56d52-118">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="56d52-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="56d52-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="56d52-119">-InputObject</span></span>
<span data-ttu-id="56d52-120">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="56d52-120">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56d52-121">-Name</span><span class="sxs-lookup"><span data-stu-id="56d52-121">-Name</span></span>
<span data-ttu-id="56d52-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="56d52-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d52-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d52-123">-ResourceGroupName</span></span>
<span data-ttu-id="56d52-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="56d52-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d52-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="56d52-125">-ResourceId</span></span>
<span data-ttu-id="56d52-126">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="56d52-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d52-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="56d52-127">-Confirm</span></span>
<span data-ttu-id="56d52-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56d52-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56d52-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d52-129">-WhatIf</span></span>
<span data-ttu-id="56d52-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56d52-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="56d52-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56d52-131">INPUTS</span></span>

### <span data-ttu-id="56d52-132">System. String</span><span class="sxs-lookup"><span data-stu-id="56d52-132">System.String</span></span>
<span data-ttu-id="56d52-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="56d52-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="56d52-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56d52-134">OUTPUTS</span></span>

### <span data-ttu-id="56d52-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="56d52-135">System.Object</span></span>

## <span data-ttu-id="56d52-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="56d52-136">NOTES</span></span>
<span data-ttu-id="56d52-137">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="56d52-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="56d52-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56d52-138">RELATED LINKS</span></span>
[<span data-ttu-id="56d52-139">Satz-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="56d52-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="56d52-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="56d52-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

