---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: a563d6b0e72c60632d99df2668552b649ffb1662
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651672"
---
# <span data-ttu-id="2ac73-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="2ac73-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="2ac73-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ac73-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac73-103">Erstellt einen Datenfluss in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2ac73-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="2ac73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ac73-104">SYNTAX</span></span>

### <span data-ttu-id="2ac73-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ac73-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ac73-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2ac73-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ac73-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ac73-107">DESCRIPTION</span></span>
<span data-ttu-id="2ac73-108">Das Set-AzDataFactoryV2DataFlow-Cmdlet erstellt einen Datenfluss oder aktualisiert einen vorhandenen Datenfluss in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2ac73-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="2ac73-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ac73-109">EXAMPLES</span></span>

### <span data-ttu-id="2ac73-110">Beispiel 1: Erstellen eines Datenflusses</span><span class="sxs-lookup"><span data-stu-id="2ac73-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="2ac73-111">Dieser Befehl erstellt einen Datenfluss mit dem Namen TaxiDemo1 in der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2ac73-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="2ac73-112">Der Befehl basiert den Datenfluss auf Informationen in der TaxiDemo1.jsDatei.</span><span class="sxs-lookup"><span data-stu-id="2ac73-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="2ac73-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ac73-113">PARAMETERS</span></span>

### <span data-ttu-id="2ac73-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2ac73-114">-DataFactoryName</span></span>
<span data-ttu-id="2ac73-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="2ac73-115">The data factory name.</span></span>

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

### <span data-ttu-id="2ac73-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac73-116">-DefaultProfile</span></span>
<span data-ttu-id="2ac73-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ac73-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ac73-118">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="2ac73-118">-DefinitionFile</span></span>
<span data-ttu-id="2ac73-119">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="2ac73-119">The JSON file path.</span></span>

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

### <span data-ttu-id="2ac73-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2ac73-120">-Force</span></span>
<span data-ttu-id="2ac73-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="2ac73-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2ac73-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2ac73-122">-Name</span></span>
<span data-ttu-id="2ac73-123">Der Name des Datenflusses.</span><span class="sxs-lookup"><span data-stu-id="2ac73-123">The data flow name.</span></span>

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

### <span data-ttu-id="2ac73-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac73-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ac73-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2ac73-125">The resource group name.</span></span>

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

### <span data-ttu-id="2ac73-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2ac73-126">-ResourceId</span></span>
<span data-ttu-id="2ac73-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2ac73-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2ac73-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ac73-128">-Confirm</span></span>
<span data-ttu-id="2ac73-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ac73-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ac73-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ac73-130">-WhatIf</span></span>
<span data-ttu-id="2ac73-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ac73-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ac73-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ac73-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ac73-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac73-133">CommonParameters</span></span>
<span data-ttu-id="2ac73-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac73-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac73-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ac73-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac73-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ac73-136">INPUTS</span></span>

### <span data-ttu-id="2ac73-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac73-137">System.String</span></span>

## <span data-ttu-id="2ac73-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ac73-138">OUTPUTS</span></span>

### <span data-ttu-id="2ac73-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="2ac73-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="2ac73-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ac73-140">NOTES</span></span>
<span data-ttu-id="2ac73-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="2ac73-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2ac73-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ac73-142">RELATED LINKS</span></span>

[<span data-ttu-id="2ac73-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="2ac73-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="2ac73-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="2ac73-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
