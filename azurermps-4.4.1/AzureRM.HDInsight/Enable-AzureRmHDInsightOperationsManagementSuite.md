---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fcaa5c1342801c4c0ef00e1a4c48abf4a6b4da41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663324"
---
# <span data-ttu-id="3d6f2-101">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="3d6f2-101">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="3d6f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6f2-103">Aktiviert die Operations Management Suite (OMS) in einem HDInsight-Cluster, und relevante Protokolle werden an den OMS-Arbeitsbereich gesendet, der während der Aktivierung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d6f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d6f2-104">SYNTAX</span></span>

```
Enable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String>
 [-PrimaryKey] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d6f2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d6f2-105">DESCRIPTION</span></span>
<span data-ttu-id="3d6f2-106">Das Cmdlet **enable-AzureRmHDInsightOperationsManagementSuite** aktiviert die Operations Management Suite (OMS) in einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-106">The **Enable-AzureRmHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="3d6f2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d6f2-107">EXAMPLES</span></span>

### <span data-ttu-id="3d6f2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d6f2-108">Example 1</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="3d6f2-109">Die Operations Management Suite (OMS) wird im HDInsight-Cluster aktiviert, und relevante Protokolle werden mit ID 1d364e89-bb71-4503-aa3d-a23535aea7bd an den OMS-Arbeitsbereich gesendet.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="3d6f2-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3d6f2-110">Example 2</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="3d6f2-111">Die Operations Management Suite (OMS) wird im HDInsight-Cluster aktiviert, und relevante Protokolle werden mit ID 1d364e89-bb71-4503-aa3d-a23535aea7bd an den OMS-Arbeitsbereich gesendet.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="3d6f2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d6f2-112">PARAMETERS</span></span>

### <span data-ttu-id="3d6f2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3d6f2-113">-Name</span></span>
<span data-ttu-id="3d6f2-114">Der Name des Clusters, in dem die Operations Management Suite (OMS) aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-114">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6f2-115">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="3d6f2-115">-PrimaryKey</span></span>
<span data-ttu-id="3d6f2-116">Der Primärschlüssel des Arbeitsbereichs Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="3d6f2-116">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="3d6f2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d6f2-117">-ResourceGroupName</span></span>
<span data-ttu-id="3d6f2-118">Die Ressourcengruppe des Clusters.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="3d6f2-119">-Arbeitsbereichs-Nr</span><span class="sxs-lookup"><span data-stu-id="3d6f2-119">-WorkspaceId</span></span>
<span data-ttu-id="3d6f2-120">Die ID des OMS-Arbeitsbereichs (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="3d6f2-120">The id of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="3d6f2-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d6f2-121">-Confirm</span></span>
<span data-ttu-id="3d6f2-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d6f2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6f2-123">-DefaultProfile</span></span>
<span data-ttu-id="3d6f2-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d6f2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d6f2-125">-WhatIf</span></span>
<span data-ttu-id="3d6f2-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d6f2-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d6f2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6f2-128">CommonParameters</span></span>
<span data-ttu-id="3d6f2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6f2-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d6f2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6f2-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d6f2-131">INPUTS</span></span>

### <span data-ttu-id="3d6f2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3d6f2-132">System.String</span></span>

## <span data-ttu-id="3d6f2-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d6f2-133">OUTPUTS</span></span>

### <span data-ttu-id="3d6f2-134">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="3d6f2-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="3d6f2-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d6f2-135">NOTES</span></span>

## <span data-ttu-id="3d6f2-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d6f2-136">RELATED LINKS</span></span>

