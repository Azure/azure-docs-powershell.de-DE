---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8dc191223d5ec17856605c7640d324cc2ee3794e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505981"
---
# <span data-ttu-id="13a21-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="13a21-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="13a21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13a21-102">SYNOPSIS</span></span>
<span data-ttu-id="13a21-103">Erstellt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="13a21-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13a21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13a21-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
[[-Tag] <Hashtable>] [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="13a21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13a21-105">DESCRIPTION</span></span>
<span data-ttu-id="13a21-106">Das Cmdlet " **Satz-AzureRmDataFactoryV2** " erstellt eine Data Factory mit dem angegebenen Namen und Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="13a21-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="13a21-107">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="13a21-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="13a21-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13a21-108">EXAMPLES</span></span>

### <span data-ttu-id="13a21-109">Beispiel 1: Erstellen einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="13a21-109">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="13a21-110">Mit diesem Befehl wird eine Data Factory mit dem Namen WikiADF in der Ressourcengruppe ADF in der westus-Position erstellt.</span><span class="sxs-lookup"><span data-stu-id="13a21-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="13a21-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="13a21-111">PARAMETERS</span></span>

### <span data-ttu-id="13a21-112">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13a21-112">-Confirm</span></span>
<span data-ttu-id="13a21-113">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13a21-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13a21-114">-Force</span><span class="sxs-lookup"><span data-stu-id="13a21-114">-Force</span></span>
<span data-ttu-id="13a21-115">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="13a21-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="13a21-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="13a21-116">-Location</span></span>
<span data-ttu-id="13a21-117">Die Data Factory wird in diesem Bereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="13a21-117">The data factory is created in this region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a21-118">-Name</span><span class="sxs-lookup"><span data-stu-id="13a21-118">-Name</span></span>
<span data-ttu-id="13a21-119">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="13a21-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a21-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13a21-120">-ResourceGroupName</span></span>
<span data-ttu-id="13a21-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="13a21-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a21-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="13a21-122">-Tag</span></span>
<span data-ttu-id="13a21-123">Die Tags der Data Factory.</span><span class="sxs-lookup"><span data-stu-id="13a21-123">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a21-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13a21-124">-WhatIf</span></span>
<span data-ttu-id="13a21-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13a21-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="13a21-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13a21-126">INPUTS</span></span>

### <span data-ttu-id="13a21-127">System. String</span><span class="sxs-lookup"><span data-stu-id="13a21-127">System.String</span></span>
<span data-ttu-id="13a21-128">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="13a21-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="13a21-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13a21-129">OUTPUTS</span></span>

### <span data-ttu-id="13a21-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="13a21-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="13a21-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="13a21-131">NOTES</span></span>
<span data-ttu-id="13a21-132">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="13a21-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="13a21-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13a21-133">RELATED LINKS</span></span>
[<span data-ttu-id="13a21-134">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="13a21-134">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="13a21-135">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="13a21-135">Remove-AzureRmDataFactoryV2</span></span>]()
