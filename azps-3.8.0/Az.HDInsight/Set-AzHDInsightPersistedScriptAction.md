---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: bff21d969a88282f3ba3c1d79d1f717c3c169265
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846276"
---
# <span data-ttu-id="f5bf9-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="f5bf9-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="f5bf9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="f5bf9-103">Legt eine zuvor ausgeführte Skript Aktion als permanente Skript Aktion fest.</span><span class="sxs-lookup"><span data-stu-id="f5bf9-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="f5bf9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5bf9-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5bf9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="f5bf9-106">Das Cmdlet " **Set-AzHDInsightPersistedScriptAction** " legt eine zuvor ausgeführte Skript Aktion als permanente Skript Aktion fest.</span><span class="sxs-lookup"><span data-stu-id="f5bf9-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="f5bf9-107">Die angegebene Skript Aktion muss zuvor erfolgreich ausgeführt worden sein.</span><span class="sxs-lookup"><span data-stu-id="f5bf9-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="f5bf9-108">Die Skript Aktion wird jedes Mal ausgeführt, wenn der Azure HDInsight-Cluster skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="f5bf9-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="f5bf9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5bf9-109">EXAMPLES</span></span>

### <span data-ttu-id="f5bf9-110">Beispiel 1: Einrichten einer zuvor erfolgreichen Skript Aktion, die beibehalten werden soll, oder Ausführen für die Cluster Skalierung nach oben</span><span class="sxs-lookup"><span data-stu-id="f5bf9-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="f5bf9-111">Mit diesem Befehl wird eine zuvor erfolgreiche Skript Aktion als permanente Skript Aktion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f5bf9-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="f5bf9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5bf9-112">PARAMETERS</span></span>

### <span data-ttu-id="f5bf9-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f5bf9-113">-ClusterName</span></span>
<span data-ttu-id="f5bf9-114">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="f5bf9-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f5bf9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5bf9-115">-DefaultProfile</span></span>
<span data-ttu-id="f5bf9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f5bf9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5bf9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5bf9-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5bf9-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f5bf9-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f5bf9-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="f5bf9-119">-ScriptExecutionId</span></span>
<span data-ttu-id="f5bf9-120">Gibt die Ausführungs-ID der Skript Aktion an, die auf PERSISTED heraufgestuft werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5bf9-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="f5bf9-121">Diese Skript Aktion muss erfolgreich ausgeführt werden, damit Sie höher gestuft werden kann.</span><span class="sxs-lookup"><span data-stu-id="f5bf9-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="f5bf9-122">Sie finden die Ausführungs-ID der Skript Aktion mithilfe von Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="f5bf9-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5bf9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5bf9-123">CommonParameters</span></span>
<span data-ttu-id="f5bf9-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5bf9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5bf9-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5bf9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5bf9-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5bf9-126">INPUTS</span></span>

### <span data-ttu-id="f5bf9-127">Keine</span><span class="sxs-lookup"><span data-stu-id="f5bf9-127">None</span></span>

## <span data-ttu-id="f5bf9-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5bf9-128">OUTPUTS</span></span>

### <span data-ttu-id="f5bf9-129">System. void</span><span class="sxs-lookup"><span data-stu-id="f5bf9-129">System.Void</span></span>

## <span data-ttu-id="f5bf9-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5bf9-130">NOTES</span></span>

## <span data-ttu-id="f5bf9-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5bf9-131">RELATED LINKS</span></span>

[<span data-ttu-id="f5bf9-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="f5bf9-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="f5bf9-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="f5bf9-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


