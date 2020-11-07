---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: a437c27aaa5caea7ae0efb7ab477fe643a5c80a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819935"
---
# <span data-ttu-id="53c4b-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="53c4b-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="53c4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="53c4b-103">Ruft die beibehaltenen Skriptaktionen für einen Cluster ab und listet sie in chronologischer Reihenfolge auf oder ruft Details für eine angegebene permanente Skript Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="53c4b-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="53c4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53c4b-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53c4b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53c4b-105">DESCRIPTION</span></span>
<span data-ttu-id="53c4b-106">Das Cmdlet " **Get-AzHDInsightPersistedScriptAction** " Ruft die beibehaltenen Skriptaktionen für einen Azure HDInsight-Cluster ab und listet sie in chronologischer Reihenfolge auf oder ruft Details für eine angegebene permanente Skript Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="53c4b-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="53c4b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53c4b-107">EXAMPLES</span></span>

### <span data-ttu-id="53c4b-108">Beispiel 1: Abrufen der beibehaltenen Skriptaktionen in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="53c4b-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="53c4b-109">Dieser Befehl ruft permanente Skriptaktionen auf dem Cluster mit dem Namen "Your-Hadoop-001" ab.</span><span class="sxs-lookup"><span data-stu-id="53c4b-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="53c4b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="53c4b-110">PARAMETERS</span></span>

### <span data-ttu-id="53c4b-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="53c4b-111">-ClusterName</span></span>
<span data-ttu-id="53c4b-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="53c4b-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="53c4b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c4b-113">-DefaultProfile</span></span>
<span data-ttu-id="53c4b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="53c4b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53c4b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="53c4b-115">-Name</span></span>
<span data-ttu-id="53c4b-116">Gibt den Namen der beibehaltenen Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="53c4b-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c4b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53c4b-117">-ResourceGroupName</span></span>
<span data-ttu-id="53c4b-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="53c4b-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="53c4b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c4b-119">CommonParameters</span></span>
<span data-ttu-id="53c4b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c4b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c4b-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53c4b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c4b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53c4b-122">INPUTS</span></span>

### <span data-ttu-id="53c4b-123">Keine</span><span class="sxs-lookup"><span data-stu-id="53c4b-123">None</span></span>

## <span data-ttu-id="53c4b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53c4b-124">OUTPUTS</span></span>

### <span data-ttu-id="53c4b-125">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="53c4b-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="53c4b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="53c4b-126">NOTES</span></span>

## <span data-ttu-id="53c4b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53c4b-127">RELATED LINKS</span></span>

[<span data-ttu-id="53c4b-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="53c4b-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="53c4b-129">Satz-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="53c4b-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


