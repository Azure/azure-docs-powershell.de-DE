---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: 976f00f62cfda991e7d1aff349a0b04807dbbe1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651685"
---
# <span data-ttu-id="3f27a-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="3f27a-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="3f27a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f27a-102">SYNOPSIS</span></span>
<span data-ttu-id="3f27a-103">Downloadet Protokolldateien aus Azure HDInsight processing.</span><span class="sxs-lookup"><span data-stu-id="3f27a-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="3f27a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f27a-104">SYNTAX</span></span>

### <span data-ttu-id="3f27a-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f27a-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f27a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3f27a-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f27a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f27a-107">DESCRIPTION</span></span>
<span data-ttu-id="3f27a-108">Das Cmdlet **Save-AzDataFactoryLog** downloadet Protokolldateien, die der Azure HDInsight-Verarbeitung von Pig-oder Hive-Projekten zugeordnet sind, oder für benutzerdefinierte Aktivitäten auf der lokalen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="3f27a-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="3f27a-109">Sie führen zunächst das Get-AzDataFactoryRun-Cmdlet aus, um eine ID für eine Aktivitätsausführung für einen Datenslice abzurufen, und verwenden Sie dann diese ID, um Protokolldateien aus dem BLOB-Speicher (Binary Large Object) abzurufen, der dem HDInsight-Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3f27a-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="3f27a-110">Wenn Sie den *DownloadLogs* -Parameter nicht angeben, gibt das Cmdlet nur den Speicherort der Protokolldateien zurück.</span><span class="sxs-lookup"><span data-stu-id="3f27a-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="3f27a-111">Wenn Sie *DownloadLogs* angeben, ohne ein Ausgabeverzeichnis ( *Ausgabe* Parameter) anzugeben, werden die Protokolldateien in den Standardordner "Dokumente" heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="3f27a-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="3f27a-112">Wenn Sie *DownloadLogs* zusammen mit einem Ausgabeordner ( *Output* ) angeben, werden die Protokolldateien in den angegebenen Ordner heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="3f27a-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="3f27a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f27a-113">EXAMPLES</span></span>

### <span data-ttu-id="3f27a-114">Beispiel 1: Speichern von Protokolldateien in einem bestimmten Ordner</span><span class="sxs-lookup"><span data-stu-id="3f27a-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="3f27a-115">Dieser Befehl speichert Protokolldateien für die Aktivität, die mit der ID von 841b77c9-d56c-48d1-99a3-8c16c3e77d39 ausgeführt wird, wobei die Aktivität zu einer Pipeline in der Data Factory mit dem Namen LogProcessingFactory in der Ressourcengruppe "ADF" gehört.</span><span class="sxs-lookup"><span data-stu-id="3f27a-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="3f27a-116">Die Protokolldateien werden im Ordner C:\test gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3f27a-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="3f27a-117">Beispiel 2: Speichern von Protokolldateien im Standardordner "Dokumente"</span><span class="sxs-lookup"><span data-stu-id="3f27a-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="3f27a-118">Dieser Befehl speichert Protokolldateien in Ordner "Dokumente" (Standard).</span><span class="sxs-lookup"><span data-stu-id="3f27a-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="3f27a-119">Beispiel 3: Abrufen des Speicherorts von Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="3f27a-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="3f27a-120">Dieser Befehl gibt den Speicherort der Protokolldateien zurück.</span><span class="sxs-lookup"><span data-stu-id="3f27a-120">This command returns the location of log files.</span></span>
<span data-ttu-id="3f27a-121">Beachten Sie, dass *DownloadLogs* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3f27a-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="3f27a-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f27a-122">PARAMETERS</span></span>

### <span data-ttu-id="3f27a-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f27a-123">-DataFactory</span></span>
<span data-ttu-id="3f27a-124">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3f27a-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="3f27a-125">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3f27a-125">-DataFactoryName</span></span>
<span data-ttu-id="3f27a-126">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="3f27a-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3f27a-127">Dieses Cmdlet downloadet Protokolldateien für die Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3f27a-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f27a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f27a-128">-DefaultProfile</span></span>
<span data-ttu-id="3f27a-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3f27a-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f27a-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="3f27a-130">-DownloadLogs</span></span>
<span data-ttu-id="3f27a-131">Gibt an, dass das Cmdlet Protokolldateien auf Ihren lokalen Computer herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="3f27a-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="3f27a-132">Wenn der *Ausgabe* Ordner nicht angegeben ist, werden die Dateien im Ordner Dokumente unter einem Unterordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3f27a-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="3f27a-133">-ID</span><span class="sxs-lookup"><span data-stu-id="3f27a-133">-Id</span></span>
<span data-ttu-id="3f27a-134">Gibt die ID der Aktivitätsausführung für den Datenslice an.</span><span class="sxs-lookup"><span data-stu-id="3f27a-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="3f27a-135">Verwenden Sie das Get-AzDataFactoryRun-Cmdlet, um eine ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3f27a-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="3f27a-136">-Output</span><span class="sxs-lookup"><span data-stu-id="3f27a-136">-Output</span></span>
<span data-ttu-id="3f27a-137">Gibt den Ausgabeordner an, in dem die heruntergeladenen Protokolldateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3f27a-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="3f27a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f27a-138">-ResourceGroupName</span></span>
<span data-ttu-id="3f27a-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3f27a-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3f27a-140">Mit diesem Cmdlet wird eine Data Factory erstellt, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3f27a-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f27a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f27a-141">CommonParameters</span></span>
<span data-ttu-id="3f27a-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f27a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f27a-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f27a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f27a-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f27a-144">INPUTS</span></span>

### <span data-ttu-id="3f27a-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3f27a-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="3f27a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3f27a-146">System.String</span></span>

## <span data-ttu-id="3f27a-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f27a-147">OUTPUTS</span></span>

### <span data-ttu-id="3f27a-148">Microsoft. Azure. Commands. datafactoring. Models. PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="3f27a-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="3f27a-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f27a-149">NOTES</span></span>
* <span data-ttu-id="3f27a-150">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="3f27a-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3f27a-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f27a-151">RELATED LINKS</span></span>

[<span data-ttu-id="3f27a-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="3f27a-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="3f27a-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3f27a-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="3f27a-154">Neu – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3f27a-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="3f27a-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3f27a-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="3f27a-156">Satz-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="3f27a-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="3f27a-157">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3f27a-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


