---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: f593989125642d03a9dff1b48bbc7430498b2a36
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153108"
---
# <span data-ttu-id="d71d7-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="d71d7-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="d71d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d71d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d71d7-103">Legt eine zuvor ausgeführte Skriptaktion als aktion für beibehaltene Skripts fest.</span><span class="sxs-lookup"><span data-stu-id="d71d7-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="d71d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d71d7-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d71d7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d71d7-105">DESCRIPTION</span></span>
<span data-ttu-id="d71d7-106">Das **Cmdlet "Set-AzHDInsightPersistedScriptAction"** legt eine zuvor ausgeführte Skriptaktion als Persisted Script Action fest.</span><span class="sxs-lookup"><span data-stu-id="d71d7-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="d71d7-107">Die angegebene Skriptaktion muss zuvor erfolgreich gewesen sein.</span><span class="sxs-lookup"><span data-stu-id="d71d7-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="d71d7-108">Die Skriptaktion wird jedes Mal ausgeführt, wenn der Azure -HDInsight-Cluster skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="d71d7-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="d71d7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d71d7-109">EXAMPLES</span></span>

### <span data-ttu-id="d71d7-110">Beispiel 1: Festlegen einer zuvor erfolgreichen Skriptaktion, die beibehalten werden soll, oder Ausführen bei gruppierter Skalierung</span><span class="sxs-lookup"><span data-stu-id="d71d7-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="d71d7-111">Mit diesem Befehl wird eine zuvor erfolgreiche Skriptaktion als beibehaltene Skriptaktion definiert.</span><span class="sxs-lookup"><span data-stu-id="d71d7-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="d71d7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d71d7-112">PARAMETERS</span></span>

### <span data-ttu-id="d71d7-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d71d7-113">-ClusterName</span></span>
<span data-ttu-id="d71d7-114">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="d71d7-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d71d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d71d7-115">-DefaultProfile</span></span>
<span data-ttu-id="d71d7-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d71d7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d71d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d71d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="d71d7-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d71d7-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d71d7-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="d71d7-119">-ScriptExecutionId</span></span>
<span data-ttu-id="d71d7-120">Gibt die Ausführungs-ID der Skriptaktion an, die in die beibehaltene Skriptaktion zu promoten ist.</span><span class="sxs-lookup"><span data-stu-id="d71d7-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="d71d7-121">Diese Skriptaktion muss erfolgreich ausgeführt worden sein, um heraufgestuft zu werden.</span><span class="sxs-lookup"><span data-stu-id="d71d7-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="d71d7-122">Sie finden die Skriptausführungs-ID mithilfe von "Get-AzHDInsightScriptActionHistory".</span><span class="sxs-lookup"><span data-stu-id="d71d7-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="d71d7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d71d7-123">CommonParameters</span></span>
<span data-ttu-id="d71d7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d71d7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d71d7-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d71d7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d71d7-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d71d7-126">INPUTS</span></span>

### <span data-ttu-id="d71d7-127">Keine</span><span class="sxs-lookup"><span data-stu-id="d71d7-127">None</span></span>

## <span data-ttu-id="d71d7-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d71d7-128">OUTPUTS</span></span>

### <span data-ttu-id="d71d7-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="d71d7-129">System.Void</span></span>

## <span data-ttu-id="d71d7-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d71d7-130">NOTES</span></span>

## <span data-ttu-id="d71d7-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d71d7-131">RELATED LINKS</span></span>

[<span data-ttu-id="d71d7-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="d71d7-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="d71d7-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="d71d7-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


