---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847584"
---
# <span data-ttu-id="570f6-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="570f6-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="570f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="570f6-102">SYNOPSIS</span></span>
<span data-ttu-id="570f6-103">Deaktiviert die Überwachung in einem HDInsight-Cluster, und relevante Protokolle werden nicht mehr in den während der Aktivierung angegebenen Überwachungs Arbeitsbereich überfließen.</span><span class="sxs-lookup"><span data-stu-id="570f6-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="570f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="570f6-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="570f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="570f6-105">DESCRIPTION</span></span>
<span data-ttu-id="570f6-106">Das Cmdlet **Disable-AzHDInsightMonitoring** deaktiviert die Überwachung in einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="570f6-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="570f6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="570f6-107">EXAMPLES</span></span>

### <span data-ttu-id="570f6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="570f6-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="570f6-109">Die Überwachung wird im HDInsight-Cluster deaktiviert, und relevante Protokolle werden nicht mehr in den Arbeitsbereich "Überwachung" fließen.</span><span class="sxs-lookup"><span data-stu-id="570f6-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="570f6-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="570f6-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="570f6-111">Die Überwachung wird im HDInsight-Cluster deaktiviert, und relevante Protokolle werden nicht mehr in den Arbeitsbereich "Überwachung" fließen.</span><span class="sxs-lookup"><span data-stu-id="570f6-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="570f6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="570f6-112">PARAMETERS</span></span>

### <span data-ttu-id="570f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="570f6-113">-DefaultProfile</span></span>
<span data-ttu-id="570f6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="570f6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="570f6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="570f6-115">-Name</span></span>
<span data-ttu-id="570f6-116">Der Name des Clusters, um die Überwachung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="570f6-116">The name of the cluster to disable Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="570f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="570f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="570f6-118">Die Ressourcengruppe des Clusters.</span><span class="sxs-lookup"><span data-stu-id="570f6-118">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="570f6-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="570f6-119">-Confirm</span></span>
<span data-ttu-id="570f6-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="570f6-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570f6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="570f6-121">-WhatIf</span></span>
<span data-ttu-id="570f6-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="570f6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="570f6-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="570f6-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="570f6-124">CommonParameters</span></span>
<span data-ttu-id="570f6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="570f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="570f6-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="570f6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="570f6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="570f6-127">INPUTS</span></span>

### <span data-ttu-id="570f6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="570f6-128">System.String</span></span>

## <span data-ttu-id="570f6-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="570f6-129">OUTPUTS</span></span>

### <span data-ttu-id="570f6-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="570f6-130">System.Boolean</span></span>

## <span data-ttu-id="570f6-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="570f6-131">NOTES</span></span>

## <span data-ttu-id="570f6-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="570f6-132">RELATED LINKS</span></span>
