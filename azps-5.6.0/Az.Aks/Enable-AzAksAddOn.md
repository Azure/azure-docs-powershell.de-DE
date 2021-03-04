---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
ms.openlocfilehash: 1280f65659f986d0fd8402da0d3db5b1c5a92b58
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926091"
---
# <span data-ttu-id="7d18a-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="7d18a-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="7d18a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d18a-102">SYNOPSIS</span></span>
<span data-ttu-id="7d18a-103">Aktivieren Sie die Addons für aks.</span><span class="sxs-lookup"><span data-stu-id="7d18a-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="7d18a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d18a-104">SYNTAX</span></span>

### <span data-ttu-id="7d18a-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d18a-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d18a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d18a-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d18a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d18a-107">DESCRIPTION</span></span>
<span data-ttu-id="7d18a-108">Aktivieren Sie die Addons für aks.</span><span class="sxs-lookup"><span data-stu-id="7d18a-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="7d18a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7d18a-109">EXAMPLES</span></span>

### <span data-ttu-id="7d18a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7d18a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="7d18a-111">Aktivieren Sie die Addons `HttpApplicationRouting` , , und für `Monitoring` `AzurePolicy` `VirtualNode` `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="7d18a-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="7d18a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7d18a-112">PARAMETERS</span></span>

### <span data-ttu-id="7d18a-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7d18a-113">-ClusterName</span></span>
<span data-ttu-id="7d18a-114">Verwalteter Clustername von Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7d18a-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="7d18a-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="7d18a-115">-ClusterObject</span></span>
<span data-ttu-id="7d18a-116">Ein PSKubernetesCluster-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7d18a-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="7d18a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d18a-117">-DefaultProfile</span></span>
<span data-ttu-id="7d18a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d18a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d18a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7d18a-119">-Name</span></span>
<span data-ttu-id="7d18a-120">Verwalteter Clustername von Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7d18a-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="7d18a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d18a-121">-ResourceGroupName</span></span>
<span data-ttu-id="7d18a-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="7d18a-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="7d18a-123">-Subnetzname</span><span class="sxs-lookup"><span data-stu-id="7d18a-123">-SubnetName</span></span>
<span data-ttu-id="7d18a-124">Subnetzname von VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="7d18a-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="7d18a-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="7d18a-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="7d18a-126">Ressourcen-ID des Arbeitsbereichs der Überwachung.</span><span class="sxs-lookup"><span data-stu-id="7d18a-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="7d18a-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7d18a-127">-Confirm</span></span>
<span data-ttu-id="7d18a-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d18a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d18a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d18a-129">-WhatIf</span></span>
<span data-ttu-id="7d18a-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d18a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d18a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d18a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d18a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d18a-132">CommonParameters</span></span>
<span data-ttu-id="7d18a-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d18a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d18a-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d18a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d18a-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7d18a-135">INPUTS</span></span>

### <span data-ttu-id="7d18a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7d18a-136">System.String</span></span>

### <span data-ttu-id="7d18a-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="7d18a-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="7d18a-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7d18a-138">OUTPUTS</span></span>

### <span data-ttu-id="7d18a-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="7d18a-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="7d18a-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7d18a-140">NOTES</span></span>

## <span data-ttu-id="7d18a-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7d18a-141">RELATED LINKS</span></span>
