---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 450a833656f6508f70ebd97f5387075c1711c5f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847239"
---
# <span data-ttu-id="31b9c-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="31b9c-101">New-AzDataFactory</span></span>

## <span data-ttu-id="31b9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="31b9c-103">Erstellt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="31b9c-103">Creates a data factory.</span></span>

## <span data-ttu-id="31b9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31b9c-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31b9c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="31b9c-106">Das Cmdlet **New-AzDataFactory** erstellt eine Data Factory mit dem angegebenen Namen und Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="31b9c-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="31b9c-107">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="31b9c-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="31b9c-108">Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="31b9c-108">Create a data factory.</span></span> 
- <span data-ttu-id="31b9c-109">Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="31b9c-109">Create linked services.</span></span> 
- <span data-ttu-id="31b9c-110">Erstellen von Datasets</span><span class="sxs-lookup"><span data-stu-id="31b9c-110">Create datasets.</span></span> 
- <span data-ttu-id="31b9c-111">Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="31b9c-111">Create a pipeline.</span></span>

## <span data-ttu-id="31b9c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31b9c-112">EXAMPLES</span></span>

### <span data-ttu-id="31b9c-113">Beispiel 1: Erstellen einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="31b9c-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="31b9c-114">Mit diesem Befehl wird eine Data Factory mit dem Namen WikiADF in der Ressourcengruppe ADF in der westus-Position erstellt.</span><span class="sxs-lookup"><span data-stu-id="31b9c-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="31b9c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="31b9c-115">PARAMETERS</span></span>

### <span data-ttu-id="31b9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b9c-116">-DefaultProfile</span></span>
<span data-ttu-id="31b9c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="31b9c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b9c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="31b9c-118">-Force</span></span>
<span data-ttu-id="31b9c-119">Gibt an, dass dieses Cmdlet eine vorhandene Data Factory ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="31b9c-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="31b9c-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="31b9c-120">-Location</span></span>
<span data-ttu-id="31b9c-121">Gibt den Speicherort für die Data Factory an, beispielsweise westus oder eastus.</span><span class="sxs-lookup"><span data-stu-id="31b9c-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="31b9c-122">Derzeit wird nur westus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="31b9c-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="31b9c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="31b9c-123">-Name</span></span>
<span data-ttu-id="31b9c-124">Gibt den Namen der Daten Factory an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="31b9c-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="31b9c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b9c-125">-ResourceGroupName</span></span>
<span data-ttu-id="31b9c-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="31b9c-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="31b9c-127">Mit diesem Cmdlet wird eine Data Factory erstellt, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="31b9c-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="31b9c-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="31b9c-128">-Tag</span></span>
<span data-ttu-id="31b9c-129">Die Tags der Data Factory.</span><span class="sxs-lookup"><span data-stu-id="31b9c-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="31b9c-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="31b9c-130">-Confirm</span></span>
<span data-ttu-id="31b9c-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="31b9c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b9c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b9c-132">-WhatIf</span></span>
<span data-ttu-id="31b9c-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31b9c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31b9c-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31b9c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b9c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b9c-135">CommonParameters</span></span>
<span data-ttu-id="31b9c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b9c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b9c-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b9c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b9c-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31b9c-138">INPUTS</span></span>

### <span data-ttu-id="31b9c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="31b9c-139">System.String</span></span>

### <span data-ttu-id="31b9c-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="31b9c-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="31b9c-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31b9c-141">OUTPUTS</span></span>

### <span data-ttu-id="31b9c-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="31b9c-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="31b9c-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="31b9c-143">NOTES</span></span>
* <span data-ttu-id="31b9c-144">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="31b9c-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="31b9c-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31b9c-145">RELATED LINKS</span></span>

[<span data-ttu-id="31b9c-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="31b9c-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="31b9c-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="31b9c-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


