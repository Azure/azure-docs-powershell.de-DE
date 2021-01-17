---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469147"
---
# <span data-ttu-id="72d56-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="72d56-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="72d56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72d56-102">SYNOPSIS</span></span>
<span data-ttu-id="72d56-103">Aktivieren Sie die Add-Ons für aks.</span><span class="sxs-lookup"><span data-stu-id="72d56-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="72d56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72d56-104">SYNTAX</span></span>

### <span data-ttu-id="72d56-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="72d56-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72d56-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72d56-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72d56-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72d56-107">DESCRIPTION</span></span>
<span data-ttu-id="72d56-108">Aktivieren Sie die Add-Ons für aks.</span><span class="sxs-lookup"><span data-stu-id="72d56-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="72d56-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72d56-109">EXAMPLES</span></span>

### <span data-ttu-id="72d56-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72d56-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="72d56-111">Aktivieren Sie die `HttpApplicationRouting` Add-Ons `Monitoring` , und `AzurePolicy` für `VirtualNode` `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="72d56-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="72d56-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72d56-112">PARAMETERS</span></span>

### <span data-ttu-id="72d56-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="72d56-113">-ClusterName</span></span>
<span data-ttu-id="72d56-114">Verwalteter Clustername in Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="72d56-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="72d56-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="72d56-115">-ClusterObject</span></span>
<span data-ttu-id="72d56-116">Ein PSAkiernetesCluster-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="72d56-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="72d56-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d56-117">-DefaultProfile</span></span>
<span data-ttu-id="72d56-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72d56-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72d56-119">-Name</span><span class="sxs-lookup"><span data-stu-id="72d56-119">-Name</span></span>
<span data-ttu-id="72d56-120">Verwalteter Clustername in Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="72d56-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="72d56-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72d56-121">-ResourceGroupName</span></span>
<span data-ttu-id="72d56-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="72d56-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="72d56-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="72d56-123">-SubnetName</span></span>
<span data-ttu-id="72d56-124">Subnetzname von VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="72d56-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="72d56-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="72d56-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="72d56-126">Ressourcen-ID des Arbeitsbereichs für Überwachung.</span><span class="sxs-lookup"><span data-stu-id="72d56-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="72d56-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72d56-127">-Confirm</span></span>
<span data-ttu-id="72d56-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72d56-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72d56-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="72d56-129">-WhatIf</span></span>
<span data-ttu-id="72d56-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72d56-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72d56-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72d56-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72d56-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d56-132">CommonParameters</span></span>
<span data-ttu-id="72d56-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72d56-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d56-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72d56-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d56-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72d56-135">INPUTS</span></span>

### <span data-ttu-id="72d56-136">System.String</span><span class="sxs-lookup"><span data-stu-id="72d56-136">System.String</span></span>

### <span data-ttu-id="72d56-137">Microsoft.Azure.Commands.Aks.Models.PSAkiernetesCluster</span><span class="sxs-lookup"><span data-stu-id="72d56-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="72d56-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72d56-138">OUTPUTS</span></span>

### <span data-ttu-id="72d56-139">Microsoft.Azure.Commands.Aks.Models.PSAkiernetesCluster</span><span class="sxs-lookup"><span data-stu-id="72d56-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="72d56-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="72d56-140">NOTES</span></span>

## <span data-ttu-id="72d56-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="72d56-141">RELATED LINKS</span></span>
