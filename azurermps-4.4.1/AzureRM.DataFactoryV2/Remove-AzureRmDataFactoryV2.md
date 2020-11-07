---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 73cc7df9dcb32dac592df56f16ad819219e06b7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664276"
---
# <span data-ttu-id="38e00-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="38e00-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="38e00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38e00-102">SYNOPSIS</span></span>
<span data-ttu-id="38e00-103">Entfernt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="38e00-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38e00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38e00-104">SYNTAX</span></span>

### <span data-ttu-id="38e00-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="38e00-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="38e00-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="38e00-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="38e00-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="38e00-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="38e00-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38e00-108">DESCRIPTION</span></span>
<span data-ttu-id="38e00-109">Das Remove-AzureRmDataFactoryV2-Cmdlet entfernt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="38e00-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="38e00-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38e00-110">EXAMPLES</span></span>

### <span data-ttu-id="38e00-111">Beispiel 1: Entfernen einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="38e00-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="38e00-112">Mit diesem Befehl wird die Data Factory mit dem Namen WikiADF aus der Ressourcengruppe ADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="38e00-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="38e00-113">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="38e00-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="38e00-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="38e00-114">PARAMETERS</span></span>

### <span data-ttu-id="38e00-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="38e00-115">-Confirm</span></span>
<span data-ttu-id="38e00-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38e00-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38e00-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="38e00-117">-InputObject</span></span>
<span data-ttu-id="38e00-118">Gibt das zu entfernende DataFactory-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="38e00-118">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38e00-119">-Force</span><span class="sxs-lookup"><span data-stu-id="38e00-119">-Force</span></span>
<span data-ttu-id="38e00-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="38e00-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="38e00-121">-Name</span><span class="sxs-lookup"><span data-stu-id="38e00-121">-Name</span></span>
<span data-ttu-id="38e00-122">Gibt den Namen der Daten Factory an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="38e00-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e00-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38e00-123">-ResourceGroupName</span></span>
<span data-ttu-id="38e00-124">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="38e00-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="38e00-125">Mit diesem Cmdlet wird eine Data Factory aus der Gruppe entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="38e00-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e00-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="38e00-126">-ResourceId</span></span>
<span data-ttu-id="38e00-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="38e00-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38e00-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38e00-128">-WhatIf</span></span>
<span data-ttu-id="38e00-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38e00-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="38e00-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38e00-130">INPUTS</span></span>

### <span data-ttu-id="38e00-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="38e00-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="38e00-132">System. String</span><span class="sxs-lookup"><span data-stu-id="38e00-132">System.String</span></span>


## <span data-ttu-id="38e00-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38e00-133">OUTPUTS</span></span>

### <span data-ttu-id="38e00-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="38e00-134">System.Object</span></span>

## <span data-ttu-id="38e00-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="38e00-135">NOTES</span></span>
<span data-ttu-id="38e00-136">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="38e00-136">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="38e00-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38e00-137">RELATED LINKS</span></span>
[<span data-ttu-id="38e00-138">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="38e00-138">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="38e00-139">Satz-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="38e00-139">Set-AzureRmDataFactoryV2</span></span>]()
