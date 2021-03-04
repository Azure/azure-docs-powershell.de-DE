---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: da4cd54b9865cdf30487a7e49e5581474ebb2a35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948880"
---
# <span data-ttu-id="21d50-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="21d50-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="21d50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21d50-102">SYNOPSIS</span></span>
<span data-ttu-id="21d50-103">Gibt die Eigenschaften des angegebenen verbundenen Clusters zurück, einschließlich Name, Identität, Eigenschaften und zusätzlichen Clusterdetails.</span><span class="sxs-lookup"><span data-stu-id="21d50-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="21d50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21d50-104">SYNTAX</span></span>

### <span data-ttu-id="21d50-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="21d50-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="21d50-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="21d50-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="21d50-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="21d50-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="21d50-108">Liste</span><span class="sxs-lookup"><span data-stu-id="21d50-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="21d50-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21d50-109">DESCRIPTION</span></span>
<span data-ttu-id="21d50-110">Gibt die Eigenschaften des angegebenen verbundenen Clusters zurück, einschließlich Name, Identität, Eigenschaften und zusätzlichen Clusterdetails.</span><span class="sxs-lookup"><span data-stu-id="21d50-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="21d50-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21d50-111">EXAMPLES</span></span>

### <span data-ttu-id="21d50-112">Beispiel 1: Alle verbundenen Kubernetes unter einem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="21d50-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="21d50-113">Dieser Befehl ruft alle verbundenen Kubernetes unter einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="21d50-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="21d50-114">Beispiel 2: Alle verbundenen Kubernetes unter der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="21d50-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="21d50-115">Dieser Befehl ruft alle verbundenen Kubernetes unter der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="21d50-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="21d50-116">Beispiel 3: Erhalten eines verbundenen Kubernetes</span><span class="sxs-lookup"><span data-stu-id="21d50-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="21d50-117">Dieser Befehl ruft ein verbundenes Kubernetes ab.</span><span class="sxs-lookup"><span data-stu-id="21d50-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="21d50-118">Beispiel 4: Erstellen eines verbundenen Kubernetes nach Objekt</span><span class="sxs-lookup"><span data-stu-id="21d50-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="21d50-119">Dieser Befehl ruft ein verbundenes Kubernetes nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="21d50-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="21d50-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="21d50-120">PARAMETERS</span></span>

### <span data-ttu-id="21d50-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="21d50-121">-ClusterName</span></span>
<span data-ttu-id="21d50-122">Der Name des Kubernetes-Clusters, für den get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="21d50-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="21d50-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d50-123">-DefaultProfile</span></span>
<span data-ttu-id="21d50-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21d50-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21d50-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21d50-125">-InputObject</span></span>
<span data-ttu-id="21d50-126">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="21d50-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="21d50-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d50-127">-ResourceGroupName</span></span>
<span data-ttu-id="21d50-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="21d50-128">The name of the resource group.</span></span>
<span data-ttu-id="21d50-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="21d50-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="21d50-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="21d50-130">-SubscriptionId</span></span>
<span data-ttu-id="21d50-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="21d50-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="21d50-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d50-132">CommonParameters</span></span>
<span data-ttu-id="21d50-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21d50-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d50-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21d50-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d50-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21d50-135">INPUTS</span></span>

### <span data-ttu-id="21d50-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="21d50-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="21d50-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21d50-137">OUTPUTS</span></span>

### <span data-ttu-id="21d50-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="21d50-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="21d50-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="21d50-139">NOTES</span></span>

<span data-ttu-id="21d50-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="21d50-140">ALIASES</span></span>

<span data-ttu-id="21d50-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="21d50-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="21d50-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="21d50-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="21d50-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="21d50-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="21d50-144">INPUTOBJECT <IConnectedKubernetesIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="21d50-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="21d50-145">`[ClusterName <String>]`: Der Name des Kubernetes-Clusters, für den get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="21d50-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="21d50-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="21d50-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="21d50-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="21d50-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="21d50-148">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="21d50-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="21d50-149">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="21d50-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="21d50-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="21d50-150">RELATED LINKS</span></span>

