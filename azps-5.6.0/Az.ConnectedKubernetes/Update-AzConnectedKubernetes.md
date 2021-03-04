---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2e0c7f11592238f11f49e82102c6d58c24f8b9fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948835"
---
# <span data-ttu-id="aad5f-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="aad5f-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="aad5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aad5f-102">SYNOPSIS</span></span>
<span data-ttu-id="aad5f-103">API, um bestimmte Eigenschaften der verbundenen Clusterressource zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aad5f-103">API to update certain properties of the connected cluster resource.</span></span>

## <span data-ttu-id="aad5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aad5f-104">SYNTAX</span></span>

### <span data-ttu-id="aad5f-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="aad5f-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aad5f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="aad5f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aad5f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aad5f-107">DESCRIPTION</span></span>
<span data-ttu-id="aad5f-108">API, um bestimmte Eigenschaften der verbundenen Clusterressource zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aad5f-108">API to update certain properties of the connected cluster resource.</span></span>

## <span data-ttu-id="aad5f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aad5f-109">EXAMPLES</span></span>

### <span data-ttu-id="aad5f-110">Beispiel 1: Aktualisieren eines verbundenen Kubernetes</span><span class="sxs-lookup"><span data-stu-id="aad5f-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="aad5f-111">Mit diesem Befehl wird ein verbundenes Kubernetes aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="aad5f-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="aad5f-112">Beispiel 2: Aktualisieren eines verbundenen Kubernetes nach Objekt</span><span class="sxs-lookup"><span data-stu-id="aad5f-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="aad5f-113">Mit diesem Befehl wird ein verbundenes Kubernetes nach Objekt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="aad5f-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="aad5f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aad5f-114">PARAMETERS</span></span>

### <span data-ttu-id="aad5f-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="aad5f-115">-ClusterName</span></span>
<span data-ttu-id="aad5f-116">Der Name des Kubernetes-Clusters, für den get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="aad5f-116">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="aad5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad5f-117">-DefaultProfile</span></span>
<span data-ttu-id="aad5f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aad5f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aad5f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aad5f-119">-InputObject</span></span>
<span data-ttu-id="aad5f-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="aad5f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aad5f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad5f-121">-ResourceGroupName</span></span>
<span data-ttu-id="aad5f-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aad5f-122">The name of the resource group.</span></span>
<span data-ttu-id="aad5f-123">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="aad5f-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="aad5f-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aad5f-124">-SubscriptionId</span></span>
<span data-ttu-id="aad5f-125">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="aad5f-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="aad5f-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="aad5f-126">-Tag</span></span>
<span data-ttu-id="aad5f-127">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="aad5f-127">Resource tags.</span></span>

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

### <span data-ttu-id="aad5f-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aad5f-128">-Confirm</span></span>
<span data-ttu-id="aad5f-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aad5f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aad5f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aad5f-130">-WhatIf</span></span>
<span data-ttu-id="aad5f-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aad5f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aad5f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aad5f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aad5f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad5f-133">CommonParameters</span></span>
<span data-ttu-id="aad5f-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad5f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad5f-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aad5f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad5f-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aad5f-136">INPUTS</span></span>

### <span data-ttu-id="aad5f-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="aad5f-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="aad5f-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aad5f-138">OUTPUTS</span></span>

### <span data-ttu-id="aad5f-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="aad5f-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="aad5f-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aad5f-140">NOTES</span></span>

<span data-ttu-id="aad5f-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="aad5f-141">ALIASES</span></span>

<span data-ttu-id="aad5f-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="aad5f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aad5f-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="aad5f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aad5f-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aad5f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aad5f-145">INPUTOBJECT <IConnectedKubernetesIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="aad5f-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aad5f-146">`[ClusterName <String>]`: Der Name des Kubernetes-Clusters, für den get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="aad5f-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="aad5f-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="aad5f-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aad5f-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aad5f-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="aad5f-149">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="aad5f-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="aad5f-150">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="aad5f-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="aad5f-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aad5f-151">RELATED LINKS</span></span>

