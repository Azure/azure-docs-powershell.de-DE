---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458143"
---
# <span data-ttu-id="815be-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="815be-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="815be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="815be-102">SYNOPSIS</span></span>
<span data-ttu-id="815be-103">API zum Registrieren eines neuen K8s-Cluster und damit zum Erstellen einer nachverfolgten Ressource in ARM</span><span class="sxs-lookup"><span data-stu-id="815be-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="815be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="815be-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="815be-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="815be-105">DESCRIPTION</span></span>
<span data-ttu-id="815be-106">API zum Registrieren eines neuen K8s-Cluster und damit zum Erstellen einer nachverfolgten Ressource in ARM</span><span class="sxs-lookup"><span data-stu-id="815be-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="815be-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="815be-107">EXAMPLES</span></span>

### <span data-ttu-id="815be-108">Beispiel 1: Erstellen eines verbundenen Kubernets</span><span class="sxs-lookup"><span data-stu-id="815be-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="815be-109">Mit diesem Befehl werden verbundene Kubernets erstellt.</span><span class="sxs-lookup"><span data-stu-id="815be-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="815be-110">Beispiel 1: Erstellen eines verbundenen Kubernets mit den Parametern "kubeConfig" und "kubeContext"</span><span class="sxs-lookup"><span data-stu-id="815be-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="815be-111">Mit diesem Befehl werden verbundene Kubernets mit den Parametern "kubeConfig" und "kubeContext" erstellt.</span><span class="sxs-lookup"><span data-stu-id="815be-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="815be-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="815be-112">PARAMETERS</span></span>

### <span data-ttu-id="815be-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="815be-113">-ClusterName</span></span>
<span data-ttu-id="815be-114">Der Name des Kubernetes-Cluster, für den "get" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="815be-114">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815be-115">-DefaultProfile</span></span>
<span data-ttu-id="815be-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="815be-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815be-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="815be-117">-KubeConfig</span></span>
<span data-ttu-id="815be-118">Pfad zur Konfigurationsdatei "kube"</span><span class="sxs-lookup"><span data-stu-id="815be-118">Path to the kube config file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815be-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="815be-119">-KubeContext</span></span>
<span data-ttu-id="815be-120">Kontext "Kubconfig" vom aktuellen Computer</span><span class="sxs-lookup"><span data-stu-id="815be-120">Kubconfig context from current machine</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815be-121">-Location</span><span class="sxs-lookup"><span data-stu-id="815be-121">-Location</span></span>
<span data-ttu-id="815be-122">Position des Clusters</span><span class="sxs-lookup"><span data-stu-id="815be-122">Location of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815be-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="815be-123">-ResourceGroupName</span></span>
<span data-ttu-id="815be-124">Der Name der Ressourcengruppe, für die der Kubernetes-Cluster registriert ist.</span><span class="sxs-lookup"><span data-stu-id="815be-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815be-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="815be-125">-SubscriptionId</span></span>
<span data-ttu-id="815be-126">Die ID des Abonnements, für das der Kubernetes-Cluster registriert ist.</span><span class="sxs-lookup"><span data-stu-id="815be-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815be-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="815be-127">-Confirm</span></span>
<span data-ttu-id="815be-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="815be-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="815be-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="815be-129">-WhatIf</span></span>
<span data-ttu-id="815be-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="815be-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="815be-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="815be-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="815be-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815be-132">CommonParameters</span></span>
<span data-ttu-id="815be-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="815be-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815be-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="815be-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815be-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="815be-135">INPUTS</span></span>

## <span data-ttu-id="815be-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="815be-136">OUTPUTS</span></span>

### <span data-ttu-id="815be-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedConnecternetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="815be-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="815be-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="815be-138">NOTES</span></span>

<span data-ttu-id="815be-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="815be-139">ALIASES</span></span>

## <span data-ttu-id="815be-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="815be-140">RELATED LINKS</span></span>

