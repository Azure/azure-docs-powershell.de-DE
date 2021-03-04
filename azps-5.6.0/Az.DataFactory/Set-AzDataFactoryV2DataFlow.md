---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 6827fb627a3d393c8971886cee869c330f7d4099
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942872"
---
# <span data-ttu-id="7eaf7-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="7eaf7-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="7eaf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eaf7-102">SYNOPSIS</span></span>
<span data-ttu-id="7eaf7-103">Erstellt einen Datenfluss in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="7eaf7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7eaf7-104">SYNTAX</span></span>

### <span data-ttu-id="7eaf7-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7eaf7-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7eaf7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7eaf7-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eaf7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7eaf7-107">DESCRIPTION</span></span>
<span data-ttu-id="7eaf7-108">Das Set-AzDataFactoryV2DataFlow-Cmdlet erstellt einen Datenfluss oder aktualisiert einen vorhandenen Datenfluss in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="7eaf7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7eaf7-109">EXAMPLES</span></span>

### <span data-ttu-id="7eaf7-110">Beispiel 1: Erstellen eines Datenflusses</span><span class="sxs-lookup"><span data-stu-id="7eaf7-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="7eaf7-111">Mit diesem Befehl wird ein Datenfluss mit dem Namen "TaxiDemo1" in der Daten factory mit dem Namen WikiADF erstellt.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="7eaf7-112">Mit dem Befehl wird der Datenfluss auf Informationen in der Datei TaxiDemo1.jsgespeichert.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="7eaf7-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7eaf7-113">PARAMETERS</span></span>

### <span data-ttu-id="7eaf7-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7eaf7-114">-DataFactoryName</span></span>
<span data-ttu-id="7eaf7-115">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eaf7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eaf7-116">-DefaultProfile</span></span>
<span data-ttu-id="7eaf7-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eaf7-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="7eaf7-118">-DefinitionFile</span></span>
<span data-ttu-id="7eaf7-119">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eaf7-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="7eaf7-120">-Force</span></span>
<span data-ttu-id="7eaf7-121">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7eaf7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7eaf7-122">-Name</span></span>
<span data-ttu-id="7eaf7-123">Der Name des Datenflusses.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eaf7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eaf7-124">-ResourceGroupName</span></span>
<span data-ttu-id="7eaf7-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eaf7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7eaf7-126">-ResourceId</span></span>
<span data-ttu-id="7eaf7-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eaf7-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7eaf7-128">-Confirm</span></span>
<span data-ttu-id="7eaf7-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eaf7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eaf7-130">-WhatIf</span></span>
<span data-ttu-id="7eaf7-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eaf7-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eaf7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eaf7-133">CommonParameters</span></span>
<span data-ttu-id="7eaf7-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eaf7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eaf7-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7eaf7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eaf7-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7eaf7-136">INPUTS</span></span>

### <span data-ttu-id="7eaf7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7eaf7-137">System.String</span></span>

## <span data-ttu-id="7eaf7-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7eaf7-138">OUTPUTS</span></span>

### <span data-ttu-id="7eaf7-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="7eaf7-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="7eaf7-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7eaf7-140">NOTES</span></span>
<span data-ttu-id="7eaf7-141">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="7eaf7-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7eaf7-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7eaf7-142">RELATED LINKS</span></span>

[<span data-ttu-id="7eaf7-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="7eaf7-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="7eaf7-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="7eaf7-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
