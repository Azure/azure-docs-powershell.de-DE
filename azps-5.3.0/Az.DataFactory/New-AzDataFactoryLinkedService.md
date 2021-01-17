---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 09b766ec77b9f915a03bf6f5b20bd53941b66fc9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472662"
---
# <span data-ttu-id="cdb0d-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="cdb0d-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="cdb0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdb0d-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb0d-103">Verknüpft einen Datenspeicher oder einen Clouddienst mit einer Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="cdb0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdb0d-104">SYNTAX</span></span>

### <span data-ttu-id="cdb0d-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cdb0d-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdb0d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cdb0d-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdb0d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cdb0d-107">DESCRIPTION</span></span>
<span data-ttu-id="cdb0d-108">Das **Cmdlet "New-AzDataFactoryLinkedService"** verknüpft einen Datenspeicher oder einen Clouddienst mit Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="cdb0d-109">Wenn Sie einen Namen für einen verknüpften Dienst angeben, der bereits vorhanden ist, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor der verknüpfte Dienst ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="cdb0d-110">Wenn Sie den Parameter *"Erzwingen"* angeben, ersetzt das Cmdlet den vorhandenen verknüpften Dienst ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="cdb0d-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="cdb0d-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="cdb0d-112">Erstellen Sie eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-112">Create a data factory.</span></span> 
- <span data-ttu-id="cdb0d-113">Erstellen verknüpfter Dienste</span><span class="sxs-lookup"><span data-stu-id="cdb0d-113">Create linked services.</span></span> 
- <span data-ttu-id="cdb0d-114">Erstellen von Datasets</span><span class="sxs-lookup"><span data-stu-id="cdb0d-114">Create datasets.</span></span> 
- <span data-ttu-id="cdb0d-115">Erstellen sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-115">Create a pipeline.</span></span>

## <span data-ttu-id="cdb0d-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cdb0d-116">EXAMPLES</span></span>

### <span data-ttu-id="cdb0d-117">Beispiel 1: Erstellen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="cdb0d-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="cdb0d-118">Mit diesem Befehl wird ein verknüpfter Dienst mit dem Namen "LinkedServiceCuratedWikiData" in der Daten factory namens "WikiADF" erstellt.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="cdb0d-119">Dieser verknüpfte Dienst verknüpft einen Azure-BLOB-Speicher, der in der Datei angegeben ist, mit der Daten factory namens WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="cdb0d-120">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators Format-List an das Format-List Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cdb0d-121">Auf Windows PowerShell cmdlet werden die Ergebnisse formatiert.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="cdb0d-122">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Format-List` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="cdb0d-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdb0d-123">PARAMETERS</span></span>

### <span data-ttu-id="cdb0d-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cdb0d-124">-DataFactory</span></span>
<span data-ttu-id="cdb0d-125">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cdb0d-126">Dieses Cmdlet erstellt einen verknüpften Dienst für die Daten factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdb0d-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cdb0d-127">-DataFactoryName</span></span>
<span data-ttu-id="cdb0d-128">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cdb0d-129">Dieses Cmdlet erstellt einen verknüpften Dienst für die Daten factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdb0d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb0d-130">-DefaultProfile</span></span>
<span data-ttu-id="cdb0d-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cdb0d-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdb0d-132">-File</span><span class="sxs-lookup"><span data-stu-id="cdb0d-132">-File</span></span>
<span data-ttu-id="cdb0d-133">Gibt den vollständigen Pfad der JavaScript Object Notation (JSON)-Datei an, die die Beschreibung des verknüpften Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="cdb0d-134">-Force</span><span class="sxs-lookup"><span data-stu-id="cdb0d-134">-Force</span></span>
<span data-ttu-id="cdb0d-135">Zeigt an, dass dieses Cmdlet einen vorhandenen verknüpften Dienst ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="cdb0d-136">-Name</span><span class="sxs-lookup"><span data-stu-id="cdb0d-136">-Name</span></span>
<span data-ttu-id="cdb0d-137">Gibt den Namen des verknüpften Diensts an, der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-137">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="cdb0d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb0d-138">-ResourceGroupName</span></span>
<span data-ttu-id="cdb0d-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cdb0d-140">Dieses Cmdlet erstellt einen verknüpften Dienst für die Gruppe, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdb0d-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdb0d-141">-Confirm</span></span>
<span data-ttu-id="cdb0d-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb0d-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cdb0d-143">-WhatIf</span></span>
<span data-ttu-id="cdb0d-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdb0d-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb0d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb0d-146">CommonParameters</span></span>
<span data-ttu-id="cdb0d-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb0d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb0d-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb0d-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb0d-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cdb0d-149">INPUTS</span></span>

### <span data-ttu-id="cdb0d-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cdb0d-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="cdb0d-151">System.String</span><span class="sxs-lookup"><span data-stu-id="cdb0d-151">System.String</span></span>

## <span data-ttu-id="cdb0d-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cdb0d-152">OUTPUTS</span></span>

### <span data-ttu-id="cdb0d-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="cdb0d-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="cdb0d-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cdb0d-154">NOTES</span></span>
* <span data-ttu-id="cdb0d-155">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="cdb0d-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cdb0d-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cdb0d-156">RELATED LINKS</span></span>

[<span data-ttu-id="cdb0d-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="cdb0d-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="cdb0d-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="cdb0d-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


