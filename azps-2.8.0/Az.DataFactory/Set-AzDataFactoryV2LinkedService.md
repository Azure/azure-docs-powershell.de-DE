---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 2ff8e4a92c01c38b81ad5f1fded5661501b1c46c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651667"
---
# <span data-ttu-id="e1c46-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e1c46-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="e1c46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1c46-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c46-103">Verknüpft einen Datenspeicher oder einen clouddienst mit Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e1c46-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="e1c46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1c46-104">SYNTAX</span></span>

### <span data-ttu-id="e1c46-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1c46-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1c46-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1c46-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1c46-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1c46-107">DESCRIPTION</span></span>
<span data-ttu-id="e1c46-108">Das Set-AzDataFactoryV2LinkedService-Cmdlet verknüpft einen Datenspeicher oder einen clouddienst mit Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e1c46-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="e1c46-109">Wenn Sie einen Namen für einen verknüpften Dienst angeben, der bereits vorhanden ist, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor der verknüpfte Dienst ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="e1c46-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="e1c46-110">Wenn Sie den Parameter Force angeben, wird der vorhandene verknüpfte Dienst ohne Bestätigung durch das Cmdlet ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e1c46-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="e1c46-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:--Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e1c46-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="e1c46-112">--Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="e1c46-112">-- Create linked services.</span></span>
<span data-ttu-id="e1c46-113">--Erstellen von Datasets.</span><span class="sxs-lookup"><span data-stu-id="e1c46-113">-- Create datasets.</span></span>
<span data-ttu-id="e1c46-114">--Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e1c46-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="e1c46-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1c46-115">EXAMPLES</span></span>

### <span data-ttu-id="e1c46-116">Beispiel 1: Erstellen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="e1c46-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="e1c46-117">Dieser Befehl erstellt einen verknüpften Dienst mit dem Namen LinkedServiceCuratedWikiData in der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e1c46-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="e1c46-118">Dieser verknüpfte Dienst verknüpft einen in der Datei angegebenen Azure BLOB-Speicher mit der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e1c46-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="e1c46-119">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1c46-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e1c46-120">Das Windows PowerShell-Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="e1c46-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="e1c46-121">Wenn Sie weitere Informationen wünschen, geben Sie Get-Help Format-List ein.</span><span class="sxs-lookup"><span data-stu-id="e1c46-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="e1c46-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1c46-122">PARAMETERS</span></span>

### <span data-ttu-id="e1c46-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e1c46-123">-DataFactoryName</span></span>
<span data-ttu-id="e1c46-124">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="e1c46-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e1c46-125">Mit diesem Cmdlet wird ein verknüpfter Dienst für die Data Factory erstellt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e1c46-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e1c46-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c46-126">-DefaultProfile</span></span>
<span data-ttu-id="e1c46-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1c46-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1c46-128">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="e1c46-128">-DefinitionFile</span></span>
<span data-ttu-id="e1c46-129">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="e1c46-129">The JSON file path.</span></span>

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

### <span data-ttu-id="e1c46-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e1c46-130">-Force</span></span>
<span data-ttu-id="e1c46-131">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="e1c46-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e1c46-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e1c46-132">-Name</span></span>
<span data-ttu-id="e1c46-133">Gibt den Namen des verknüpften Diensts an, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="e1c46-133">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="e1c46-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1c46-134">-ResourceGroupName</span></span>
<span data-ttu-id="e1c46-135">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e1c46-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e1c46-136">Mit diesem Cmdlet wird ein verknüpfter Dienst für die von diesem Parameter festgelegte Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1c46-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e1c46-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e1c46-137">-ResourceId</span></span>
<span data-ttu-id="e1c46-138">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e1c46-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e1c46-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1c46-139">-Confirm</span></span>
<span data-ttu-id="e1c46-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1c46-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1c46-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1c46-141">-WhatIf</span></span>
<span data-ttu-id="e1c46-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1c46-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e1c46-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c46-143">CommonParameters</span></span>
<span data-ttu-id="e1c46-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c46-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c46-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1c46-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c46-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1c46-146">INPUTS</span></span>

### <span data-ttu-id="e1c46-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e1c46-147">System.String</span></span>

## <span data-ttu-id="e1c46-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1c46-148">OUTPUTS</span></span>

### <span data-ttu-id="e1c46-149">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="e1c46-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="e1c46-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1c46-150">NOTES</span></span>
<span data-ttu-id="e1c46-151">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="e1c46-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e1c46-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1c46-152">RELATED LINKS</span></span>

[<span data-ttu-id="e1c46-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e1c46-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="e1c46-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e1c46-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
