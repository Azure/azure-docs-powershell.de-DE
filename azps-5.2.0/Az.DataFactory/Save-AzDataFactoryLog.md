---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365685"
---
# <span data-ttu-id="0db8b-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="0db8b-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="0db8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0db8b-102">SYNOPSIS</span></span>
<span data-ttu-id="0db8b-103">Lädt Protokolldateien aus Azure HDInsight Processing herunter.</span><span class="sxs-lookup"><span data-stu-id="0db8b-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="0db8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0db8b-104">SYNTAX</span></span>

### <span data-ttu-id="0db8b-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0db8b-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0db8b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0db8b-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0db8b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0db8b-107">DESCRIPTION</span></span>
<span data-ttu-id="0db8b-108">Das **Cmdlet "Save-AzDataFactoryLog"** lädt Protokolldateien herunter, die mit der Azure -HDInsight-Verarbeitung von Schwein- oder Strukturprojekten oder für benutzerdefinierte Aktivitäten auf Ihrer lokalen Festplatte verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="0db8b-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="0db8b-109">Zuerst führen Sie das Cmdlet Get-AzDataFactoryRun aus, um eine ID für eine Aktivität abzurufen, die für ein Datendatenschnitt ausgeführt wird, und verwenden sie dann zum Abrufen von Protokolldateien aus dem BLOB (Binary Large Object)-Speicher, der dem Cluster "HDInsight" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0db8b-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="0db8b-110">Wenn Sie den Parameter *"DownloadLogs" nicht* angeben, gibt das Cmdlet einfach den Speicherort der Protokolldateien zurück.</span><span class="sxs-lookup"><span data-stu-id="0db8b-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="0db8b-111">Wenn Sie *"DownloadLogs"* angeben, ohne ein Ausgabeverzeichnis *(Ausgabeparameter)* anzugeben, werden die Protokolldateien in den Standardordner "Dokumente" heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="0db8b-111">If you specify *DownloadLogs* without specifying an output directory (*Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="0db8b-112">Wenn Sie *DownloadLogs* zusammen mit einem Ausgabeordner *(Ausgabe)* angeben, werden die Protokolldateien in den angegebenen Ordner heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="0db8b-112">If you specify *DownloadLogs* along with an output folder (*Output*), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="0db8b-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0db8b-113">EXAMPLES</span></span>

### <span data-ttu-id="0db8b-114">Beispiel 1: Speichern von Protokolldateien in einem bestimmten Ordner</span><span class="sxs-lookup"><span data-stu-id="0db8b-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="0db8b-115">Dieser Befehl speichert Protokolldateien für die Aktivität, die mit der ID 841b77c9-d56c-48d1-99a3-8c16c3e77d39 ausgeführt wird, wobei die Aktivität zu einer Pipeline in der Datenfactory mit dem Namen "LogProcessingFactory" in der Ressourcengruppe mit dem Namen ADF gehört.</span><span class="sxs-lookup"><span data-stu-id="0db8b-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="0db8b-116">Die Protokolldateien werden im Ordner "C:\Test" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0db8b-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="0db8b-117">Beispiel 2: Speichern von Protokolldateien im Standardordner "Dokumente"</span><span class="sxs-lookup"><span data-stu-id="0db8b-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="0db8b-118">Dieser Befehl speichert Protokolldateien im Ordner "Dokumente" (Standard).</span><span class="sxs-lookup"><span data-stu-id="0db8b-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="0db8b-119">Beispiel 3: Herunterladen des Speicherorts von Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="0db8b-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="0db8b-120">Dieser Befehl gibt den Speicherort der Protokolldateien zurück.</span><span class="sxs-lookup"><span data-stu-id="0db8b-120">This command returns the location of log files.</span></span>
<span data-ttu-id="0db8b-121">Beachten Sie, *dass "DownloadLogs"* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0db8b-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="0db8b-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0db8b-122">PARAMETERS</span></span>

### <span data-ttu-id="0db8b-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0db8b-123">-DataFactory</span></span>
<span data-ttu-id="0db8b-124">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="0db8b-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="0db8b-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0db8b-125">-DataFactoryName</span></span>
<span data-ttu-id="0db8b-126">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="0db8b-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0db8b-127">Dieses Cmdlet lädt Protokolldateien für die Daten factory herunter, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0db8b-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0db8b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db8b-128">-DefaultProfile</span></span>
<span data-ttu-id="0db8b-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0db8b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0db8b-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="0db8b-130">-DownloadLogs</span></span>
<span data-ttu-id="0db8b-131">Gibt an, dass dieses Cmdlet Protokolldateien auf Ihren lokalen Computer herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="0db8b-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="0db8b-132">Wenn *der* Ordner "Ausgabe" nicht angegeben ist, werden Dateien im Ordner "Dokumente" unter einem Unterordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0db8b-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="0db8b-133">-ID</span><span class="sxs-lookup"><span data-stu-id="0db8b-133">-Id</span></span>
<span data-ttu-id="0db8b-134">Gibt die ID der Aktivität an, die für das Datenschnitt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0db8b-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="0db8b-135">Verwenden Sie das Get-AzDataFactoryRun Cmdlet, um eine ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0db8b-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="0db8b-136">-Output</span><span class="sxs-lookup"><span data-stu-id="0db8b-136">-Output</span></span>
<span data-ttu-id="0db8b-137">Gibt den Ausgabeordner an, in dem die heruntergeladenen Protokolldateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0db8b-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="0db8b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db8b-138">-ResourceGroupName</span></span>
<span data-ttu-id="0db8b-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0db8b-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0db8b-140">Dieses Cmdlet erstellt eine Daten factory, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0db8b-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0db8b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db8b-141">CommonParameters</span></span>
<span data-ttu-id="0db8b-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db8b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db8b-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db8b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db8b-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0db8b-144">INPUTS</span></span>

### <span data-ttu-id="0db8b-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0db8b-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="0db8b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="0db8b-146">System.String</span></span>

## <span data-ttu-id="0db8b-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0db8b-147">OUTPUTS</span></span>

### <span data-ttu-id="0db8b-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="0db8b-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="0db8b-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0db8b-149">NOTES</span></span>
* <span data-ttu-id="0db8b-150">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="0db8b-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0db8b-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0db8b-151">RELATED LINKS</span></span>

[<span data-ttu-id="0db8b-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="0db8b-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="0db8b-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0db8b-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="0db8b-154">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0db8b-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="0db8b-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0db8b-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="0db8b-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="0db8b-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="0db8b-157">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0db8b-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


