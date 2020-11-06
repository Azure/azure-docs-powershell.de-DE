---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: c89a7950b70bf3b3b13b053e4e007434afdb078d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496621"
---
# <span data-ttu-id="f8388-101">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="f8388-101">New-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="f8388-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8388-102">SYNOPSIS</span></span>
<span data-ttu-id="f8388-103">Verknüpft einen Datenspeicher oder einen clouddienst mit einer Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f8388-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8388-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8388-104">SYNTAX</span></span>

### <span data-ttu-id="f8388-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8388-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8388-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f8388-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8388-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8388-107">DESCRIPTION</span></span>
<span data-ttu-id="f8388-108">Das Cmdlet **New-AzureRmDataFactoryLinkedService** verknüpft einen Datenspeicher oder einen clouddienst mit Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f8388-108">The **New-AzureRmDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="f8388-109">Wenn Sie einen Namen für einen verknüpften Dienst angeben, der bereits vorhanden ist, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor der verknüpfte Dienst ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f8388-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="f8388-110">Wenn Sie den Parameter *Force* angeben, wird der vorhandene verknüpfte Dienst ohne Bestätigung durch das Cmdlet ersetzt.</span><span class="sxs-lookup"><span data-stu-id="f8388-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="f8388-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="f8388-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="f8388-112">Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f8388-112">Create a data factory.</span></span> 
- <span data-ttu-id="f8388-113">Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="f8388-113">Create linked services.</span></span> 
- <span data-ttu-id="f8388-114">Erstellen von Datasets</span><span class="sxs-lookup"><span data-stu-id="f8388-114">Create datasets.</span></span> 
- <span data-ttu-id="f8388-115">Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f8388-115">Create a pipeline.</span></span>

## <span data-ttu-id="f8388-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8388-116">EXAMPLES</span></span>

### <span data-ttu-id="f8388-117">Beispiel 1: Erstellen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="f8388-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="f8388-118">Dieser Befehl erstellt einen verknüpften Dienst mit dem Namen LinkedServiceCuratedWikiData in der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f8388-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="f8388-119">Dieser verknüpfte Dienst verknüpft einen in der Datei angegebenen Azure BLOB-Speicher mit der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f8388-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="f8388-120">Der Befehl übergibt das Ergebnis mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8388-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f8388-121">Das Windows PowerShell-Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="f8388-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="f8388-122">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="f8388-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="f8388-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8388-123">PARAMETERS</span></span>

### <span data-ttu-id="f8388-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f8388-124">-DataFactory</span></span>
<span data-ttu-id="f8388-125">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f8388-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f8388-126">Mit diesem Cmdlet wird ein verknüpfter Dienst für die Data Factory erstellt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f8388-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8388-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f8388-127">-DataFactoryName</span></span>
<span data-ttu-id="f8388-128">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="f8388-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f8388-129">Mit diesem Cmdlet wird ein verknüpfter Dienst für die Data Factory erstellt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f8388-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8388-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8388-130">-DefaultProfile</span></span>
<span data-ttu-id="f8388-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f8388-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8388-132">-Datei</span><span class="sxs-lookup"><span data-stu-id="f8388-132">-File</span></span>
<span data-ttu-id="f8388-133">Gibt den vollständigen Pfad der JSON-Datei (JavaScript Object Notation) an, die die Beschreibung des verknüpften Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="f8388-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8388-134">-Force</span><span class="sxs-lookup"><span data-stu-id="f8388-134">-Force</span></span>
<span data-ttu-id="f8388-135">Gibt an, dass dieses Cmdlet einen vorhandenen verknüpften Dienst ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f8388-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f8388-136">-Name</span><span class="sxs-lookup"><span data-stu-id="f8388-136">-Name</span></span>
<span data-ttu-id="f8388-137">Gibt den Namen des verknüpften Diensts an, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="f8388-137">Specifies the name of the linked service to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8388-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8388-138">-ResourceGroupName</span></span>
<span data-ttu-id="f8388-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f8388-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f8388-140">Mit diesem Cmdlet wird ein verknüpfter Dienst für die von diesem Parameter festgelegte Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="f8388-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8388-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8388-141">-Confirm</span></span>
<span data-ttu-id="f8388-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8388-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8388-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8388-143">-WhatIf</span></span>
<span data-ttu-id="f8388-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8388-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8388-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8388-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8388-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8388-146">CommonParameters</span></span>
<span data-ttu-id="f8388-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8388-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8388-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8388-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8388-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8388-149">INPUTS</span></span>

### <span data-ttu-id="f8388-150">Keine</span><span class="sxs-lookup"><span data-stu-id="f8388-150">None</span></span>
<span data-ttu-id="f8388-151">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f8388-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8388-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8388-152">OUTPUTS</span></span>

### <span data-ttu-id="f8388-153">Microsoft. WindowsAzure. Commands. Utilities. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="f8388-153">Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService</span></span>

## <span data-ttu-id="f8388-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8388-154">NOTES</span></span>
* <span data-ttu-id="f8388-155">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="f8388-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f8388-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8388-156">RELATED LINKS</span></span>

[<span data-ttu-id="f8388-157">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="f8388-157">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="f8388-158">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="f8388-158">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)


