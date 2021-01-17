---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b4af5eae61e47d8617eb270451f406f349162f50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472682"
---
# <span data-ttu-id="b8193-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="b8193-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="b8193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8193-102">SYNOPSIS</span></span>
<span data-ttu-id="b8193-103">Ruft Informationen zu Datenflüssen in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="b8193-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="b8193-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8193-104">SYNTAX</span></span>

### <span data-ttu-id="b8193-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8193-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8193-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b8193-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8193-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8193-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8193-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8193-108">DESCRIPTION</span></span>
<span data-ttu-id="b8193-109">Das Get-AzDataFactoryV2DataFlow Cmdlet ruft Informationen zu Datenflüssen in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="b8193-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="b8193-110">Wenn Sie den Namen eines Datenflusses angeben, ruft dieses Cmdlet Informationen zu diesem Datenfluss ab.</span><span class="sxs-lookup"><span data-stu-id="b8193-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="b8193-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datenflüssen in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="b8193-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="b8193-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8193-112">EXAMPLES</span></span>
### <span data-ttu-id="b8193-113">Beispiel 1: Informationen zu allen Datenflüssen</span><span class="sxs-lookup"><span data-stu-id="b8193-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="b8193-114">Dieser Befehl ruft Informationen zu allen Datenflüssen in der Daten factory namens WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="b8193-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="b8193-115">Beispiel 2: Erhalten von Informationen zu einem bestimmten Datenfluss</span><span class="sxs-lookup"><span data-stu-id="b8193-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="b8193-116">Dieser Befehl ruft Informationen über den Datenfluss namens "Datenfluss1" in der Daten factory namens WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="b8193-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="b8193-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8193-117">PARAMETERS</span></span>

### <span data-ttu-id="b8193-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8193-118">-DataFactory</span></span>
<span data-ttu-id="b8193-119">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b8193-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8193-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b8193-120">-DataFactoryName</span></span>
<span data-ttu-id="b8193-121">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="b8193-121">The data factory name.</span></span>

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

### <span data-ttu-id="b8193-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8193-122">-DefaultProfile</span></span>
<span data-ttu-id="b8193-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8193-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8193-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b8193-124">-Name</span></span>
<span data-ttu-id="b8193-125">Der Datenflussname.</span><span class="sxs-lookup"><span data-stu-id="b8193-125">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DataFlowName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8193-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8193-126">-ResourceGroupName</span></span>
<span data-ttu-id="b8193-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b8193-127">The resource group name.</span></span>

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

### <span data-ttu-id="b8193-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8193-128">-ResourceId</span></span>
<span data-ttu-id="b8193-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b8193-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b8193-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8193-130">CommonParameters</span></span>
<span data-ttu-id="b8193-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8193-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8193-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8193-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8193-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8193-133">INPUTS</span></span>

### <span data-ttu-id="b8193-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b8193-134">System.String</span></span>

### <span data-ttu-id="b8193-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b8193-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b8193-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8193-136">OUTPUTS</span></span>

### <span data-ttu-id="b8193-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="b8193-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="b8193-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b8193-138">NOTES</span></span>
<span data-ttu-id="b8193-139">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="b8193-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b8193-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b8193-140">RELATED LINKS</span></span>

[<span data-ttu-id="b8193-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="b8193-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="b8193-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="b8193-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)