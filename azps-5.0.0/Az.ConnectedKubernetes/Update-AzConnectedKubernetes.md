---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176956"
---
# <span data-ttu-id="3751b-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="3751b-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="3751b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3751b-102">SYNOPSIS</span></span>
<span data-ttu-id="3751b-103">API zum Aktualisieren bestimmter Eigenschaften der verbundenen Clusterressource</span><span class="sxs-lookup"><span data-stu-id="3751b-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="3751b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3751b-104">SYNTAX</span></span>

### <span data-ttu-id="3751b-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="3751b-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3751b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3751b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3751b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3751b-107">DESCRIPTION</span></span>
<span data-ttu-id="3751b-108">API zum Aktualisieren bestimmter Eigenschaften der verbundenen Clusterressource</span><span class="sxs-lookup"><span data-stu-id="3751b-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="3751b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3751b-109">EXAMPLES</span></span>

### <span data-ttu-id="3751b-110">Beispiel 1: Aktualisieren einer verbundenen kubernetes</span><span class="sxs-lookup"><span data-stu-id="3751b-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="3751b-111">Mit diesem Befehl wird ein verbundener kubernetes aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3751b-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="3751b-112">Beispiel 2: Aktualisieren einer verbundenen kubernetes nach Objekt</span><span class="sxs-lookup"><span data-stu-id="3751b-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="3751b-113">Dieser Befehl aktualisiert eine verbundene kubernetes nach Objekt.</span><span class="sxs-lookup"><span data-stu-id="3751b-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="3751b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3751b-114">PARAMETERS</span></span>

### <span data-ttu-id="3751b-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="3751b-115">-ClusterName</span></span>
<span data-ttu-id="3751b-116">Der Name des Kubernetes-Clusters, in dem Get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3751b-116">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3751b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3751b-117">-DefaultProfile</span></span>
<span data-ttu-id="3751b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3751b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3751b-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3751b-119">-InputObject</span></span>
<span data-ttu-id="3751b-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3751b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3751b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3751b-121">-ResourceGroupName</span></span>
<span data-ttu-id="3751b-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3751b-122">The name of the resource group.</span></span>
<span data-ttu-id="3751b-123">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="3751b-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3751b-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="3751b-124">-SubscriptionId</span></span>
<span data-ttu-id="3751b-125">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="3751b-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3751b-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="3751b-126">-Tag</span></span>
<span data-ttu-id="3751b-127">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="3751b-127">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3751b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3751b-128">-Confirm</span></span>
<span data-ttu-id="3751b-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3751b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3751b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3751b-130">-WhatIf</span></span>
<span data-ttu-id="3751b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3751b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3751b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3751b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3751b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3751b-133">CommonParameters</span></span>
<span data-ttu-id="3751b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3751b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3751b-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3751b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3751b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3751b-136">INPUTS</span></span>

### <span data-ttu-id="3751b-137">Microsoft. Azure. PowerShell. Cmdlets. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="3751b-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="3751b-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3751b-138">OUTPUTS</span></span>

### <span data-ttu-id="3751b-139">Microsoft. Azure. PowerShell. Cmdlets. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="3751b-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="3751b-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="3751b-140">NOTES</span></span>

<span data-ttu-id="3751b-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="3751b-141">ALIASES</span></span>

<span data-ttu-id="3751b-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3751b-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3751b-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3751b-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3751b-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="3751b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3751b-145">Inputobject <IConnectedKubernetesIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="3751b-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3751b-146">`[ClusterName <String>]`: Der Name des Kubernetes-Clusters, in dem Get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3751b-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="3751b-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="3751b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3751b-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3751b-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3751b-149">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="3751b-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="3751b-150">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="3751b-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="3751b-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3751b-151">RELATED LINKS</span></span>

