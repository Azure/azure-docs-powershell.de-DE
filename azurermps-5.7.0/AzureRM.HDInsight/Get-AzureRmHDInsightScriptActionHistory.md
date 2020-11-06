---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
ms.openlocfilehash: b2e302f9490cb5671728a46105ad574b54270c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476773"
---
# <span data-ttu-id="2c61a-101">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="2c61a-101">Get-AzureRmHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="2c61a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c61a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c61a-103">Ruft den Skript Aktionsverlauf für einen Cluster ab und listet ihn in umgekehrter chronologischer Reihenfolge auf oder ruft Details einer zuvor ausgeführten Skript Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="2c61a-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c61a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c61a-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c61a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c61a-105">DESCRIPTION</span></span>
<span data-ttu-id="2c61a-106">Das Cmdlet " **Get-AzureRmHDInsightScriptActionHistory** " Ruft den Skript Aktionsverlauf für einen Azure HDInsight-Cluster ab und listet ihn in umgekehrter chronologischer Reihenfolge auf oder ruft Details einer zuvor ausgeführten Skript Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="2c61a-106">The **Get-AzureRmHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="2c61a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c61a-107">EXAMPLES</span></span>

### <span data-ttu-id="2c61a-108">Beispiel 1: Abrufen des Verlaufs der Ausführung von Skriptaktionen für einen Cluster</span><span class="sxs-lookup"><span data-stu-id="2c61a-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="2c61a-109">Dieser Befehl ruft das Protokoll der Skriptaktionen für den Cluster your-Hadoop-001 ab.</span><span class="sxs-lookup"><span data-stu-id="2c61a-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="2c61a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c61a-110">PARAMETERS</span></span>

### <span data-ttu-id="2c61a-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="2c61a-111">-ClusterName</span></span>
<span data-ttu-id="2c61a-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2c61a-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c61a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c61a-113">-DefaultProfile</span></span>
<span data-ttu-id="2c61a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2c61a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c61a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c61a-115">-ResourceGroupName</span></span>
<span data-ttu-id="2c61a-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2c61a-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c61a-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="2c61a-117">-ScriptExecutionId</span></span>
<span data-ttu-id="2c61a-118">Gibt die Ausführungs-ID der ausgeführten Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="2c61a-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c61a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c61a-119">CommonParameters</span></span>
<span data-ttu-id="2c61a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c61a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c61a-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c61a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c61a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c61a-122">INPUTS</span></span>

### <span data-ttu-id="2c61a-123">Keine</span><span class="sxs-lookup"><span data-stu-id="2c61a-123">None</span></span>
<span data-ttu-id="2c61a-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2c61a-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2c61a-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c61a-125">OUTPUTS</span></span>

### <span data-ttu-id="2c61a-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionDetail]</span><span class="sxs-lookup"><span data-stu-id="2c61a-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail]</span></span>

## <span data-ttu-id="2c61a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c61a-127">NOTES</span></span>

## <span data-ttu-id="2c61a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c61a-128">RELATED LINKS</span></span>

