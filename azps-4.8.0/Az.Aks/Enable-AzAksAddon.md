---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173624"
---
# <span data-ttu-id="ffbb3-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="ffbb3-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="ffbb3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ffbb3-102">SYNOPSIS</span></span>
<span data-ttu-id="ffbb3-103">Aktivieren Sie die Addons für AKS.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="ffbb3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffbb3-104">SYNTAX</span></span>

### <span data-ttu-id="ffbb3-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ffbb3-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ffbb3-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffbb3-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffbb3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffbb3-107">DESCRIPTION</span></span>
<span data-ttu-id="ffbb3-108">Aktivieren Sie die Addons für AKS.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="ffbb3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ffbb3-109">EXAMPLES</span></span>

### <span data-ttu-id="ffbb3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ffbb3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="ffbb3-111">Aktivieren Sie die Addons `HttpApplicationRouting` ,, `Monitoring` `AzurePolicy` `VirtualNode` und `KubeDashboard` für AKS.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="ffbb3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffbb3-112">PARAMETERS</span></span>

### <span data-ttu-id="ffbb3-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ffbb3-113">-ClusterName</span></span>
<span data-ttu-id="ffbb3-114">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="ffbb3-115">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="ffbb3-115">-ClusterObject</span></span>
<span data-ttu-id="ffbb3-116">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ffbb3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffbb3-117">-DefaultProfile</span></span>
<span data-ttu-id="ffbb3-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffbb3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ffbb3-119">-Name</span></span>
<span data-ttu-id="ffbb3-120">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="ffbb3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffbb3-121">-ResourceGroupName</span></span>
<span data-ttu-id="ffbb3-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="ffbb3-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ffbb3-123">-SubnetName</span></span>
<span data-ttu-id="ffbb3-124">Subnet-Name von VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="ffbb3-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="ffbb3-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="ffbb3-126">Die Ressourcen-ID des Arbeitsbereichs der Überwachung.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="ffbb3-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ffbb3-127">-Confirm</span></span>
<span data-ttu-id="ffbb3-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffbb3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffbb3-129">-WhatIf</span></span>
<span data-ttu-id="ffbb3-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffbb3-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffbb3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffbb3-132">CommonParameters</span></span>
<span data-ttu-id="ffbb3-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffbb3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffbb3-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffbb3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffbb3-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ffbb3-135">INPUTS</span></span>

### <span data-ttu-id="ffbb3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ffbb3-136">System.String</span></span>

### <span data-ttu-id="ffbb3-137">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ffbb3-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ffbb3-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ffbb3-138">OUTPUTS</span></span>

### <span data-ttu-id="ffbb3-139">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ffbb3-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ffbb3-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="ffbb3-140">NOTES</span></span>

## <span data-ttu-id="ffbb3-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ffbb3-141">RELATED LINKS</span></span>
