---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: c50023cefbae9a9ba341eba22f40a421c37d12c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496261"
---
# <span data-ttu-id="643de-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="643de-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="643de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="643de-102">SYNOPSIS</span></span>
<span data-ttu-id="643de-103">Erstellt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="643de-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="643de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="643de-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="643de-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="643de-105">DESCRIPTION</span></span>
<span data-ttu-id="643de-106">Das Cmdlet " **Satz-AzureRmDataFactoryV2** " erstellt eine Data Factory mit dem angegebenen Namen und Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="643de-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="643de-107">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:--Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="643de-107">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="643de-108">--Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="643de-108">-- Create linked services.</span></span>
<span data-ttu-id="643de-109">--Erstellen von Datasets.</span><span class="sxs-lookup"><span data-stu-id="643de-109">-- Create datasets.</span></span>
<span data-ttu-id="643de-110">--Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="643de-110">-- Create a pipeline.</span></span>

## <span data-ttu-id="643de-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="643de-111">EXAMPLES</span></span>

### <span data-ttu-id="643de-112">Beispiel 1: Erstellen einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="643de-112">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="643de-113">Mit diesem Befehl wird eine Data Factory mit dem Namen WikiADF in der Ressourcengruppe ADF in der westus-Position erstellt.</span><span class="sxs-lookup"><span data-stu-id="643de-113">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="643de-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="643de-114">PARAMETERS</span></span>

### <span data-ttu-id="643de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643de-115">-DefaultProfile</span></span>
<span data-ttu-id="643de-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="643de-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="643de-117">-Force</span><span class="sxs-lookup"><span data-stu-id="643de-117">-Force</span></span>
<span data-ttu-id="643de-118">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="643de-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="643de-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="643de-119">-Location</span></span>
<span data-ttu-id="643de-120">Die Data Factory wird in diesem Bereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="643de-120">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="643de-121">-Name</span><span class="sxs-lookup"><span data-stu-id="643de-121">-Name</span></span>
<span data-ttu-id="643de-122">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="643de-122">The data factory name.</span></span>

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

### <span data-ttu-id="643de-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="643de-123">-ResourceGroupName</span></span>
<span data-ttu-id="643de-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="643de-124">The resource group name.</span></span>

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

### <span data-ttu-id="643de-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="643de-125">-Tag</span></span>
<span data-ttu-id="643de-126">Die Tags der Data Factory.</span><span class="sxs-lookup"><span data-stu-id="643de-126">The tags of the data factory.</span></span>

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

### <span data-ttu-id="643de-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="643de-127">-Confirm</span></span>
<span data-ttu-id="643de-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="643de-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="643de-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="643de-129">-WhatIf</span></span>
<span data-ttu-id="643de-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="643de-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="643de-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643de-131">CommonParameters</span></span>
<span data-ttu-id="643de-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="643de-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643de-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="643de-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643de-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="643de-134">INPUTS</span></span>

### <span data-ttu-id="643de-135">System. String</span><span class="sxs-lookup"><span data-stu-id="643de-135">System.String</span></span>

### <span data-ttu-id="643de-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="643de-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="643de-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="643de-137">OUTPUTS</span></span>

### <span data-ttu-id="643de-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="643de-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="643de-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="643de-139">NOTES</span></span>
<span data-ttu-id="643de-140">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="643de-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="643de-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="643de-141">RELATED LINKS</span></span>

[<span data-ttu-id="643de-142">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="643de-142">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="643de-143">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="643de-143">Remove-AzureRmDataFactoryV2</span></span>]()
