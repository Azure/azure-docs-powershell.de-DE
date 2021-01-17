---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 42d9de3f23f1aca904aa0f42722217d0b9bf8a3a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357760"
---
# <span data-ttu-id="22ab8-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="22ab8-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="22ab8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="22ab8-103">Erstellt einen Datenfluss in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="22ab8-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="22ab8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22ab8-104">SYNTAX</span></span>

### <span data-ttu-id="22ab8-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="22ab8-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22ab8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="22ab8-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22ab8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22ab8-107">DESCRIPTION</span></span>
<span data-ttu-id="22ab8-108">Das Set-AzDataFactoryV2DataFlow cmdlet erstellt einen Datenfluss oder aktualisiert einen vorhandenen Datenfluss in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="22ab8-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="22ab8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22ab8-109">EXAMPLES</span></span>

### <span data-ttu-id="22ab8-110">Beispiel 1: Erstellen eines Datenflusses</span><span class="sxs-lookup"><span data-stu-id="22ab8-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="22ab8-111">Dieser Befehl erstellt einen Datenfluss namens "TaxiDemo1" in der Daten factory namens WikiADF.</span><span class="sxs-lookup"><span data-stu-id="22ab8-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="22ab8-112">Der Befehl basiert auf Den Datenfluss auf Informationen im TaxiDemo1.jsDatei.</span><span class="sxs-lookup"><span data-stu-id="22ab8-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="22ab8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22ab8-113">PARAMETERS</span></span>

### <span data-ttu-id="22ab8-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="22ab8-114">-DataFactoryName</span></span>
<span data-ttu-id="22ab8-115">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="22ab8-115">The data factory name.</span></span>

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

### <span data-ttu-id="22ab8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ab8-116">-DefaultProfile</span></span>
<span data-ttu-id="22ab8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22ab8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22ab8-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="22ab8-118">-DefinitionFile</span></span>
<span data-ttu-id="22ab8-119">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="22ab8-119">The JSON file path.</span></span>

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

### <span data-ttu-id="22ab8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="22ab8-120">-Force</span></span>
<span data-ttu-id="22ab8-121">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="22ab8-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="22ab8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="22ab8-122">-Name</span></span>
<span data-ttu-id="22ab8-123">Der Datenflussname.</span><span class="sxs-lookup"><span data-stu-id="22ab8-123">The data flow name.</span></span>

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

### <span data-ttu-id="22ab8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ab8-124">-ResourceGroupName</span></span>
<span data-ttu-id="22ab8-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="22ab8-125">The resource group name.</span></span>

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

### <span data-ttu-id="22ab8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22ab8-126">-ResourceId</span></span>
<span data-ttu-id="22ab8-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="22ab8-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="22ab8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22ab8-128">-Confirm</span></span>
<span data-ttu-id="22ab8-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22ab8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ab8-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="22ab8-130">-WhatIf</span></span>
<span data-ttu-id="22ab8-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22ab8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22ab8-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22ab8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ab8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ab8-133">CommonParameters</span></span>
<span data-ttu-id="22ab8-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ab8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ab8-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22ab8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ab8-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22ab8-136">INPUTS</span></span>

### <span data-ttu-id="22ab8-137">System.String</span><span class="sxs-lookup"><span data-stu-id="22ab8-137">System.String</span></span>

## <span data-ttu-id="22ab8-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22ab8-138">OUTPUTS</span></span>

### <span data-ttu-id="22ab8-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="22ab8-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="22ab8-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="22ab8-140">NOTES</span></span>
<span data-ttu-id="22ab8-141">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="22ab8-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="22ab8-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="22ab8-142">RELATED LINKS</span></span>

[<span data-ttu-id="22ab8-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="22ab8-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="22ab8-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="22ab8-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
