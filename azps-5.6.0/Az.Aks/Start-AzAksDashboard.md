---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 5202f4c86d1d83d6e337c61ee6fc0f72a2b031de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942747"
---
# <span data-ttu-id="7b1de-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="7b1de-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="7b1de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b1de-102">SYNOPSIS</span></span>
<span data-ttu-id="7b1de-103">Erstellen Sie einen Kubectl-SSH-Tunnel zum Dashboard des verwalteten Clusters.</span><span class="sxs-lookup"><span data-stu-id="7b1de-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="7b1de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b1de-104">SYNTAX</span></span>

### <span data-ttu-id="7b1de-105">GroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7b1de-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b1de-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b1de-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b1de-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b1de-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b1de-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b1de-108">DESCRIPTION</span></span>
<span data-ttu-id="7b1de-109">Erstellen Sie einen Kubectl-SSH-Tunnel zum Dashboard des verwalteten Clusters.</span><span class="sxs-lookup"><span data-stu-id="7b1de-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="7b1de-110">Der SSH-Tunnel wird in einem PowerShell-Auftrag namens Kubectl-Tunnel eingerichtet und kann durch Ausführen von gefunden `Get-Job` werden.</span><span class="sxs-lookup"><span data-stu-id="7b1de-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="7b1de-111">Der Tunnel sollte über zugänglich [http://127.0.0.1:8001](http://127.0.0.1:8001) sein.</span><span class="sxs-lookup"><span data-stu-id="7b1de-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="7b1de-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7b1de-112">EXAMPLES</span></span>

### <span data-ttu-id="7b1de-113">Starten eines SSH-Tunnels und Öffnen eines Browsers für das Kubernetes-Dashboard</span><span class="sxs-lookup"><span data-stu-id="7b1de-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="7b1de-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7b1de-114">PARAMETERS</span></span>

### <span data-ttu-id="7b1de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b1de-115">-DefaultProfile</span></span>
<span data-ttu-id="7b1de-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b1de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b1de-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="7b1de-117">-DisableBrowser</span></span>
<span data-ttu-id="7b1de-118">Öffnen Sie nach dem Einrichten des kubectl-Port-Forwards keinen Browser.</span><span class="sxs-lookup"><span data-stu-id="7b1de-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b1de-119">-ID</span><span class="sxs-lookup"><span data-stu-id="7b1de-119">-Id</span></span>
<span data-ttu-id="7b1de-120">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="7b1de-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b1de-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b1de-121">-InputObject</span></span>
<span data-ttu-id="7b1de-122">Ein PSKubernetesCluster-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7b1de-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b1de-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="7b1de-123">-ListenPort</span></span>
<span data-ttu-id="7b1de-124">Der Wiedergabeport für das Dashboard.</span><span class="sxs-lookup"><span data-stu-id="7b1de-124">The listening port for the dashboard.</span></span> <span data-ttu-id="7b1de-125">Der Standardwert ist 8003.</span><span class="sxs-lookup"><span data-stu-id="7b1de-125">Default value is 8003.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b1de-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7b1de-126">-Name</span></span>
<span data-ttu-id="7b1de-127">Name Des verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="7b1de-127">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b1de-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b1de-128">-PassThru</span></span>
<span data-ttu-id="7b1de-129">Cmdlet gibt den KubeTunnelJob zurück, wenn übergeben.</span><span class="sxs-lookup"><span data-stu-id="7b1de-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b1de-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b1de-130">-ResourceGroupName</span></span>
<span data-ttu-id="7b1de-131">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="7b1de-131">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b1de-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b1de-132">CommonParameters</span></span>
<span data-ttu-id="7b1de-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b1de-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b1de-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b1de-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b1de-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7b1de-135">INPUTS</span></span>

### <span data-ttu-id="7b1de-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="7b1de-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="7b1de-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7b1de-137">System.String</span></span>

## <span data-ttu-id="7b1de-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7b1de-138">OUTPUTS</span></span>

### <span data-ttu-id="7b1de-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="7b1de-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="7b1de-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7b1de-140">NOTES</span></span>

## <span data-ttu-id="7b1de-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7b1de-141">RELATED LINKS</span></span>
