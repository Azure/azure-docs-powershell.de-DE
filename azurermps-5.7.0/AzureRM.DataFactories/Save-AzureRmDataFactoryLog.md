---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/save-azurermdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
ms.openlocfilehash: 696e2de560b67db78f24dea7e8512d85c3640902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478541"
---
# <span data-ttu-id="31cdc-101">Save-AzureRmDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="31cdc-101">Save-AzureRmDataFactoryLog</span></span>

## <span data-ttu-id="31cdc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="31cdc-103">Downloadet Protokolldateien aus Azure HDInsight processing.</span><span class="sxs-lookup"><span data-stu-id="31cdc-103">Downloads log files from Azure HDInsight processing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31cdc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31cdc-104">SYNTAX</span></span>

### <span data-ttu-id="31cdc-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="31cdc-105">ByFactoryName (Default)</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31cdc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="31cdc-106">ByFactoryObject</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31cdc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31cdc-107">DESCRIPTION</span></span>
<span data-ttu-id="31cdc-108">Das Cmdlet **Save-AzureRmDataFactoryLog** downloadet Protokolldateien, die der Azure HDInsight-Verarbeitung von Pig-oder Hive-Projekten zugeordnet sind, oder für benutzerdefinierte Aktivitäten auf der lokalen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="31cdc-108">The **Save-AzureRmDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="31cdc-109">Sie führen zunächst das Get-AzureRmDataFactoryRun-Cmdlet aus, um eine ID für eine Aktivitätsausführung für einen Datenslice abzurufen, und verwenden Sie dann diese ID, um Protokolldateien aus dem BLOB-Speicher (Binary Large Object) abzurufen, der dem HDInsight-Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="31cdc-109">You first run the Get-AzureRmDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>

<span data-ttu-id="31cdc-110">Wenn Sie den *DownloadLogs* -Parameter nicht angeben, gibt das Cmdlet nur den Speicherort der Protokolldateien zurück.</span><span class="sxs-lookup"><span data-stu-id="31cdc-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>

<span data-ttu-id="31cdc-111">Wenn Sie *DownloadLogs* angeben, ohne ein Ausgabeverzeichnis ( *Ausgabe* Parameter) anzugeben, werden die Protokolldateien in den Standardordner "Dokumente" heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="31cdc-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>

<span data-ttu-id="31cdc-112">Wenn Sie *DownloadLogs* zusammen mit einem Ausgabeordner ( *Output* ) angeben, werden die Protokolldateien in den angegebenen Ordner heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="31cdc-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="31cdc-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31cdc-113">EXAMPLES</span></span>

### <span data-ttu-id="31cdc-114">Beispiel 1: Speichern von Protokolldateien in einem bestimmten Ordner</span><span class="sxs-lookup"><span data-stu-id="31cdc-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="31cdc-115">Dieser Befehl speichert Protokolldateien für die Aktivität, die mit der ID von 841b77c9-d56c-48d1-99a3-8c16c3e77d39 ausgeführt wird, wobei die Aktivität zu einer Pipeline in der Data Factory mit dem Namen LogProcessingFactory in der Ressourcengruppe "ADF" gehört.</span><span class="sxs-lookup"><span data-stu-id="31cdc-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="31cdc-116">Die Protokolldateien werden im Ordner C:\test gespeichert.</span><span class="sxs-lookup"><span data-stu-id="31cdc-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="31cdc-117">Beispiel 2: Speichern von Protokolldateien im Standardordner "Dokumente"</span><span class="sxs-lookup"><span data-stu-id="31cdc-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="31cdc-118">Dieser Befehl speichert Protokolldateien in Ordner "Dokumente" (Standard).</span><span class="sxs-lookup"><span data-stu-id="31cdc-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="31cdc-119">Beispiel 3: Abrufen des Speicherorts von Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="31cdc-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="31cdc-120">Dieser Befehl gibt den Speicherort der Protokolldateien zurück.</span><span class="sxs-lookup"><span data-stu-id="31cdc-120">This command returns the location of log files.</span></span>
<span data-ttu-id="31cdc-121">Beachten Sie, dass *DownloadLogs* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="31cdc-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="31cdc-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="31cdc-122">PARAMETERS</span></span>

### <span data-ttu-id="31cdc-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="31cdc-123">-DataFactory</span></span>
<span data-ttu-id="31cdc-124">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="31cdc-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="31cdc-125">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="31cdc-125">-DataFactoryName</span></span>
<span data-ttu-id="31cdc-126">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="31cdc-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="31cdc-127">Dieses Cmdlet downloadet Protokolldateien für die Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="31cdc-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="31cdc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31cdc-128">-DefaultProfile</span></span>
<span data-ttu-id="31cdc-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="31cdc-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31cdc-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="31cdc-130">-DownloadLogs</span></span>
<span data-ttu-id="31cdc-131">Gibt an, dass das Cmdlet Protokolldateien auf Ihren lokalen Computer herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="31cdc-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="31cdc-132">Wenn der Ordner *Ouptut* nicht angegeben ist, werden die Dateien im Ordner Dokumente unter einem Unterordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="31cdc-132">If *Ouptut* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="31cdc-133">-ID</span><span class="sxs-lookup"><span data-stu-id="31cdc-133">-Id</span></span>
<span data-ttu-id="31cdc-134">Gibt die ID der Aktivitätsausführung für den Datenslice an.</span><span class="sxs-lookup"><span data-stu-id="31cdc-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="31cdc-135">Verwenden Sie das Get-AzureRmDataFactoryRun-Cmdlet, um eine ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="31cdc-135">Use the Get-AzureRmDataFactoryRun cmdlet to get an ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31cdc-136">-Output</span><span class="sxs-lookup"><span data-stu-id="31cdc-136">-Output</span></span>
<span data-ttu-id="31cdc-137">Gibt den Ausgabeordner an, in dem die heruntergeladenen Protokolldateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="31cdc-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31cdc-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31cdc-138">-ResourceGroupName</span></span>
<span data-ttu-id="31cdc-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="31cdc-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="31cdc-140">Mit diesem Cmdlet wird eine Data Factory erstellt, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="31cdc-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="31cdc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31cdc-141">CommonParameters</span></span>
<span data-ttu-id="31cdc-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31cdc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31cdc-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31cdc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31cdc-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31cdc-144">INPUTS</span></span>

### <span data-ttu-id="31cdc-145">Keine</span><span class="sxs-lookup"><span data-stu-id="31cdc-145">None</span></span>
<span data-ttu-id="31cdc-146">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="31cdc-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31cdc-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31cdc-147">OUTPUTS</span></span>

### <span data-ttu-id="31cdc-148">Microsoft. Azure. Commands. datafactoring. Models. PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="31cdc-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="31cdc-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="31cdc-149">NOTES</span></span>
* <span data-ttu-id="31cdc-150">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="31cdc-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="31cdc-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31cdc-151">RELATED LINKS</span></span>

[<span data-ttu-id="31cdc-152">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="31cdc-152">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="31cdc-153">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="31cdc-153">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="31cdc-154">Neu – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="31cdc-154">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="31cdc-155">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="31cdc-155">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="31cdc-156">Satz-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="31cdc-156">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="31cdc-157">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="31cdc-157">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


