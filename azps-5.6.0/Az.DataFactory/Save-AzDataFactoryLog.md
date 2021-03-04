---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: eb2e3c9acd93e8b20c7bdf6f4ee04ef2910a3cbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946199"
---
# <span data-ttu-id="4811f-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="4811f-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="4811f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4811f-102">SYNOPSIS</span></span>
<span data-ttu-id="4811f-103">Lädt Protokolldateien aus der Azure HDInsight-Verarbeitung herunter.</span><span class="sxs-lookup"><span data-stu-id="4811f-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="4811f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4811f-104">SYNTAX</span></span>

### <span data-ttu-id="4811f-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4811f-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4811f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4811f-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4811f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4811f-107">DESCRIPTION</span></span>
<span data-ttu-id="4811f-108">Das **Cmdlet Save-AzDataFactoryLog** lädt Protokolldateien zur Azure HDInsight-Verarbeitung von Projekten mit Schwein oder Hive oder für benutzerdefinierte Aktivitäten auf Ihre lokale Festplatte herunter.</span><span class="sxs-lookup"><span data-stu-id="4811f-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="4811f-109">Sie führen zuerst das Get-AzDataFactoryRun-Cmdlet aus, um eine ID für eine Aktivität abzurufen, die für ein Datendatenschnitt ausgeführt wird, und verwenden sie dann zum Abrufen von Protokolldateien aus dem binary large object (BLOB)-Speicher, der dem HDInsight-Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4811f-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="4811f-110">Wenn Sie den Parameter *DownloadLogs* nicht angeben, gibt das Cmdlet einfach den Speicherort der Protokolldateien zurück.</span><span class="sxs-lookup"><span data-stu-id="4811f-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="4811f-111">Wenn Sie *DownloadLogs ohne* Angabe eines Ausgabeverzeichnisses (Ausgabeparameter) angeben, werden die Protokolldateien in den Standardordner Dokumente heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="4811f-111">If you specify *DownloadLogs* without specifying an output directory (*Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="4811f-112">Wenn Sie *DownloadLogs* zusammen mit einem Ausgabeordner *(Ausgabe)* angeben, werden die Protokolldateien in den angegebenen Ordner heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="4811f-112">If you specify *DownloadLogs* along with an output folder (*Output*), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="4811f-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4811f-113">EXAMPLES</span></span>

### <span data-ttu-id="4811f-114">Beispiel 1: Speichern von Protokolldateien in einem bestimmten Ordner</span><span class="sxs-lookup"><span data-stu-id="4811f-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="4811f-115">Mit diesem Befehl werden Protokolldateien für die Aktivität gespeichert, die mit der ID 841b77c9-d56c-48d1-99a3-8c16c3e77d39 ausgeführt werden, in der die Aktivität zu einer Pipeline in der Daten factory mit dem Namen LogProcessingFactory in der Ressourcengruppe adF gehört.</span><span class="sxs-lookup"><span data-stu-id="4811f-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="4811f-116">Die Protokolldateien werden im Ordner "C:\Test" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4811f-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="4811f-117">Beispiel 2: Speichern von Protokolldateien im Standardordner "Dokumente"</span><span class="sxs-lookup"><span data-stu-id="4811f-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="4811f-118">Mit diesem Befehl werden Protokolldateien im Ordner Dokumente gespeichert (Standard).</span><span class="sxs-lookup"><span data-stu-id="4811f-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="4811f-119">Beispiel 3: Herunterladen des Speicherorts von Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="4811f-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="4811f-120">Dieser Befehl gibt den Speicherort der Protokolldateien zurück.</span><span class="sxs-lookup"><span data-stu-id="4811f-120">This command returns the location of log files.</span></span>
<span data-ttu-id="4811f-121">Beachten Sie, *dass DownloadLogs* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4811f-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="4811f-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4811f-122">PARAMETERS</span></span>

### <span data-ttu-id="4811f-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4811f-123">-DataFactory</span></span>
<span data-ttu-id="4811f-124">Gibt ein **PSDataFactory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="4811f-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="4811f-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4811f-125">-DataFactoryName</span></span>
<span data-ttu-id="4811f-126">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="4811f-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4811f-127">Dieses Cmdlet lädt Protokolldateien für die Daten factory herunter, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4811f-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4811f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4811f-128">-DefaultProfile</span></span>
<span data-ttu-id="4811f-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4811f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4811f-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="4811f-130">-DownloadLogs</span></span>
<span data-ttu-id="4811f-131">Gibt an, dass dieses Cmdlet Protokolldateien auf Ihren lokalen Computer herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="4811f-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="4811f-132">Wenn *kein* Ausgabeordner angegeben ist, werden Dateien im Ordner Dokumente unter einem Unterordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4811f-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="4811f-133">-ID</span><span class="sxs-lookup"><span data-stu-id="4811f-133">-Id</span></span>
<span data-ttu-id="4811f-134">Gibt die ID der Aktivität an, die für das Datendatenschnitt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4811f-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="4811f-135">Verwenden Sie Get-AzDataFactoryRun cmdlet, um eine ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4811f-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4811f-136">-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="4811f-136">-Output</span></span>
<span data-ttu-id="4811f-137">Gibt den Ausgabeordner an, in dem die heruntergeladenen Protokolldateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4811f-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4811f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4811f-138">-ResourceGroupName</span></span>
<span data-ttu-id="4811f-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4811f-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4811f-140">Dieses Cmdlet erstellt eine Daten factory, die zu der Gruppe gehört, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4811f-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4811f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4811f-141">CommonParameters</span></span>
<span data-ttu-id="4811f-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4811f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4811f-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4811f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4811f-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4811f-144">INPUTS</span></span>

### <span data-ttu-id="4811f-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4811f-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="4811f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4811f-146">System.String</span></span>

## <span data-ttu-id="4811f-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4811f-147">OUTPUTS</span></span>

### <span data-ttu-id="4811f-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="4811f-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="4811f-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4811f-149">NOTES</span></span>
* <span data-ttu-id="4811f-150">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="4811f-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4811f-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4811f-151">RELATED LINKS</span></span>

[<span data-ttu-id="4811f-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="4811f-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="4811f-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4811f-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="4811f-154">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4811f-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="4811f-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4811f-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="4811f-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="4811f-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="4811f-157">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4811f-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


