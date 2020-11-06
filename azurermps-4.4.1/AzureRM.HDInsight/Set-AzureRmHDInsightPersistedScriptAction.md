---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 28c608711e222ce85d4ea959caa6c4afe7bafaaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504966"
---
# <span data-ttu-id="ec975-101">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ec975-101">Set-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="ec975-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec975-102">SYNOPSIS</span></span>
<span data-ttu-id="ec975-103">Legt eine zuvor ausgeführte Skript Aktion als permanente Skript Aktion fest.</span><span class="sxs-lookup"><span data-stu-id="ec975-103">Sets a previously executed script action to be a persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec975-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec975-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec975-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec975-105">DESCRIPTION</span></span>
<span data-ttu-id="ec975-106">Das Cmdlet " **Set-AzureRmHDInsightPersistedScriptAction** " legt eine zuvor ausgeführte Skript Aktion als permanente Skript Aktion fest.</span><span class="sxs-lookup"><span data-stu-id="ec975-106">The **Set-AzureRmHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="ec975-107">Die angegebene Skript Aktion muss zuvor erfolgreich ausgeführt worden sein.</span><span class="sxs-lookup"><span data-stu-id="ec975-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="ec975-108">Die Skript Aktion wird jedes Mal ausgeführt, wenn der Azure HDInsight-Cluster skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="ec975-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="ec975-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec975-109">EXAMPLES</span></span>

### <span data-ttu-id="ec975-110">Beispiel 1: Einrichten einer zuvor erfolgreichen Skript Aktion, die beibehalten werden soll, oder Ausführen für die Cluster Skalierung nach oben</span><span class="sxs-lookup"><span data-stu-id="ec975-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="ec975-111">Mit diesem Befehl wird eine zuvor erfolgreiche Skript Aktion als permanente Skript Aktion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ec975-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="ec975-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec975-112">PARAMETERS</span></span>

### <span data-ttu-id="ec975-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ec975-113">-ClusterName</span></span>
<span data-ttu-id="ec975-114">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="ec975-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ec975-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec975-115">-ResourceGroupName</span></span>
<span data-ttu-id="ec975-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ec975-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ec975-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="ec975-117">-ScriptExecutionId</span></span>
<span data-ttu-id="ec975-118">Gibt die Ausführungs-ID der Skript Aktion an, die auf PERSISTED heraufgestuft werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec975-118">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="ec975-119">Diese Skript Aktion muss erfolgreich ausgeführt werden, damit Sie höher gestuft werden kann.</span><span class="sxs-lookup"><span data-stu-id="ec975-119">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="ec975-120">Sie finden die Ausführungs-ID der Skript Aktion mithilfe von Get-AzureRmHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="ec975-120">You can find the script action execution ID using Get-AzureRmHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="ec975-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec975-121">-DefaultProfile</span></span>
<span data-ttu-id="ec975-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec975-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec975-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec975-123">CommonParameters</span></span>
<span data-ttu-id="ec975-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec975-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec975-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec975-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec975-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec975-126">INPUTS</span></span>

## <span data-ttu-id="ec975-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec975-127">OUTPUTS</span></span>

### <span data-ttu-id="ec975-128">System. void</span><span class="sxs-lookup"><span data-stu-id="ec975-128">System.Void</span></span>

## <span data-ttu-id="ec975-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec975-129">NOTES</span></span>

## <span data-ttu-id="ec975-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec975-130">RELATED LINKS</span></span>

[<span data-ttu-id="ec975-131">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ec975-131">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="ec975-132">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ec975-132">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)


