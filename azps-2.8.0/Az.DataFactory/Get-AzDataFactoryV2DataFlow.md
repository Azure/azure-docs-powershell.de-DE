---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 369540a80ec6ffdc02f96783de5e86cc50f0c8f3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407062"
---
# <span data-ttu-id="f994f-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="f994f-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="f994f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f994f-102">SYNOPSIS</span></span>
<span data-ttu-id="f994f-103">Ruft Informationen zu Datenflüssen in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="f994f-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="f994f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f994f-104">SYNTAX</span></span>

### <span data-ttu-id="f994f-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f994f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f994f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f994f-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f994f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f994f-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f994f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f994f-108">DESCRIPTION</span></span>
<span data-ttu-id="f994f-109">Das Get-AzDataFactoryV2DataFlow Cmdlet ruft Informationen zu Datenflüssen in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="f994f-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="f994f-110">Wenn Sie den Namen eines Datenflusses angeben, ruft dieses Cmdlet Informationen zu diesem Datenfluss ab.</span><span class="sxs-lookup"><span data-stu-id="f994f-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="f994f-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datenflüssen in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="f994f-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="f994f-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f994f-112">EXAMPLES</span></span>
### <span data-ttu-id="f994f-113">Beispiel 1: Informationen zu allen Datenflüssen</span><span class="sxs-lookup"><span data-stu-id="f994f-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="f994f-114">Dieser Befehl ruft Informationen zu allen Datenflüssen in der Daten factory namens WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="f994f-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="f994f-115">Beispiel 2: Erhalten von Informationen zu einem bestimmten Datenfluss</span><span class="sxs-lookup"><span data-stu-id="f994f-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="f994f-116">Dieser Befehl ruft Informationen über den Datenfluss namens "dataflow1" in der Daten factory namens WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="f994f-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="f994f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f994f-117">PARAMETERS</span></span>

### <span data-ttu-id="f994f-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f994f-118">-DataFactory</span></span>
<span data-ttu-id="f994f-119">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f994f-119">The data factory object.</span></span>

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

### <span data-ttu-id="f994f-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f994f-120">-DataFactoryName</span></span>
<span data-ttu-id="f994f-121">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="f994f-121">The data factory name.</span></span>

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

### <span data-ttu-id="f994f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f994f-122">-DefaultProfile</span></span>
<span data-ttu-id="f994f-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f994f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f994f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f994f-124">-Name</span></span>
<span data-ttu-id="f994f-125">Der Datenflussname.</span><span class="sxs-lookup"><span data-stu-id="f994f-125">The data flow name.</span></span>

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

### <span data-ttu-id="f994f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f994f-126">-ResourceGroupName</span></span>
<span data-ttu-id="f994f-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f994f-127">The resource group name.</span></span>

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

### <span data-ttu-id="f994f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f994f-128">-ResourceId</span></span>
<span data-ttu-id="f994f-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f994f-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f994f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f994f-130">CommonParameters</span></span>
<span data-ttu-id="f994f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f994f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f994f-132">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f994f-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f994f-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f994f-133">INPUTS</span></span>

### <span data-ttu-id="f994f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f994f-134">System.String</span></span>

### <span data-ttu-id="f994f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f994f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f994f-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f994f-136">OUTPUTS</span></span>

### <span data-ttu-id="f994f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="f994f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="f994f-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f994f-138">NOTES</span></span>
<span data-ttu-id="f994f-139">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="f994f-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f994f-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f994f-140">RELATED LINKS</span></span>


