---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: d6fd12e96a98d0771a984aa5234013dbe4a548af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472635"
---
# <span data-ttu-id="2cbd8-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="2cbd8-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="2cbd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cbd8-102">SYNOPSIS</span></span>
<span data-ttu-id="2cbd8-103">Verknüpft einen Datenspeicher oder einen Clouddienst mit Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="2cbd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cbd8-104">SYNTAX</span></span>

### <span data-ttu-id="2cbd8-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2cbd8-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cbd8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2cbd8-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cbd8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2cbd8-107">DESCRIPTION</span></span>
<span data-ttu-id="2cbd8-108">Das Set-AzDataFactoryV2LinkedService verknüpft einen Datenspeicher oder einen Clouddienst mit Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="2cbd8-109">Wenn Sie einen Namen für einen verknüpften Dienst angeben, der bereits vorhanden ist, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor der verknüpfte Dienst ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="2cbd8-110">Wenn Sie den Parameter "Erzwingen" angeben, ersetzt das Cmdlet den vorhandenen verknüpften Dienst ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="2cbd8-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus: -- Erstellen Sie eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="2cbd8-112">- Verknüpfte Dienste erstellen.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-112">-- Create linked services.</span></span>
<span data-ttu-id="2cbd8-113">– Erstellen sie Datasets.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-113">-- Create datasets.</span></span>
<span data-ttu-id="2cbd8-114">– Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="2cbd8-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2cbd8-115">EXAMPLES</span></span>

### <span data-ttu-id="2cbd8-116">Beispiel 1: Erstellen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="2cbd8-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="2cbd8-117">Mit diesem Befehl wird ein verknüpfter Dienst mit dem Namen "LinkedServiceCuratedWikiData" in der Daten factory namens "WikiADF" erstellt.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="2cbd8-118">Dieser verknüpfte Dienst verknüpft einen Azure-BLOB-Speicher, der in der Datei angegeben ist, mit der Daten factory namens WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="2cbd8-119">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators Format-List an das Format-List Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2cbd8-120">Auf Windows PowerShell cmdlet werden die Ergebnisse formatiert.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="2cbd8-121">Wenn Sie weitere Informationen erhalten möchten, geben Get-Help "Format-Liste" ein.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="2cbd8-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cbd8-122">PARAMETERS</span></span>

### <span data-ttu-id="2cbd8-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2cbd8-123">-DataFactoryName</span></span>
<span data-ttu-id="2cbd8-124">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2cbd8-125">Dieses Cmdlet erstellt einen verknüpften Dienst für die Daten factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2cbd8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cbd8-126">-DefaultProfile</span></span>
<span data-ttu-id="2cbd8-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cbd8-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="2cbd8-128">-DefinitionFile</span></span>
<span data-ttu-id="2cbd8-129">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-129">The JSON file path.</span></span>

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

### <span data-ttu-id="2cbd8-130">-Force</span><span class="sxs-lookup"><span data-stu-id="2cbd8-130">-Force</span></span>
<span data-ttu-id="2cbd8-131">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2cbd8-132">-Name</span><span class="sxs-lookup"><span data-stu-id="2cbd8-132">-Name</span></span>
<span data-ttu-id="2cbd8-133">Gibt den Namen des verknüpften Diensts an, der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-133">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cbd8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cbd8-134">-ResourceGroupName</span></span>
<span data-ttu-id="2cbd8-135">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2cbd8-136">Dieses Cmdlet erstellt einen verknüpften Dienst für die Gruppe, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2cbd8-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cbd8-137">-ResourceId</span></span>
<span data-ttu-id="2cbd8-138">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2cbd8-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cbd8-139">-Confirm</span></span>
<span data-ttu-id="2cbd8-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cbd8-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2cbd8-141">-WhatIf</span></span>
<span data-ttu-id="2cbd8-142">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2cbd8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cbd8-143">CommonParameters</span></span>
<span data-ttu-id="2cbd8-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cbd8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cbd8-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cbd8-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cbd8-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2cbd8-146">INPUTS</span></span>

### <span data-ttu-id="2cbd8-147">System.String</span><span class="sxs-lookup"><span data-stu-id="2cbd8-147">System.String</span></span>

## <span data-ttu-id="2cbd8-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2cbd8-148">OUTPUTS</span></span>

### <span data-ttu-id="2cbd8-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="2cbd8-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="2cbd8-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2cbd8-150">NOTES</span></span>
<span data-ttu-id="2cbd8-151">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="2cbd8-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2cbd8-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2cbd8-152">RELATED LINKS</span></span>

[<span data-ttu-id="2cbd8-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="2cbd8-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="2cbd8-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="2cbd8-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
