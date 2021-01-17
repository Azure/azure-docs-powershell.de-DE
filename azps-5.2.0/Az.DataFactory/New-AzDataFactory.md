---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 450a833656f6508f70ebd97f5387075c1711c5f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372867"
---
# <span data-ttu-id="ff84a-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="ff84a-101">New-AzDataFactory</span></span>

## <span data-ttu-id="ff84a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff84a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff84a-103">Erstellt eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="ff84a-103">Creates a data factory.</span></span>

## <span data-ttu-id="ff84a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff84a-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff84a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff84a-105">DESCRIPTION</span></span>
<span data-ttu-id="ff84a-106">Das **Cmdlet "New-AzDataFactory"** erstellt eine Datenfactory mit dem angegebenen Ressourcengruppennamen und -ort.</span><span class="sxs-lookup"><span data-stu-id="ff84a-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="ff84a-107">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="ff84a-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="ff84a-108">Erstellen Sie eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="ff84a-108">Create a data factory.</span></span> 
- <span data-ttu-id="ff84a-109">Erstellen verknüpfter Dienste</span><span class="sxs-lookup"><span data-stu-id="ff84a-109">Create linked services.</span></span> 
- <span data-ttu-id="ff84a-110">Erstellen sie Datasets.</span><span class="sxs-lookup"><span data-stu-id="ff84a-110">Create datasets.</span></span> 
- <span data-ttu-id="ff84a-111">Erstellen sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ff84a-111">Create a pipeline.</span></span>

## <span data-ttu-id="ff84a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ff84a-112">EXAMPLES</span></span>

### <span data-ttu-id="ff84a-113">Beispiel 1: Erstellen einer Daten factory</span><span class="sxs-lookup"><span data-stu-id="ff84a-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="ff84a-114">Mit diesem Befehl wird eine Daten factory namens WikiADF in der Ressourcengruppe namens ADF am Speicherort "WestUS" erstellt.</span><span class="sxs-lookup"><span data-stu-id="ff84a-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="ff84a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff84a-115">PARAMETERS</span></span>

### <span data-ttu-id="ff84a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff84a-116">-DefaultProfile</span></span>
<span data-ttu-id="ff84a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ff84a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff84a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ff84a-118">-Force</span></span>
<span data-ttu-id="ff84a-119">Gibt an, dass dieses Cmdlet eine vorhandene Daten factory ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="ff84a-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ff84a-120">-Location</span><span class="sxs-lookup"><span data-stu-id="ff84a-120">-Location</span></span>
<span data-ttu-id="ff84a-121">Gibt den Speicherort für die Daten factory an, z. B. "WestUS" oder "EastUS".</span><span class="sxs-lookup"><span data-stu-id="ff84a-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="ff84a-122">Derzeit wird nur WestUS unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ff84a-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="ff84a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ff84a-123">-Name</span></span>
<span data-ttu-id="ff84a-124">Gibt den Namen der zu erstellenden Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="ff84a-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="ff84a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff84a-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff84a-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ff84a-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ff84a-127">Dieses Cmdlet erstellt eine Daten factory, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ff84a-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff84a-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff84a-128">-Tag</span></span>
<span data-ttu-id="ff84a-129">Die Tags der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="ff84a-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="ff84a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff84a-130">-Confirm</span></span>
<span data-ttu-id="ff84a-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ff84a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff84a-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ff84a-132">-WhatIf</span></span>
<span data-ttu-id="ff84a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff84a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff84a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff84a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff84a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff84a-135">CommonParameters</span></span>
<span data-ttu-id="ff84a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff84a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff84a-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff84a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff84a-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ff84a-138">INPUTS</span></span>

### <span data-ttu-id="ff84a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ff84a-139">System.String</span></span>

### <span data-ttu-id="ff84a-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ff84a-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ff84a-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ff84a-141">OUTPUTS</span></span>

### <span data-ttu-id="ff84a-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ff84a-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ff84a-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ff84a-143">NOTES</span></span>
* <span data-ttu-id="ff84a-144">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="ff84a-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ff84a-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ff84a-145">RELATED LINKS</span></span>

[<span data-ttu-id="ff84a-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="ff84a-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="ff84a-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="ff84a-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


