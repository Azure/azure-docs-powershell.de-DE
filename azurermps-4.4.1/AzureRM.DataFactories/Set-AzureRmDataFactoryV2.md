---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: b5e5d42ba114da87daa3fa3effb15d3ad8bab22c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477170"
---
# <span data-ttu-id="ecfe1-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ecfe1-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="ecfe1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecfe1-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfe1-103">Erstellt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecfe1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecfe1-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecfe1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecfe1-105">DESCRIPTION</span></span>
<span data-ttu-id="ecfe1-106">Das Cmdlet " **Satz-AzureRmDataFactoryV2** " erstellt eine Data Factory mit dem angegebenen Namen und Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="ecfe1-107">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="ecfe1-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="ecfe1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecfe1-108">EXAMPLES</span></span>

### <span data-ttu-id="ecfe1-109">Beispiel 1: Erstellen einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="ecfe1-109">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="ecfe1-110">Mit diesem Befehl wird eine Data Factory mit dem Namen WikiADF in der Ressourcengruppe ADF in der westus-Position erstellt.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="ecfe1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecfe1-111">PARAMETERS</span></span>

### <span data-ttu-id="ecfe1-112">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ecfe1-112">-Confirm</span></span>
<span data-ttu-id="ecfe1-113">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecfe1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ecfe1-114">-Force</span></span>
<span data-ttu-id="ecfe1-115">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ecfe1-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="ecfe1-116">-Location</span></span>
<span data-ttu-id="ecfe1-117">Die Data Factory wird in diesem Bereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-117">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfe1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ecfe1-118">-Name</span></span>
<span data-ttu-id="ecfe1-119">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfe1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecfe1-120">-ResourceGroupName</span></span>
<span data-ttu-id="ecfe1-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfe1-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="ecfe1-122">-Tag</span></span>
<span data-ttu-id="ecfe1-123">Die Tags der Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-123">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfe1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecfe1-124">-WhatIf</span></span>
<span data-ttu-id="ecfe1-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ecfe1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfe1-126">-DefaultProfile</span></span>
<span data-ttu-id="ecfe1-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecfe1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfe1-128">CommonParameters</span></span>
<span data-ttu-id="ecfe1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfe1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfe1-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecfe1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfe1-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecfe1-131">INPUTS</span></span>

### <span data-ttu-id="ecfe1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ecfe1-132">System.String</span></span>
<span data-ttu-id="ecfe1-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ecfe1-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ecfe1-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecfe1-134">OUTPUTS</span></span>

### <span data-ttu-id="ecfe1-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ecfe1-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ecfe1-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecfe1-136">NOTES</span></span>
<span data-ttu-id="ecfe1-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="ecfe1-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ecfe1-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecfe1-138">RELATED LINKS</span></span>

[<span data-ttu-id="ecfe1-139">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ecfe1-139">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="ecfe1-140">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ecfe1-140">Remove-AzureRmDataFactoryV2</span></span>]()
