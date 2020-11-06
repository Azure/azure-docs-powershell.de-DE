---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/disable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: f701d0c5e0ea2d8f4ce5ded850d131c6c066e9ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496158"
---
# <span data-ttu-id="46afc-101">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="46afc-101">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="46afc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46afc-102">SYNOPSIS</span></span>
<span data-ttu-id="46afc-103">Deaktiviert die Operations Management Suite (OMS) in einem HDInsight-Cluster, und relevante Protokolle werden nicht mehr in den OMS-Arbeitsbereich fließen, der während der Aktivierung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="46afc-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46afc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46afc-104">SYNTAX</span></span>

```
Disable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46afc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46afc-105">DESCRIPTION</span></span>
<span data-ttu-id="46afc-106">Das Cmdlet **Disable-AzureRmHDInsightOperationsManagementSuite** deaktiviert Operations Management Suite (OMS) in einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="46afc-106">The **Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="46afc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46afc-107">EXAMPLES</span></span>

### <span data-ttu-id="46afc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46afc-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="46afc-109">Die Operations Management Suite (OMS) wird im HDInsight-Cluster deaktiviert, und relevante Protokolle werden nicht mehr in den OMS-Arbeitsbereich weiter fließen.</span><span class="sxs-lookup"><span data-stu-id="46afc-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="46afc-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="46afc-110">Example 2</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="46afc-111">Die Operations Management Suite (OMS) wird im HDInsight-Cluster deaktiviert, und relevante Protokolle werden nicht mehr in den OMS-Arbeitsbereich weiter fließen.</span><span class="sxs-lookup"><span data-stu-id="46afc-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="46afc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="46afc-112">PARAMETERS</span></span>

### <span data-ttu-id="46afc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46afc-113">-DefaultProfile</span></span>
<span data-ttu-id="46afc-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="46afc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46afc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="46afc-115">-Name</span></span>
<span data-ttu-id="46afc-116">Der Name des Clusters, in dem die Operations Management Suite (OMS) deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="46afc-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="46afc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46afc-117">-ResourceGroupName</span></span>
<span data-ttu-id="46afc-118">Die Ressourcengruppe des Clusters.</span><span class="sxs-lookup"><span data-stu-id="46afc-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="46afc-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46afc-119">-Confirm</span></span>
<span data-ttu-id="46afc-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46afc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46afc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46afc-121">-WhatIf</span></span>
<span data-ttu-id="46afc-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46afc-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46afc-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46afc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46afc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46afc-124">CommonParameters</span></span>
<span data-ttu-id="46afc-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46afc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46afc-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46afc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46afc-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46afc-127">INPUTS</span></span>

### <span data-ttu-id="46afc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="46afc-128">System.String</span></span>

## <span data-ttu-id="46afc-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46afc-129">OUTPUTS</span></span>

### <span data-ttu-id="46afc-130">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="46afc-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="46afc-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="46afc-131">NOTES</span></span>

## <span data-ttu-id="46afc-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46afc-132">RELATED LINKS</span></span>
