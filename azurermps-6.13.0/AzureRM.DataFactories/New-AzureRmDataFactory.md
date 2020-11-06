---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 1636dd6b101a7639c84b0cd7c2659eac23a10b11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503002"
---
# <span data-ttu-id="60f60-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="60f60-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="60f60-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60f60-102">SYNOPSIS</span></span>
<span data-ttu-id="60f60-103">Erstellt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="60f60-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60f60-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60f60-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60f60-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60f60-105">DESCRIPTION</span></span>
<span data-ttu-id="60f60-106">Das Cmdlet **New-AzureRmDataFactory** erstellt eine Data Factory mit dem angegebenen Namen und Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="60f60-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="60f60-107">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="60f60-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="60f60-108">Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="60f60-108">Create a data factory.</span></span> 
- <span data-ttu-id="60f60-109">Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="60f60-109">Create linked services.</span></span> 
- <span data-ttu-id="60f60-110">Erstellen von Datasets</span><span class="sxs-lookup"><span data-stu-id="60f60-110">Create datasets.</span></span> 
- <span data-ttu-id="60f60-111">Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="60f60-111">Create a pipeline.</span></span>

## <span data-ttu-id="60f60-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60f60-112">EXAMPLES</span></span>

### <span data-ttu-id="60f60-113">Beispiel 1: Erstellen einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="60f60-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="60f60-114">Mit diesem Befehl wird eine Data Factory mit dem Namen WikiADF in der Ressourcengruppe ADF in der westus-Position erstellt.</span><span class="sxs-lookup"><span data-stu-id="60f60-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="60f60-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="60f60-115">PARAMETERS</span></span>

### <span data-ttu-id="60f60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f60-116">-DefaultProfile</span></span>
<span data-ttu-id="60f60-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="60f60-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60f60-118">-Force</span><span class="sxs-lookup"><span data-stu-id="60f60-118">-Force</span></span>
<span data-ttu-id="60f60-119">Gibt an, dass dieses Cmdlet eine vorhandene Data Factory ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="60f60-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="60f60-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="60f60-120">-Location</span></span>
<span data-ttu-id="60f60-121">Gibt den Speicherort für die Data Factory an, beispielsweise westus oder eastus.</span><span class="sxs-lookup"><span data-stu-id="60f60-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="60f60-122">Derzeit wird nur westus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60f60-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="60f60-123">-Name</span><span class="sxs-lookup"><span data-stu-id="60f60-123">-Name</span></span>
<span data-ttu-id="60f60-124">Gibt den Namen der Daten Factory an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="60f60-124">Specifies the name of the data factory to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60f60-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f60-125">-ResourceGroupName</span></span>
<span data-ttu-id="60f60-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="60f60-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="60f60-127">Mit diesem Cmdlet wird eine Data Factory erstellt, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="60f60-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="60f60-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="60f60-128">-Tag</span></span>
<span data-ttu-id="60f60-129">Die Tags der Data Factory.</span><span class="sxs-lookup"><span data-stu-id="60f60-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="60f60-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="60f60-130">-Confirm</span></span>
<span data-ttu-id="60f60-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60f60-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f60-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f60-132">-WhatIf</span></span>
<span data-ttu-id="60f60-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60f60-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f60-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60f60-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f60-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f60-135">CommonParameters</span></span>
<span data-ttu-id="60f60-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f60-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f60-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60f60-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f60-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60f60-138">INPUTS</span></span>

### <span data-ttu-id="60f60-139">System. String</span><span class="sxs-lookup"><span data-stu-id="60f60-139">System.String</span></span>

### <span data-ttu-id="60f60-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="60f60-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="60f60-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60f60-141">OUTPUTS</span></span>

### <span data-ttu-id="60f60-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="60f60-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="60f60-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="60f60-143">NOTES</span></span>
* <span data-ttu-id="60f60-144">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="60f60-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="60f60-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60f60-145">RELATED LINKS</span></span>

[<span data-ttu-id="60f60-146">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="60f60-146">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="60f60-147">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="60f60-147">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


