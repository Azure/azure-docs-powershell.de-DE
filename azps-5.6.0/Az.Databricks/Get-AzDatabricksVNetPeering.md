---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: a5654fa0974accf4319df4cbbd08ef220fa7ad9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925851"
---
# <span data-ttu-id="f7111-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="f7111-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="f7111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7111-102">SYNOPSIS</span></span>
<span data-ttu-id="f7111-103">Ruft den Arbeitsbereich vNet-Peering ab.</span><span class="sxs-lookup"><span data-stu-id="f7111-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="f7111-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7111-104">SYNTAX</span></span>

### <span data-ttu-id="f7111-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7111-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f7111-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="f7111-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="f7111-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f7111-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="f7111-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7111-108">DESCRIPTION</span></span>
<span data-ttu-id="f7111-109">Ruft den Arbeitsbereich vNet-Peering ab.</span><span class="sxs-lookup"><span data-stu-id="f7111-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="f7111-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7111-110">EXAMPLES</span></span>

### <span data-ttu-id="f7111-111">Beispiel 1: Auflisten aller Vnet-Peerings unter einem Databricks</span><span class="sxs-lookup"><span data-stu-id="f7111-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="f7111-112">Mit diesem Befehl werden alle vnet-Peerings unter einem Databricks aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7111-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="f7111-113">Beispiel 2: Erhalten eines vnet-Peerings</span><span class="sxs-lookup"><span data-stu-id="f7111-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="f7111-114">Dieser Befehl ruft ein vnet-Peering ab.</span><span class="sxs-lookup"><span data-stu-id="f7111-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="f7111-115">Beispiel 3: Erhalten eines vnet-Peerings nach -Objekt</span><span class="sxs-lookup"><span data-stu-id="f7111-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="f7111-116">Dieser Befehl ruft ein vnet-Peering nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="f7111-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="f7111-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f7111-117">PARAMETERS</span></span>

### <span data-ttu-id="f7111-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7111-118">-DefaultProfile</span></span>
<span data-ttu-id="f7111-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7111-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7111-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7111-120">-InputObject</span></span>
<span data-ttu-id="f7111-121">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f7111-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f7111-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f7111-122">-Name</span></span>
<span data-ttu-id="f7111-123">Der Name des Arbeitsbereichs vNet-Peering.</span><span class="sxs-lookup"><span data-stu-id="f7111-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="f7111-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7111-124">-PassThru</span></span>
<span data-ttu-id="f7111-125">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7111-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f7111-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7111-126">-ResourceGroupName</span></span>
<span data-ttu-id="f7111-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f7111-127">The name of the resource group.</span></span>
<span data-ttu-id="f7111-128">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="f7111-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f7111-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7111-129">-SubscriptionId</span></span>
<span data-ttu-id="f7111-130">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f7111-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f7111-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f7111-131">-WorkspaceName</span></span>
<span data-ttu-id="f7111-132">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f7111-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="f7111-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7111-133">CommonParameters</span></span>
<span data-ttu-id="f7111-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7111-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7111-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7111-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7111-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7111-136">INPUTS</span></span>

### <span data-ttu-id="f7111-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="f7111-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="f7111-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7111-138">OUTPUTS</span></span>

### <span data-ttu-id="f7111-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f7111-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="f7111-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f7111-140">NOTES</span></span>

<span data-ttu-id="f7111-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f7111-141">ALIASES</span></span>

<span data-ttu-id="f7111-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f7111-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f7111-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="f7111-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f7111-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f7111-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f7111-145">INPUTOBJECT <IDatabricksIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="f7111-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f7111-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f7111-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f7111-147">`[PeeringName <String>]`: Der Name des Arbeitsbereichs vNet-Peering.</span><span class="sxs-lookup"><span data-stu-id="f7111-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="f7111-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f7111-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f7111-149">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="f7111-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="f7111-150">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f7111-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f7111-151">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f7111-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="f7111-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f7111-152">RELATED LINKS</span></span>

