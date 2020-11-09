---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300292"
---
# <span data-ttu-id="ebff6-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="ebff6-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="ebff6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ebff6-102">SYNOPSIS</span></span>
<span data-ttu-id="ebff6-103">Cluster löschen</span><span class="sxs-lookup"><span data-stu-id="ebff6-103">Delete cluster</span></span>

## <span data-ttu-id="ebff6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebff6-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebff6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebff6-105">DESCRIPTION</span></span>
<span data-ttu-id="ebff6-106">Cluster löschen, gilt nur für Cluster mit Bereitstellungsstatus "erfolgreich"</span><span class="sxs-lookup"><span data-stu-id="ebff6-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="ebff6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ebff6-107">EXAMPLES</span></span>

### <span data-ttu-id="ebff6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ebff6-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="ebff6-109">Cluster löschen</span><span class="sxs-lookup"><span data-stu-id="ebff6-109">Delete cluster</span></span>

## <span data-ttu-id="ebff6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebff6-110">PARAMETERS</span></span>

### <span data-ttu-id="ebff6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebff6-111">-AsJob</span></span>
<span data-ttu-id="ebff6-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ebff6-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebff6-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ebff6-113">-ClusterName</span></span>
<span data-ttu-id="ebff6-114">Der Clustername.</span><span class="sxs-lookup"><span data-stu-id="ebff6-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebff6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebff6-115">-DefaultProfile</span></span>
<span data-ttu-id="ebff6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ebff6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebff6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebff6-117">-ResourceGroupName</span></span>
<span data-ttu-id="ebff6-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ebff6-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebff6-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ebff6-119">-Confirm</span></span>
<span data-ttu-id="ebff6-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ebff6-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebff6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebff6-121">-WhatIf</span></span>
<span data-ttu-id="ebff6-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ebff6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebff6-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ebff6-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebff6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebff6-124">CommonParameters</span></span>
<span data-ttu-id="ebff6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebff6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebff6-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebff6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebff6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ebff6-127">INPUTS</span></span>

### <span data-ttu-id="ebff6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ebff6-128">System.String</span></span>

## <span data-ttu-id="ebff6-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ebff6-129">OUTPUTS</span></span>

### <span data-ttu-id="ebff6-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ebff6-130">System.Boolean</span></span>

## <span data-ttu-id="ebff6-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="ebff6-131">NOTES</span></span>

## <span data-ttu-id="ebff6-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ebff6-132">RELATED LINKS</span></span>
