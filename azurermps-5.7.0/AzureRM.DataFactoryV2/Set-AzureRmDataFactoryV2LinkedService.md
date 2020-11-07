---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 2f7cfba7db5d675a73d21d6cd1814c13a1998ab1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662587"
---
# <span data-ttu-id="ae2b7-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ae2b7-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="ae2b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae2b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2b7-103">Verknüpft einen Datenspeicher oder einen clouddienst mit Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae2b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae2b7-104">SYNTAX</span></span>

### <span data-ttu-id="ae2b7-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ae2b7-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae2b7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae2b7-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae2b7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae2b7-107">DESCRIPTION</span></span>
<span data-ttu-id="ae2b7-108">Das Set-AzureRmDataFactoryV2LinkedService-Cmdlet verknüpft einen Datenspeicher oder einen clouddienst mit Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="ae2b7-109">Wenn Sie einen Namen für einen verknüpften Dienst angeben, der bereits vorhanden ist, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor der verknüpfte Dienst ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="ae2b7-110">Wenn Sie den Parameter Force angeben, wird der vorhandene verknüpfte Dienst ohne Bestätigung durch das Cmdlet ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="ae2b7-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="ae2b7-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="ae2b7-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae2b7-112">EXAMPLES</span></span>

### <span data-ttu-id="ae2b7-113">Beispiel 1: Erstellen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="ae2b7-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="ae2b7-114">Dieser Befehl erstellt einen verknüpften Dienst mit dem Namen LinkedServiceCuratedWikiData in der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="ae2b7-115">Dieser verknüpfte Dienst verknüpft einen in der Datei angegebenen Azure BLOB-Speicher mit der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="ae2b7-116">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ae2b7-117">Das Windows PowerShell-Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="ae2b7-118">Wenn Sie weitere Informationen wünschen, geben Sie Get-Help Format-List ein.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="ae2b7-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae2b7-119">PARAMETERS</span></span>

### <span data-ttu-id="ae2b7-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ae2b7-120">-DataFactoryName</span></span>
<span data-ttu-id="ae2b7-121">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ae2b7-122">Mit diesem Cmdlet wird ein verknüpfter Dienst für die Data Factory erstellt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-122">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2b7-123">-DefaultProfile</span></span>
<span data-ttu-id="ae2b7-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b7-125">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-125">-DefinitionFile</span></span>
<span data-ttu-id="ae2b7-126">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-126">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b7-127">-Force</span><span class="sxs-lookup"><span data-stu-id="ae2b7-127">-Force</span></span>
<span data-ttu-id="ae2b7-128">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-128">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ae2b7-129">-Name</span></span>
<span data-ttu-id="ae2b7-130">Gibt den Namen des verknüpften Diensts an, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-130">Specifies the name of the linked service to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae2b7-131">-ResourceGroupName</span></span>
<span data-ttu-id="ae2b7-132">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ae2b7-133">Mit diesem Cmdlet wird ein verknüpfter Dienst für die von diesem Parameter festgelegte Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b7-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ae2b7-134">-ResourceId</span></span>
<span data-ttu-id="ae2b7-135">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-135">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b7-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ae2b7-136">-Confirm</span></span>
<span data-ttu-id="ae2b7-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae2b7-138">-WhatIf</span></span>
<span data-ttu-id="ae2b7-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-139">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2b7-140">CommonParameters</span></span>
<span data-ttu-id="ae2b7-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae2b7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2b7-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae2b7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2b7-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae2b7-143">INPUTS</span></span>

### <span data-ttu-id="ae2b7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ae2b7-144">System.String</span></span>

## <span data-ttu-id="ae2b7-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae2b7-145">OUTPUTS</span></span>

### <span data-ttu-id="ae2b7-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="ae2b7-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="ae2b7-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae2b7-147">NOTES</span></span>
<span data-ttu-id="ae2b7-148">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="ae2b7-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ae2b7-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae2b7-149">RELATED LINKS</span></span>

[<span data-ttu-id="ae2b7-150">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ae2b7-150">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="ae2b7-151">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ae2b7-151">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
