---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847580"
---
# <span data-ttu-id="fce98-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="fce98-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="fce98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fce98-102">SYNOPSIS</span></span>
<span data-ttu-id="fce98-103">Aktiviert die Überwachung in einem HDInsight-Cluster, und relevante Protokolle werden an den während der Aktivierung angegebenen Überwachungs Arbeitsbereich gesendet.</span><span class="sxs-lookup"><span data-stu-id="fce98-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="fce98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fce98-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fce98-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fce98-105">DESCRIPTION</span></span>
<span data-ttu-id="fce98-106">Das Cmdlet **enable-AzHDInsightMonitoring** ermöglicht die Überwachung in einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="fce98-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="fce98-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fce98-107">EXAMPLES</span></span>

### <span data-ttu-id="fce98-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fce98-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="fce98-109">Die Überwachung wird im HDInsight-Cluster aktiviert, und relevante Protokolle werden mit ID 1d364e89-bb71-4503-aa3d-a23535aea7bd an den Arbeitsbereich "Überwachung" gesendet.</span><span class="sxs-lookup"><span data-stu-id="fce98-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="fce98-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fce98-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="fce98-111">Die Überwachung wird im HDInsight-Cluster aktiviert, und relevante Protokolle werden mit ID 1d364e89-bb71-4503-aa3d-a23535aea7bd an den Arbeitsbereich "Überwachung" gesendet.</span><span class="sxs-lookup"><span data-stu-id="fce98-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="fce98-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fce98-112">PARAMETERS</span></span>

### <span data-ttu-id="fce98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce98-113">-DefaultProfile</span></span>
<span data-ttu-id="fce98-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fce98-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fce98-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fce98-115">-Name</span></span>
<span data-ttu-id="fce98-116">Der Name des Clusters, in dem die Überwachung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fce98-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="fce98-117">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="fce98-117">-PrimaryKey</span></span>
<span data-ttu-id="fce98-118">Der Primärschlüssel des Überwachungs Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="fce98-118">The primary key of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fce98-119">-ResourceGroupName</span></span>
<span data-ttu-id="fce98-120">Die Ressourcengruppe des Clusters.</span><span class="sxs-lookup"><span data-stu-id="fce98-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="fce98-121">-Arbeitsbereichs-Nr</span><span class="sxs-lookup"><span data-stu-id="fce98-121">-WorkspaceId</span></span>
<span data-ttu-id="fce98-122">Die ID des Überwachungs Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="fce98-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="fce98-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fce98-123">-Confirm</span></span>
<span data-ttu-id="fce98-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fce98-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fce98-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fce98-125">-WhatIf</span></span>
<span data-ttu-id="fce98-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fce98-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fce98-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fce98-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fce98-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce98-128">CommonParameters</span></span>
<span data-ttu-id="fce98-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fce98-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce98-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fce98-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce98-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fce98-131">INPUTS</span></span>

### <span data-ttu-id="fce98-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fce98-132">System.String</span></span>

## <span data-ttu-id="fce98-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fce98-133">OUTPUTS</span></span>

### <span data-ttu-id="fce98-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fce98-134">System.Boolean</span></span>

## <span data-ttu-id="fce98-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fce98-135">NOTES</span></span>

## <span data-ttu-id="fce98-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fce98-136">RELATED LINKS</span></span>
