---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297322"
---
# <span data-ttu-id="6ba71-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="6ba71-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="6ba71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ba71-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba71-103">Erstellt vNet-Peering für Workspace.</span><span class="sxs-lookup"><span data-stu-id="6ba71-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="6ba71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ba71-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6ba71-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ba71-105">DESCRIPTION</span></span>
<span data-ttu-id="6ba71-106">Erstellt vNet-Peering für Workspace.</span><span class="sxs-lookup"><span data-stu-id="6ba71-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="6ba71-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ba71-107">EXAMPLES</span></span>

### <span data-ttu-id="6ba71-108">Beispiel 1: Erstellen eines vnet-Peerings für databricks</span><span class="sxs-lookup"><span data-stu-id="6ba71-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="6ba71-109">Dieser Befehl erstellt ein vnet-Peering für databricks.</span><span class="sxs-lookup"><span data-stu-id="6ba71-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="6ba71-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ba71-110">PARAMETERS</span></span>

### <span data-ttu-id="6ba71-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="6ba71-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="6ba71-112">Ob der weitergeleitete Datenverkehr von den VMS im lokalen virtuellen Netzwerk im virtuellen Remotenetzwerk zugelassen/nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6ba71-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="6ba71-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="6ba71-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="6ba71-114">Wenn Gateway-Links im virtuellen Remotenetzwerk verwendet werden können, um eine Verknüpfung mit diesem virtuellen Netzwerk herzustellen.</span><span class="sxs-lookup"><span data-stu-id="6ba71-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="6ba71-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="6ba71-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="6ba71-116">Gibt an, ob die VMs im lokalen virtuellen Netzwerkbereich auf die VMs im Remotespeicher des virtuellen Netzwerks zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="6ba71-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="6ba71-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ba71-117">-AsJob</span></span>
<span data-ttu-id="6ba71-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="6ba71-118">Run the command as a job</span></span>

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

### <span data-ttu-id="6ba71-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="6ba71-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="6ba71-120">Eine Liste der Adressblöcke, die für dieses virtuelle Netzwerk in der CIDR-Notation reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="6ba71-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="6ba71-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6ba71-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="6ba71-122">Die ID des virtuellen databricks-Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="6ba71-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="6ba71-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba71-123">-DefaultProfile</span></span>
<span data-ttu-id="6ba71-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6ba71-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ba71-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6ba71-125">-Name</span></span>
<span data-ttu-id="6ba71-126">Der Name des Arbeitsbereichs vNet Peering.</span><span class="sxs-lookup"><span data-stu-id="6ba71-126">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="6ba71-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6ba71-127">-NoWait</span></span>
<span data-ttu-id="6ba71-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="6ba71-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6ba71-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="6ba71-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="6ba71-130">Eine Liste der Adressblöcke, die für dieses virtuelle Netzwerk in der CIDR-Notation reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="6ba71-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="6ba71-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6ba71-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="6ba71-132">Die ID des virtuellen Remotenetzwerks.</span><span class="sxs-lookup"><span data-stu-id="6ba71-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="6ba71-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ba71-133">-ResourceGroupName</span></span>
<span data-ttu-id="6ba71-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6ba71-134">The name of the resource group.</span></span>
<span data-ttu-id="6ba71-135">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="6ba71-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6ba71-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="6ba71-136">-SubscriptionId</span></span>
<span data-ttu-id="6ba71-137">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="6ba71-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6ba71-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="6ba71-138">-UseRemoteGateway</span></span>
<span data-ttu-id="6ba71-139">Wenn Remote-Gateways in diesem virtuellen Netzwerk verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6ba71-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="6ba71-140">Wenn das Flag auf "true" festgelegt ist und allowGatewayTransit auf Remote Peering ebenfalls wahr ist, verwendet virtuelles Netzwerkgateways des virtuellen Remotenetzwerks für die Übertragung.</span><span class="sxs-lookup"><span data-stu-id="6ba71-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="6ba71-141">Dieses Flag kann nur von einem Peering auf "true" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6ba71-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="6ba71-142">Dieses Flag kann nicht gesetzt werden, wenn virtuelles Netzwerk bereits über ein Gateway verfügt.</span><span class="sxs-lookup"><span data-stu-id="6ba71-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="6ba71-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6ba71-143">-WorkspaceName</span></span>
<span data-ttu-id="6ba71-144">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="6ba71-144">The name of the workspace.</span></span>

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

### <span data-ttu-id="6ba71-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6ba71-145">-Confirm</span></span>
<span data-ttu-id="6ba71-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ba71-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ba71-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ba71-147">-WhatIf</span></span>
<span data-ttu-id="6ba71-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ba71-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ba71-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ba71-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ba71-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba71-150">CommonParameters</span></span>
<span data-ttu-id="6ba71-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ba71-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba71-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ba71-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba71-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ba71-153">INPUTS</span></span>

## <span data-ttu-id="6ba71-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ba71-154">OUTPUTS</span></span>

### <span data-ttu-id="6ba71-155">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6ba71-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="6ba71-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ba71-156">NOTES</span></span>

<span data-ttu-id="6ba71-157">Aliase</span><span class="sxs-lookup"><span data-stu-id="6ba71-157">ALIASES</span></span>

## <span data-ttu-id="6ba71-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ba71-158">RELATED LINKS</span></span>

