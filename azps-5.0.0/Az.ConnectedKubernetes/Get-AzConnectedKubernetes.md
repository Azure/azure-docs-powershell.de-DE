---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176959"
---
# <span data-ttu-id="b51cc-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="b51cc-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="b51cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b51cc-102">SYNOPSIS</span></span>
<span data-ttu-id="b51cc-103">Gibt die Eigenschaften des angegebenen verbundenen Clusters zurück, einschließlich Name, Identität, Eigenschaften und zusätzlicher Cluster Details.</span><span class="sxs-lookup"><span data-stu-id="b51cc-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="b51cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b51cc-104">SYNTAX</span></span>

### <span data-ttu-id="b51cc-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="b51cc-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b51cc-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="b51cc-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b51cc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b51cc-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b51cc-108">Liste</span><span class="sxs-lookup"><span data-stu-id="b51cc-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b51cc-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b51cc-109">DESCRIPTION</span></span>
<span data-ttu-id="b51cc-110">Gibt die Eigenschaften des angegebenen verbundenen Clusters zurück, einschließlich Name, Identität, Eigenschaften und zusätzlicher Cluster Details.</span><span class="sxs-lookup"><span data-stu-id="b51cc-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="b51cc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b51cc-111">EXAMPLES</span></span>

### <span data-ttu-id="b51cc-112">Beispiel 1: Abrufen aller verbundenen kubernetes unter einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="b51cc-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="b51cc-113">Dieser Befehl ruft alle verbundenen kubernetes unter einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b51cc-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="b51cc-114">Beispiel 2: Abrufen aller verbundenen kubernetes unter der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b51cc-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="b51cc-115">Dieser Befehl ruft alle verbundenen kubernetes unter der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b51cc-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="b51cc-116">Beispiel 3: Abrufen eines verbundenen kubernetes</span><span class="sxs-lookup"><span data-stu-id="b51cc-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="b51cc-117">Dieser Befehl ruft eine verbundene kubernetes ab.</span><span class="sxs-lookup"><span data-stu-id="b51cc-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="b51cc-118">Beispiel 4: Abrufen eines verbundenen kubernetes nach Objekt</span><span class="sxs-lookup"><span data-stu-id="b51cc-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="b51cc-119">Mit diesem Befehl wird ein verbundener kubernetes nach Objekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b51cc-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="b51cc-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="b51cc-120">PARAMETERS</span></span>

### <span data-ttu-id="b51cc-121">-Clustername</span><span class="sxs-lookup"><span data-stu-id="b51cc-121">-ClusterName</span></span>
<span data-ttu-id="b51cc-122">Der Name des Kubernetes-Clusters, in dem Get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b51cc-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="b51cc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b51cc-123">-DefaultProfile</span></span>
<span data-ttu-id="b51cc-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b51cc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b51cc-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b51cc-125">-InputObject</span></span>
<span data-ttu-id="b51cc-126">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b51cc-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b51cc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b51cc-127">-ResourceGroupName</span></span>
<span data-ttu-id="b51cc-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b51cc-128">The name of the resource group.</span></span>
<span data-ttu-id="b51cc-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="b51cc-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b51cc-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b51cc-130">-SubscriptionId</span></span>
<span data-ttu-id="b51cc-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="b51cc-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b51cc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b51cc-132">CommonParameters</span></span>
<span data-ttu-id="b51cc-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b51cc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b51cc-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b51cc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b51cc-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b51cc-135">INPUTS</span></span>

### <span data-ttu-id="b51cc-136">Microsoft. Azure. PowerShell. Cmdlets. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="b51cc-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="b51cc-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b51cc-137">OUTPUTS</span></span>

### <span data-ttu-id="b51cc-138">Microsoft. Azure. PowerShell. Cmdlets. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="b51cc-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="b51cc-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="b51cc-139">NOTES</span></span>

<span data-ttu-id="b51cc-140">Aliase</span><span class="sxs-lookup"><span data-stu-id="b51cc-140">ALIASES</span></span>

<span data-ttu-id="b51cc-141">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b51cc-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b51cc-142">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b51cc-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b51cc-143">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="b51cc-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b51cc-144">Inputobject <IConnectedKubernetesIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="b51cc-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b51cc-145">`[ClusterName <String>]`: Der Name des Kubernetes-Clusters, in dem Get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b51cc-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="b51cc-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="b51cc-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b51cc-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b51cc-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b51cc-148">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="b51cc-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="b51cc-149">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="b51cc-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="b51cc-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b51cc-150">RELATED LINKS</span></span>

