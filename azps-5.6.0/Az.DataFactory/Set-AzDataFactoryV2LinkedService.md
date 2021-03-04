---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 81894fb7aca1cd546988d94d93b14860061863f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946192"
---
# <span data-ttu-id="b1a7e-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b1a7e-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="b1a7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a7e-103">Verknüpft einen Datenspeicher oder einen Clouddienst mit Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="b1a7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1a7e-104">SYNTAX</span></span>

### <span data-ttu-id="b1a7e-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1a7e-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1a7e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1a7e-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1a7e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1a7e-107">DESCRIPTION</span></span>
<span data-ttu-id="b1a7e-108">Das Set-AzDataFactoryV2LinkedService-Cmdlet verknüpft einen Datenspeicher oder einen Clouddienst mit Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="b1a7e-109">Wenn Sie einen Namen für einen verknüpften Dienst angeben, der bereits vorhanden ist, werden Sie in diesem Cmdlet zur Bestätigung aufgefordert, bevor der verknüpfte Dienst ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="b1a7e-110">Wenn Sie den Parameter Erzwingen angeben, ersetzt das Cmdlet den vorhandenen verknüpften Dienst ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="b1a7e-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus: -- Erstellen Sie eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="b1a7e-112">-- Erstellen sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-112">-- Create linked services.</span></span>
<span data-ttu-id="b1a7e-113">- Erstellen Sie Datasets.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-113">-- Create datasets.</span></span>
<span data-ttu-id="b1a7e-114">- Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="b1a7e-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b1a7e-115">EXAMPLES</span></span>

### <span data-ttu-id="b1a7e-116">Beispiel 1: Erstellen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="b1a7e-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="b1a7e-117">Mit diesem Befehl wird ein verknüpfter Dienst namens LinkedServiceCuratedWikiData in der Daten factory mit dem Namen WikiADF erstellt.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="b1a7e-118">Dieser verknüpfte Dienst verknüpft einen in der Datei angegebenen Azure-Blob Store mit der Daten factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="b1a7e-119">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b1a7e-120">Damit Windows PowerShell cmdlet die Ergebnisse formatiert.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="b1a7e-121">Wenn Sie weitere Informationen erhalten möchten, geben Sie Get-Help Formatliste ein.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="b1a7e-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b1a7e-122">PARAMETERS</span></span>

### <span data-ttu-id="b1a7e-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b1a7e-123">-DataFactoryName</span></span>
<span data-ttu-id="b1a7e-124">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b1a7e-125">Dieses Cmdlet erstellt einen verknüpften Dienst für die Daten factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1a7e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a7e-126">-DefaultProfile</span></span>
<span data-ttu-id="b1a7e-127">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1a7e-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="b1a7e-128">-DefinitionFile</span></span>
<span data-ttu-id="b1a7e-129">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-129">The JSON file path.</span></span>

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

### <span data-ttu-id="b1a7e-130">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="b1a7e-130">-Force</span></span>
<span data-ttu-id="b1a7e-131">Führt das Cmdlet aus, ohne zur Bestätigung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b1a7e-132">-Name</span><span class="sxs-lookup"><span data-stu-id="b1a7e-132">-Name</span></span>
<span data-ttu-id="b1a7e-133">Gibt den Namen des verknüpften Diensts an, der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-133">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="b1a7e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a7e-134">-ResourceGroupName</span></span>
<span data-ttu-id="b1a7e-135">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b1a7e-136">Dieses Cmdlet erstellt einen verknüpften Dienst für die Gruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1a7e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1a7e-137">-ResourceId</span></span>
<span data-ttu-id="b1a7e-138">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b1a7e-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1a7e-139">-Confirm</span></span>
<span data-ttu-id="b1a7e-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1a7e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1a7e-141">-WhatIf</span></span>
<span data-ttu-id="b1a7e-142">Zeigt, was geschieht, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b1a7e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a7e-143">CommonParameters</span></span>
<span data-ttu-id="b1a7e-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a7e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a7e-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a7e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a7e-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b1a7e-146">INPUTS</span></span>

### <span data-ttu-id="b1a7e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b1a7e-147">System.String</span></span>

## <span data-ttu-id="b1a7e-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b1a7e-148">OUTPUTS</span></span>

### <span data-ttu-id="b1a7e-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="b1a7e-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="b1a7e-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b1a7e-150">NOTES</span></span>
<span data-ttu-id="b1a7e-151">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="b1a7e-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b1a7e-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b1a7e-152">RELATED LINKS</span></span>

[<span data-ttu-id="b1a7e-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b1a7e-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="b1a7e-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b1a7e-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
