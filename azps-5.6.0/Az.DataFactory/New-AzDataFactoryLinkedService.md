---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5b11273e61689c515cc7ed72f013514fcd309dcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928240"
---
# <span data-ttu-id="d7668-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="d7668-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="d7668-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7668-102">SYNOPSIS</span></span>
<span data-ttu-id="d7668-103">Verknüpft einen Datenspeicher oder einen Clouddienst mit einer Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d7668-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="d7668-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7668-104">SYNTAX</span></span>

### <span data-ttu-id="d7668-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7668-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7668-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d7668-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7668-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7668-107">DESCRIPTION</span></span>
<span data-ttu-id="d7668-108">Das **Cmdlet New-AzDataFactoryLinkedService** verknüpft einen Datenspeicher oder einen Clouddienst mit Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d7668-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="d7668-109">Wenn Sie einen Namen für einen verknüpften Dienst angeben, der bereits vorhanden ist, werden Sie in diesem Cmdlet zur Bestätigung aufgefordert, bevor der verknüpfte Dienst ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d7668-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="d7668-110">Wenn Sie den Parameter *Erzwingen* angeben, ersetzt das Cmdlet den vorhandenen verknüpften Dienst ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="d7668-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="d7668-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="d7668-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="d7668-112">Erstellen Sie eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="d7668-112">Create a data factory.</span></span> 
- <span data-ttu-id="d7668-113">Erstellen sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="d7668-113">Create linked services.</span></span> 
- <span data-ttu-id="d7668-114">Erstellen Sie Datasets.</span><span class="sxs-lookup"><span data-stu-id="d7668-114">Create datasets.</span></span> 
- <span data-ttu-id="d7668-115">Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d7668-115">Create a pipeline.</span></span>

## <span data-ttu-id="d7668-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d7668-116">EXAMPLES</span></span>

### <span data-ttu-id="d7668-117">Beispiel 1: Erstellen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="d7668-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="d7668-118">Mit diesem Befehl wird ein verknüpfter Dienst namens LinkedServiceCuratedWikiData in der Daten factory mit dem Namen WikiADF erstellt.</span><span class="sxs-lookup"><span data-stu-id="d7668-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="d7668-119">Dieser verknüpfte Dienst verknüpft einen in der Datei angegebenen Azure-Blob Store mit der Daten factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d7668-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="d7668-120">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7668-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d7668-121">Damit Windows PowerShell cmdlet die Ergebnisse formatiert.</span><span class="sxs-lookup"><span data-stu-id="d7668-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="d7668-122">Weitere Informationen finden Sie unter `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="d7668-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="d7668-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d7668-123">PARAMETERS</span></span>

### <span data-ttu-id="d7668-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d7668-124">-DataFactory</span></span>
<span data-ttu-id="d7668-125">Gibt ein **PSDataFactory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="d7668-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d7668-126">Dieses Cmdlet erstellt einen verknüpften Dienst für die Daten factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7668-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7668-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d7668-127">-DataFactoryName</span></span>
<span data-ttu-id="d7668-128">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="d7668-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d7668-129">Dieses Cmdlet erstellt einen verknüpften Dienst für die Daten factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7668-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7668-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7668-130">-DefaultProfile</span></span>
<span data-ttu-id="d7668-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d7668-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7668-132">-Datei</span><span class="sxs-lookup"><span data-stu-id="d7668-132">-File</span></span>
<span data-ttu-id="d7668-133">Gibt den vollständigen Pfad der JSON(JavaScript Object Notation)-Datei an, die die Beschreibung des verknüpften Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="d7668-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7668-134">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d7668-134">-Force</span></span>
<span data-ttu-id="d7668-135">Gibt an, dass dieses Cmdlet einen vorhandenen verknüpften Dienst ersetzt, ohne Dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="d7668-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d7668-136">-Name</span><span class="sxs-lookup"><span data-stu-id="d7668-136">-Name</span></span>
<span data-ttu-id="d7668-137">Gibt den Namen des verknüpften Diensts an, der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7668-137">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7668-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7668-138">-ResourceGroupName</span></span>
<span data-ttu-id="d7668-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d7668-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d7668-140">Dieses Cmdlet erstellt einen verknüpften Dienst für die Gruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7668-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7668-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7668-141">-Confirm</span></span>
<span data-ttu-id="d7668-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7668-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7668-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7668-143">-WhatIf</span></span>
<span data-ttu-id="d7668-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7668-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7668-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7668-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7668-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7668-146">CommonParameters</span></span>
<span data-ttu-id="d7668-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7668-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7668-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7668-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7668-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d7668-149">INPUTS</span></span>

### <span data-ttu-id="d7668-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d7668-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d7668-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d7668-151">System.String</span></span>

## <span data-ttu-id="d7668-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d7668-152">OUTPUTS</span></span>

### <span data-ttu-id="d7668-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="d7668-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="d7668-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d7668-154">NOTES</span></span>
* <span data-ttu-id="d7668-155">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="d7668-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d7668-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d7668-156">RELATED LINKS</span></span>

[<span data-ttu-id="d7668-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="d7668-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="d7668-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="d7668-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


