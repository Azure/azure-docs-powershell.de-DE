---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 09b766ec77b9f915a03bf6f5b20bd53941b66fc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167020"
---
# <span data-ttu-id="626fc-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="626fc-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="626fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="626fc-102">SYNOPSIS</span></span>
<span data-ttu-id="626fc-103">Verknüpft einen Datenspeicher oder einen clouddienst mit einer Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="626fc-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="626fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="626fc-104">SYNTAX</span></span>

### <span data-ttu-id="626fc-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="626fc-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="626fc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="626fc-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="626fc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="626fc-107">DESCRIPTION</span></span>
<span data-ttu-id="626fc-108">Das Cmdlet **New-AzDataFactoryLinkedService** verknüpft einen Datenspeicher oder einen clouddienst mit Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="626fc-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="626fc-109">Wenn Sie einen Namen für einen verknüpften Dienst angeben, der bereits vorhanden ist, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor der verknüpfte Dienst ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="626fc-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="626fc-110">Wenn Sie den Parameter *Force* angeben, wird der vorhandene verknüpfte Dienst ohne Bestätigung durch das Cmdlet ersetzt.</span><span class="sxs-lookup"><span data-stu-id="626fc-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="626fc-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="626fc-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="626fc-112">Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="626fc-112">Create a data factory.</span></span> 
- <span data-ttu-id="626fc-113">Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="626fc-113">Create linked services.</span></span> 
- <span data-ttu-id="626fc-114">Erstellen von Datasets</span><span class="sxs-lookup"><span data-stu-id="626fc-114">Create datasets.</span></span> 
- <span data-ttu-id="626fc-115">Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="626fc-115">Create a pipeline.</span></span>

## <span data-ttu-id="626fc-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="626fc-116">EXAMPLES</span></span>

### <span data-ttu-id="626fc-117">Beispiel 1: Erstellen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="626fc-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="626fc-118">Dieser Befehl erstellt einen verknüpften Dienst mit dem Namen LinkedServiceCuratedWikiData in der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="626fc-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="626fc-119">Dieser verknüpfte Dienst verknüpft einen in der Datei angegebenen Azure BLOB-Speicher mit der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="626fc-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="626fc-120">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="626fc-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="626fc-121">Das Windows PowerShell-Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="626fc-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="626fc-122">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="626fc-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="626fc-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="626fc-123">PARAMETERS</span></span>

### <span data-ttu-id="626fc-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="626fc-124">-DataFactory</span></span>
<span data-ttu-id="626fc-125">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="626fc-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="626fc-126">Mit diesem Cmdlet wird ein verknüpfter Dienst für die Data Factory erstellt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="626fc-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="626fc-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="626fc-127">-DataFactoryName</span></span>
<span data-ttu-id="626fc-128">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="626fc-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="626fc-129">Mit diesem Cmdlet wird ein verknüpfter Dienst für die Data Factory erstellt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="626fc-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="626fc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="626fc-130">-DefaultProfile</span></span>
<span data-ttu-id="626fc-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="626fc-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="626fc-132">-Datei</span><span class="sxs-lookup"><span data-stu-id="626fc-132">-File</span></span>
<span data-ttu-id="626fc-133">Gibt den vollständigen Pfad der JSON-Datei (JavaScript Object Notation) an, die die Beschreibung des verknüpften Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="626fc-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="626fc-134">-Force</span><span class="sxs-lookup"><span data-stu-id="626fc-134">-Force</span></span>
<span data-ttu-id="626fc-135">Gibt an, dass dieses Cmdlet einen vorhandenen verknüpften Dienst ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="626fc-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="626fc-136">-Name</span><span class="sxs-lookup"><span data-stu-id="626fc-136">-Name</span></span>
<span data-ttu-id="626fc-137">Gibt den Namen des verknüpften Diensts an, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="626fc-137">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="626fc-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="626fc-138">-ResourceGroupName</span></span>
<span data-ttu-id="626fc-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="626fc-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="626fc-140">Mit diesem Cmdlet wird ein verknüpfter Dienst für die von diesem Parameter festgelegte Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="626fc-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="626fc-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="626fc-141">-Confirm</span></span>
<span data-ttu-id="626fc-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="626fc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="626fc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="626fc-143">-WhatIf</span></span>
<span data-ttu-id="626fc-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="626fc-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="626fc-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="626fc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="626fc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="626fc-146">CommonParameters</span></span>
<span data-ttu-id="626fc-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="626fc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="626fc-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="626fc-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="626fc-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="626fc-149">INPUTS</span></span>

### <span data-ttu-id="626fc-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="626fc-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="626fc-151">System. String</span><span class="sxs-lookup"><span data-stu-id="626fc-151">System.String</span></span>

## <span data-ttu-id="626fc-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="626fc-152">OUTPUTS</span></span>

### <span data-ttu-id="626fc-153">Microsoft. Azure. Commands. datafactoring. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="626fc-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="626fc-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="626fc-154">NOTES</span></span>
* <span data-ttu-id="626fc-155">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="626fc-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="626fc-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="626fc-156">RELATED LINKS</span></span>

[<span data-ttu-id="626fc-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="626fc-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="626fc-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="626fc-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


