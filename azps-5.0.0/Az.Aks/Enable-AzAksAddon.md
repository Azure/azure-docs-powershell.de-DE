---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178104"
---
# <span data-ttu-id="eebad-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="eebad-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="eebad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eebad-102">SYNOPSIS</span></span>
<span data-ttu-id="eebad-103">Aktivieren Sie die Addons für AKS.</span><span class="sxs-lookup"><span data-stu-id="eebad-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="eebad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eebad-104">SYNTAX</span></span>

### <span data-ttu-id="eebad-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="eebad-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eebad-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebad-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eebad-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eebad-107">DESCRIPTION</span></span>
<span data-ttu-id="eebad-108">Aktivieren Sie die Addons für AKS.</span><span class="sxs-lookup"><span data-stu-id="eebad-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="eebad-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eebad-109">EXAMPLES</span></span>

### <span data-ttu-id="eebad-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eebad-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="eebad-111">Aktivieren Sie die Addons `HttpApplicationRouting` ,, `Monitoring` `AzurePolicy` `VirtualNode` und `KubeDashboard` für AKS.</span><span class="sxs-lookup"><span data-stu-id="eebad-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="eebad-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eebad-112">PARAMETERS</span></span>

### <span data-ttu-id="eebad-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="eebad-113">-ClusterName</span></span>
<span data-ttu-id="eebad-114">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="eebad-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="eebad-115">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="eebad-115">-ClusterObject</span></span>
<span data-ttu-id="eebad-116">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="eebad-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="eebad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebad-117">-DefaultProfile</span></span>
<span data-ttu-id="eebad-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eebad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eebad-119">-Name</span><span class="sxs-lookup"><span data-stu-id="eebad-119">-Name</span></span>
<span data-ttu-id="eebad-120">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="eebad-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="eebad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eebad-121">-ResourceGroupName</span></span>
<span data-ttu-id="eebad-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eebad-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="eebad-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="eebad-123">-SubnetName</span></span>
<span data-ttu-id="eebad-124">Subnet-Name von VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="eebad-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="eebad-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="eebad-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="eebad-126">Die Ressourcen-ID des Arbeitsbereichs der Überwachung.</span><span class="sxs-lookup"><span data-stu-id="eebad-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="eebad-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eebad-127">-Confirm</span></span>
<span data-ttu-id="eebad-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eebad-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eebad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eebad-129">-WhatIf</span></span>
<span data-ttu-id="eebad-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eebad-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eebad-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eebad-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eebad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebad-132">CommonParameters</span></span>
<span data-ttu-id="eebad-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eebad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebad-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eebad-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebad-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eebad-135">INPUTS</span></span>

### <span data-ttu-id="eebad-136">System. String</span><span class="sxs-lookup"><span data-stu-id="eebad-136">System.String</span></span>

### <span data-ttu-id="eebad-137">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="eebad-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="eebad-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eebad-138">OUTPUTS</span></span>

### <span data-ttu-id="eebad-139">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="eebad-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="eebad-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="eebad-140">NOTES</span></span>

## <span data-ttu-id="eebad-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eebad-141">RELATED LINKS</span></span>
