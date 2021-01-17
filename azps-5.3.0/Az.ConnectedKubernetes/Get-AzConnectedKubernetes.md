---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472907"
---
# <span data-ttu-id="97b62-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="97b62-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="97b62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97b62-102">SYNOPSIS</span></span>
<span data-ttu-id="97b62-103">Gibt die Eigenschaften des angegebenen verbundenen Cluster zurück, einschließlich Name, Identität, Eigenschaften und zusätzlichen Clusterdetails.</span><span class="sxs-lookup"><span data-stu-id="97b62-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="97b62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97b62-104">SYNTAX</span></span>

### <span data-ttu-id="97b62-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="97b62-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97b62-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="97b62-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97b62-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97b62-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="97b62-108">Liste</span><span class="sxs-lookup"><span data-stu-id="97b62-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="97b62-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97b62-109">DESCRIPTION</span></span>
<span data-ttu-id="97b62-110">Gibt die Eigenschaften des angegebenen verbundenen Cluster zurück, einschließlich Name, Identität, Eigenschaften und zusätzlichen Clusterdetails.</span><span class="sxs-lookup"><span data-stu-id="97b62-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="97b62-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97b62-111">EXAMPLES</span></span>

### <span data-ttu-id="97b62-112">Beispiel 1: Alle verbundenen Kubernets unter einem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="97b62-112">Example 1: Get all connected kubernetes under a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="97b62-113">Dieser Befehl ruft alle verbundenen Kubernets unter einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="97b62-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="97b62-114">Beispiel 2: Alle verbundenen Kubernets unter der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="97b62-114">Example 2: Get all connected kubernetes under the resource group</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="97b62-115">Dieser Befehl ruft alle verbundenen Kubernets unter der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="97b62-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="97b62-116">Beispiel 3: Erhalten eines verbundenen Kubernets</span><span class="sxs-lookup"><span data-stu-id="97b62-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="97b62-117">Dieser Befehl ruft verbundene Kubernets ab.</span><span class="sxs-lookup"><span data-stu-id="97b62-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="97b62-118">Beispiel 4: Erhalten eines verbundenen Kubernets nach Objekt</span><span class="sxs-lookup"><span data-stu-id="97b62-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="97b62-119">Dieser Befehl ruft ein verbundenes Kubernetes nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="97b62-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="97b62-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97b62-120">PARAMETERS</span></span>

### <span data-ttu-id="97b62-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="97b62-121">-ClusterName</span></span>
<span data-ttu-id="97b62-122">Der Name des Kubernetes-Cluster, für den "get" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="97b62-122">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b62-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b62-123">-DefaultProfile</span></span>
<span data-ttu-id="97b62-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97b62-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97b62-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97b62-125">-InputObject</span></span>
<span data-ttu-id="97b62-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="97b62-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97b62-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b62-127">-ResourceGroupName</span></span>
<span data-ttu-id="97b62-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="97b62-128">The name of the resource group.</span></span>
<span data-ttu-id="97b62-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="97b62-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b62-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97b62-130">-SubscriptionId</span></span>
<span data-ttu-id="97b62-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="97b62-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b62-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b62-132">CommonParameters</span></span>
<span data-ttu-id="97b62-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b62-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b62-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97b62-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b62-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97b62-135">INPUTS</span></span>

### <span data-ttu-id="97b62-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedConnecternetes.Models.IConnectedKoppelernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="97b62-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="97b62-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97b62-137">OUTPUTS</span></span>

### <span data-ttu-id="97b62-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedConnecternetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="97b62-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="97b62-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="97b62-139">NOTES</span></span>

<span data-ttu-id="97b62-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="97b62-140">ALIASES</span></span>

<span data-ttu-id="97b62-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="97b62-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97b62-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="97b62-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97b62-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97b62-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97b62-144">INPUTOBJECT <IConnectedKubernetesIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="97b62-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97b62-145">`[ClusterName <String>]`: Der Name des Kubernetes-Cluster, für den "get" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="97b62-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="97b62-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="97b62-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97b62-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="97b62-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="97b62-148">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="97b62-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="97b62-149">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="97b62-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="97b62-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="97b62-150">RELATED LINKS</span></span>

