---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
ms.openlocfilehash: 5e3ee9de0adf511407013ef346a2867cb43fb11c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504989"
---
# <span data-ttu-id="ef857-101">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="ef857-101">Get-AzureRmHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="ef857-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef857-102">SYNOPSIS</span></span>
<span data-ttu-id="ef857-103">Ruft den Skript Aktionsverlauf für einen Cluster ab und listet ihn in umgekehrter chronologischer Reihenfolge auf oder ruft Details einer zuvor ausgeführten Skript Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="ef857-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef857-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef857-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef857-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef857-105">DESCRIPTION</span></span>
<span data-ttu-id="ef857-106">Das Cmdlet " **Get-AzureRmHDInsightScriptActionHistory** " Ruft den Skript Aktionsverlauf für einen Azure HDInsight-Cluster ab und listet ihn in umgekehrter chronologischer Reihenfolge auf oder ruft Details einer zuvor ausgeführten Skript Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="ef857-106">The **Get-AzureRmHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="ef857-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef857-107">EXAMPLES</span></span>

### <span data-ttu-id="ef857-108">Beispiel 1: Abrufen des Verlaufs der Ausführung von Skriptaktionen für einen Cluster</span><span class="sxs-lookup"><span data-stu-id="ef857-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="ef857-109">Dieser Befehl ruft das Protokoll der Skriptaktionen für den Cluster your-Hadoop-001 ab.</span><span class="sxs-lookup"><span data-stu-id="ef857-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="ef857-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef857-110">PARAMETERS</span></span>

### <span data-ttu-id="ef857-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ef857-111">-ClusterName</span></span>
<span data-ttu-id="ef857-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="ef857-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ef857-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef857-113">-ResourceGroupName</span></span>
<span data-ttu-id="ef857-114">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ef857-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ef857-115">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="ef857-115">-ScriptExecutionId</span></span>
<span data-ttu-id="ef857-116">Gibt die Ausführungs-ID der ausgeführten Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="ef857-116">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef857-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef857-117">-DefaultProfile</span></span>
<span data-ttu-id="ef857-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef857-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef857-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef857-119">CommonParameters</span></span>
<span data-ttu-id="ef857-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef857-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef857-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef857-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef857-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef857-122">INPUTS</span></span>

## <span data-ttu-id="ef857-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef857-123">OUTPUTS</span></span>

### <span data-ttu-id="ef857-124">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionDetail]</span><span class="sxs-lookup"><span data-stu-id="ef857-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail]</span></span>

## <span data-ttu-id="ef857-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef857-125">NOTES</span></span>

## <span data-ttu-id="ef857-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef857-126">RELATED LINKS</span></span>

