---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297345"
---
# <span data-ttu-id="e51de-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="e51de-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="e51de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e51de-102">SYNOPSIS</span></span>
<span data-ttu-id="e51de-103">Ruft den Arbeitsbereich vNet Peering ab.</span><span class="sxs-lookup"><span data-stu-id="e51de-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="e51de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e51de-104">SYNTAX</span></span>

### <span data-ttu-id="e51de-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="e51de-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e51de-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e51de-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e51de-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e51de-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="e51de-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e51de-108">DESCRIPTION</span></span>
<span data-ttu-id="e51de-109">Ruft den Arbeitsbereich vNet Peering ab.</span><span class="sxs-lookup"><span data-stu-id="e51de-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="e51de-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e51de-110">EXAMPLES</span></span>

### <span data-ttu-id="e51de-111">Beispiel 1: Auflisten aller vnet-Peering unter einem databricks</span><span class="sxs-lookup"><span data-stu-id="e51de-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="e51de-112">Dieser Befehl listet alle vnet-Peering unter einem databricks auf.</span><span class="sxs-lookup"><span data-stu-id="e51de-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="e51de-113">Beispiel 2: Abrufen eines vnet-Peerings</span><span class="sxs-lookup"><span data-stu-id="e51de-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="e51de-114">Dieser Befehl ruft einen vnet-Peering ab.</span><span class="sxs-lookup"><span data-stu-id="e51de-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="e51de-115">Beispiel 3: Abrufen eines vnet-Peerings nach Objekt</span><span class="sxs-lookup"><span data-stu-id="e51de-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="e51de-116">Mit diesem Befehl wird ein vnet-Peering nach Objekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e51de-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="e51de-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e51de-117">PARAMETERS</span></span>

### <span data-ttu-id="e51de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51de-118">-DefaultProfile</span></span>
<span data-ttu-id="e51de-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e51de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e51de-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e51de-120">-InputObject</span></span>
<span data-ttu-id="e51de-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e51de-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e51de-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e51de-122">-Name</span></span>
<span data-ttu-id="e51de-123">Der Name des Arbeitsbereichs vNet Peering.</span><span class="sxs-lookup"><span data-stu-id="e51de-123">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51de-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e51de-124">-PassThru</span></span>
<span data-ttu-id="e51de-125">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="e51de-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51de-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e51de-126">-ResourceGroupName</span></span>
<span data-ttu-id="e51de-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e51de-127">The name of the resource group.</span></span>
<span data-ttu-id="e51de-128">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="e51de-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e51de-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e51de-129">-SubscriptionId</span></span>
<span data-ttu-id="e51de-130">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e51de-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51de-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e51de-131">-WorkspaceName</span></span>
<span data-ttu-id="e51de-132">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e51de-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="e51de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51de-133">CommonParameters</span></span>
<span data-ttu-id="e51de-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e51de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51de-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e51de-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51de-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e51de-136">INPUTS</span></span>

### <span data-ttu-id="e51de-137">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="e51de-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="e51de-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e51de-138">OUTPUTS</span></span>

### <span data-ttu-id="e51de-139">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e51de-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="e51de-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="e51de-140">NOTES</span></span>

<span data-ttu-id="e51de-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="e51de-141">ALIASES</span></span>

<span data-ttu-id="e51de-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e51de-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e51de-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e51de-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e51de-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="e51de-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e51de-145">Inputobject <IDatabricksIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="e51de-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e51de-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="e51de-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e51de-147">`[PeeringName <String>]`: Der Name des Arbeitsbereichs vNet Peering.</span><span class="sxs-lookup"><span data-stu-id="e51de-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="e51de-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e51de-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e51de-149">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="e51de-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="e51de-150">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e51de-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e51de-151">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e51de-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="e51de-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e51de-152">RELATED LINKS</span></span>

