---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: 94bd90b644b12723a36266dea34d9b5e9417b45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496145"
---
# <span data-ttu-id="b378b-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="b378b-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="b378b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b378b-102">SYNOPSIS</span></span>
<span data-ttu-id="b378b-103">Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem angegebenen Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b378b-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b378b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b378b-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b378b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b378b-105">DESCRIPTION</span></span>
<span data-ttu-id="b378b-106">Das Cmdlet " **Get-AzureRmHDInsightJobOutput** " Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem Azure HDInsight-Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b378b-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b378b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b378b-107">EXAMPLES</span></span>

### <span data-ttu-id="b378b-108">Beispiel 1: Abrufen der Protokollausgabe für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="b378b-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b378b-109">Dieser Befehl ruft die Protokollausgabe des Clusters mit dem Namen "Your-Hadoop-001" ab.</span><span class="sxs-lookup"><span data-stu-id="b378b-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b378b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b378b-110">PARAMETERS</span></span>

### <span data-ttu-id="b378b-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="b378b-111">-ClusterName</span></span>
<span data-ttu-id="b378b-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="b378b-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b378b-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="b378b-113">-DefaultContainer</span></span>
<span data-ttu-id="b378b-114">Gibt den Standardcontainernamen an.</span><span class="sxs-lookup"><span data-stu-id="b378b-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="b378b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b378b-115">-DefaultProfile</span></span>
<span data-ttu-id="b378b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b378b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b378b-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b378b-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="b378b-118">Gibt den standardmäßigen speicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="b378b-118">Specifies the default Storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b378b-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b378b-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="b378b-120">Gibt den Namen des Standardspeicher Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b378b-120">Specifies the default Storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b378b-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="b378b-121">-DisplayOutputType</span></span>
<span data-ttu-id="b378b-122">Gibt den Auftrags Ausgabetyp an, der angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="b378b-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="b378b-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b378b-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b378b-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="b378b-124">StandardOutput</span></span>
- <span data-ttu-id="b378b-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="b378b-125">StandardError</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Job.JobDisplayOutputType
Parameter Sets: (All)
Aliases:
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b378b-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="b378b-126">-HttpCredential</span></span>
<span data-ttu-id="b378b-127">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="b378b-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b378b-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="b378b-128">-JobId</span></span>
<span data-ttu-id="b378b-129">Gibt die Auftrags-ID des Auftrags an, dessen Ausgabe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b378b-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b378b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b378b-130">-ResourceGroupName</span></span>
<span data-ttu-id="b378b-131">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b378b-131">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b378b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b378b-132">CommonParameters</span></span>
<span data-ttu-id="b378b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b378b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b378b-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b378b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b378b-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b378b-135">INPUTS</span></span>

### <span data-ttu-id="b378b-136">Keine</span><span class="sxs-lookup"><span data-stu-id="b378b-136">None</span></span>

## <span data-ttu-id="b378b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b378b-137">OUTPUTS</span></span>

### <span data-ttu-id="b378b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b378b-138">System.String</span></span>

## <span data-ttu-id="b378b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="b378b-139">NOTES</span></span>

## <span data-ttu-id="b378b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b378b-140">RELATED LINKS</span></span>

[<span data-ttu-id="b378b-141">Neu – AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b378b-141">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="b378b-142">Anfang-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b378b-142">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


