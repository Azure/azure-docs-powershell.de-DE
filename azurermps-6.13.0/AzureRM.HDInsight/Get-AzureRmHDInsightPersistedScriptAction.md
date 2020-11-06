---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 6305e9a312eb5ebb34de56bcef8a8894b1bd7dd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496141"
---
# <span data-ttu-id="4204d-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="4204d-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="4204d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4204d-102">SYNOPSIS</span></span>
<span data-ttu-id="4204d-103">Ruft die beibehaltenen Skriptaktionen für einen Cluster ab und listet sie in chronologischer Reihenfolge auf oder ruft Details für eine angegebene permanente Skript Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="4204d-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4204d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4204d-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4204d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4204d-105">DESCRIPTION</span></span>
<span data-ttu-id="4204d-106">Das Cmdlet " **Get-AzureRmHDInsightPersistedScriptAction** " Ruft die beibehaltenen Skriptaktionen für einen Azure HDInsight-Cluster ab und listet sie in chronologischer Reihenfolge auf oder ruft Details für eine angegebene permanente Skript Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="4204d-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="4204d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4204d-107">EXAMPLES</span></span>

### <span data-ttu-id="4204d-108">Beispiel 1: Abrufen der beibehaltenen Skriptaktionen in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="4204d-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="4204d-109">Dieser Befehl ruft permanente Skriptaktionen auf dem Cluster mit dem Namen "Your-Hadoop-001" ab.</span><span class="sxs-lookup"><span data-stu-id="4204d-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4204d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4204d-110">PARAMETERS</span></span>

### <span data-ttu-id="4204d-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="4204d-111">-ClusterName</span></span>
<span data-ttu-id="4204d-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="4204d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4204d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4204d-113">-DefaultProfile</span></span>
<span data-ttu-id="4204d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4204d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4204d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4204d-115">-Name</span></span>
<span data-ttu-id="4204d-116">Gibt den Namen der beibehaltenen Skript Aktion an.</span><span class="sxs-lookup"><span data-stu-id="4204d-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="4204d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4204d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4204d-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4204d-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4204d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4204d-119">CommonParameters</span></span>
<span data-ttu-id="4204d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4204d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4204d-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4204d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4204d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4204d-122">INPUTS</span></span>

### <span data-ttu-id="4204d-123">Keine</span><span class="sxs-lookup"><span data-stu-id="4204d-123">None</span></span>

## <span data-ttu-id="4204d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4204d-124">OUTPUTS</span></span>

### <span data-ttu-id="4204d-125">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="4204d-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="4204d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="4204d-126">NOTES</span></span>

## <span data-ttu-id="4204d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4204d-127">RELATED LINKS</span></span>

[<span data-ttu-id="4204d-128">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="4204d-128">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="4204d-129">Satz-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="4204d-129">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


