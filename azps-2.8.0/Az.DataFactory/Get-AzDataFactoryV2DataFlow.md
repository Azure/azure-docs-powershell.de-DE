---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: ad27587e52533af1ef7989d4b52de3319137640d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651773"
---
# <span data-ttu-id="0ac95-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="0ac95-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="0ac95-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ac95-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac95-103">Ruft Informationen zu Datenströmen in Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="0ac95-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="0ac95-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ac95-104">SYNTAX</span></span>

### <span data-ttu-id="0ac95-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ac95-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ac95-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0ac95-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ac95-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ac95-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ac95-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ac95-108">DESCRIPTION</span></span>
<span data-ttu-id="0ac95-109">Das Get-AzDataFactoryV2DataFlow-Cmdlet ruft Informationen zu Datenströmen in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="0ac95-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="0ac95-110">Wenn Sie den Namen eines Datenflusses angeben, ruft dieses Cmdlet Informationen zu diesem Datenfluss ab.</span><span class="sxs-lookup"><span data-stu-id="0ac95-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="0ac95-111">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datenströmen in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="0ac95-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="0ac95-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ac95-112">EXAMPLES</span></span>
### <span data-ttu-id="0ac95-113">Beispiel 1: Abrufen von Informationen zu allen Datenströmen</span><span class="sxs-lookup"><span data-stu-id="0ac95-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="0ac95-114">Dieser Befehl ruft Informationen zu allen Datenströmen in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="0ac95-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="0ac95-115">Beispiel 2: Abrufen von Informationen zu einem bestimmten Datenfluss</span><span class="sxs-lookup"><span data-stu-id="0ac95-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="0ac95-116">Dieser Befehl ruft Informationen über den Datenfluss mit dem Namen dataflow1 in der Data Factory mit dem Namen WikiADF ab.</span><span class="sxs-lookup"><span data-stu-id="0ac95-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="0ac95-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ac95-117">PARAMETERS</span></span>

### <span data-ttu-id="0ac95-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0ac95-118">-DataFactory</span></span>
<span data-ttu-id="0ac95-119">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0ac95-119">The data factory object.</span></span>

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

### <span data-ttu-id="0ac95-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0ac95-120">-DataFactoryName</span></span>
<span data-ttu-id="0ac95-121">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="0ac95-121">The data factory name.</span></span>

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

### <span data-ttu-id="0ac95-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac95-122">-DefaultProfile</span></span>
<span data-ttu-id="0ac95-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ac95-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ac95-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0ac95-124">-Name</span></span>
<span data-ttu-id="0ac95-125">Der Name des Datenflusses.</span><span class="sxs-lookup"><span data-stu-id="0ac95-125">The data flow name.</span></span>

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

### <span data-ttu-id="0ac95-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ac95-126">-ResourceGroupName</span></span>
<span data-ttu-id="0ac95-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0ac95-127">The resource group name.</span></span>

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

### <span data-ttu-id="0ac95-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0ac95-128">-ResourceId</span></span>
<span data-ttu-id="0ac95-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0ac95-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0ac95-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac95-130">CommonParameters</span></span>
<span data-ttu-id="0ac95-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ac95-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac95-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ac95-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac95-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ac95-133">INPUTS</span></span>

### <span data-ttu-id="0ac95-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0ac95-134">System.String</span></span>

### <span data-ttu-id="0ac95-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0ac95-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0ac95-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ac95-136">OUTPUTS</span></span>

### <span data-ttu-id="0ac95-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="0ac95-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="0ac95-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ac95-138">NOTES</span></span>
<span data-ttu-id="0ac95-139">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="0ac95-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0ac95-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ac95-140">RELATED LINKS</span></span>

[<span data-ttu-id="0ac95-141">Satz-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="0ac95-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="0ac95-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="0ac95-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)