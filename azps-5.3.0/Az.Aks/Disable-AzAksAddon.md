---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471570"
---
# <span data-ttu-id="b98d2-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="b98d2-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="b98d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b98d2-102">SYNOPSIS</span></span>
<span data-ttu-id="b98d2-103">Deaktivieren Sie die Add-Ons für aks.</span><span class="sxs-lookup"><span data-stu-id="b98d2-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="b98d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b98d2-104">SYNTAX</span></span>

### <span data-ttu-id="b98d2-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b98d2-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b98d2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b98d2-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b98d2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b98d2-107">DESCRIPTION</span></span>
<span data-ttu-id="b98d2-108">Deaktivieren Sie die Add-Ons für aks.</span><span class="sxs-lookup"><span data-stu-id="b98d2-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="b98d2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b98d2-109">EXAMPLES</span></span>

### <span data-ttu-id="b98d2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b98d2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="b98d2-111">Deaktivieren Sie die `HttpApplicationRouting` Add-Ons `Monitoring` , und `AzurePolicy` für `VirtualNode` `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="b98d2-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="b98d2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b98d2-112">PARAMETERS</span></span>

### <span data-ttu-id="b98d2-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b98d2-113">-ClusterName</span></span>
<span data-ttu-id="b98d2-114">Verwalteter Clustername in Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b98d2-114">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b98d2-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="b98d2-115">-ClusterObject</span></span>
<span data-ttu-id="b98d2-116">Ein PSAkiernetesCluster-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b98d2-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b98d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b98d2-117">-DefaultProfile</span></span>
<span data-ttu-id="b98d2-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b98d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b98d2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b98d2-119">-Name</span></span>
<span data-ttu-id="b98d2-120">Verwalteter Clustername in Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b98d2-120">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b98d2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b98d2-121">-ResourceGroupName</span></span>
<span data-ttu-id="b98d2-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b98d2-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b98d2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b98d2-123">-Confirm</span></span>
<span data-ttu-id="b98d2-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b98d2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b98d2-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b98d2-125">-WhatIf</span></span>
<span data-ttu-id="b98d2-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b98d2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b98d2-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b98d2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b98d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b98d2-128">CommonParameters</span></span>
<span data-ttu-id="b98d2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b98d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b98d2-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b98d2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b98d2-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b98d2-131">INPUTS</span></span>

### <span data-ttu-id="b98d2-132">Microsoft.Azure.Commands.Aks.Models.PSAkiernetesCluster</span><span class="sxs-lookup"><span data-stu-id="b98d2-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="b98d2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b98d2-133">System.String</span></span>

## <span data-ttu-id="b98d2-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b98d2-134">OUTPUTS</span></span>

### <span data-ttu-id="b98d2-135">Microsoft.Azure.Commands.Aks.Models.PSAkiernetesCluster</span><span class="sxs-lookup"><span data-stu-id="b98d2-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="b98d2-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b98d2-136">NOTES</span></span>

## <span data-ttu-id="b98d2-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b98d2-137">RELATED LINKS</span></span>
