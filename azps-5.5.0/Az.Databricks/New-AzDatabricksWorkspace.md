---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 0626559fd80a9ebd212c8f6ebb032755d25ba59c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170790"
---
# <span data-ttu-id="20048-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="20048-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="20048-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20048-102">SYNOPSIS</span></span>
<span data-ttu-id="20048-103">Erstellt einen neuen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="20048-103">Creates a new workspace.</span></span>

## <span data-ttu-id="20048-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20048-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-EnableNoPublicIP] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20048-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20048-105">DESCRIPTION</span></span>
<span data-ttu-id="20048-106">Erstellt einen neuen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="20048-106">Creates a new workspace.</span></span>

## <span data-ttu-id="20048-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20048-107">EXAMPLES</span></span>

### <span data-ttu-id="20048-108">Beispiel 1: Erstellen eines Datenarbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="20048-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="20048-109">Mit diesem Befehl wird ein Arbeitsbereich "Databungs" erstellt.</span><span class="sxs-lookup"><span data-stu-id="20048-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="20048-110">Beispiel 2: Erstellen eines Arbeitsbereichs mit einem benutzerdefinierten virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="20048-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
```powershell
PS C:\> $dlg = New-AzDelegation -Name dbrdl -ServiceName "Microsoft.Databricks/workspaces"
PS C:\> $rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName testgroup -Location eastus -Name nsg-test -SecurityRules $rdpRule
PS C:\> $privSubnet = New-AzVirtualNetworkSubnetConfig -Name priv-sub -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $pubSubnet = New-AzVirtualNetworkSubnetConfig -Name pub-sub  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $testVN = New-AzVirtualNetwork -Name testvn -ResourceGroupName testgroup -Location eastus -AddressPrefix "10.0.0.0/16" -Subnet $privSubnet,$pubSubnet
PS C:\> New-AzDatabricksWorkspace -Name databricks-test-with-custom-vn -ResourceGroupName testgroup -Location eastus -VirtualNetworkId $testVN.Id -PrivateSubnetName $privSubnet.Name -PublicSubnetName $privSubnet.Name -Sku standard

Location Name                           Type
-------- ----                           ----
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="20048-111">Mit diesem Befehl wird ein Databungsarbeitsbereich mit benutzerdefiniertem virtuellem Netzwerk in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="20048-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="20048-112">Beispiel 3: Erstellen eines Datenarbeitsbereichs mit Aktivierter Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="20048-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="20048-113">Dieser Befehl erstellt einen Arbeitsbereich "Databungs" und legt ihn so fest, dass er für die Verschlüsselung vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="20048-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="20048-114">Weitere Einstellungen zur Verschlüsselung finden Sie in Update-AzDatabricksWorkspace Beispielen für die Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="20048-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="20048-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20048-115">PARAMETERS</span></span>

### <span data-ttu-id="20048-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20048-116">-AsJob</span></span>
<span data-ttu-id="20048-117">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="20048-117">Run the command as a job</span></span>

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

### <span data-ttu-id="20048-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20048-118">-DefaultProfile</span></span>
<span data-ttu-id="20048-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20048-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20048-120">-EnableNoPublicIP</span><span class="sxs-lookup"><span data-stu-id="20048-120">-EnableNoPublicIP</span></span>
<span data-ttu-id="20048-121">Der Wert, der für dieses Feld verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="20048-121">The value which should be used for this field.</span></span>

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

### <span data-ttu-id="20048-122">-Location</span><span class="sxs-lookup"><span data-stu-id="20048-122">-Location</span></span>
<span data-ttu-id="20048-123">Der geo-Standort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="20048-123">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="20048-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20048-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="20048-125">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="20048-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="20048-126">-Name</span><span class="sxs-lookup"><span data-stu-id="20048-126">-Name</span></span>
<span data-ttu-id="20048-127">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="20048-127">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20048-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="20048-128">-NoWait</span></span>
<span data-ttu-id="20048-129">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="20048-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="20048-130">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="20048-130">-PrepareEncryption</span></span>
<span data-ttu-id="20048-131">Bereiten Sie den Arbeitsbereich für die Verschlüsselung vor.</span><span class="sxs-lookup"><span data-stu-id="20048-131">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="20048-132">Aktiviert die verwaltete Identität für verwaltete Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="20048-132">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="20048-133">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="20048-133">-PrivateSubnetName</span></span>
<span data-ttu-id="20048-134">Der Name des privaten Subnetzes innerhalb des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="20048-134">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="20048-135">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="20048-135">-PublicSubnetName</span></span>
<span data-ttu-id="20048-136">Der Name eines öffentlichen Subnetzes innerhalb des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="20048-136">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="20048-137">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="20048-137">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="20048-138">Ein boolescher Wert, der angibt, ob das DBFS-Stammdateisystem mit sekundärer Verschlüsselungsebene mit plattform verwalteten Schlüsseln für ruhede Daten aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="20048-138">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="20048-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20048-139">-ResourceGroupName</span></span>
<span data-ttu-id="20048-140">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="20048-140">The name of the resource group.</span></span>
<span data-ttu-id="20048-141">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="20048-141">The name is case insensitive.</span></span>

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

### <span data-ttu-id="20048-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="20048-142">-Sku</span></span>
<span data-ttu-id="20048-143">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="20048-143">The SKU name.</span></span>

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

### <span data-ttu-id="20048-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20048-144">-SubscriptionId</span></span>
<span data-ttu-id="20048-145">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="20048-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="20048-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="20048-146">-Tag</span></span>
<span data-ttu-id="20048-147">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="20048-147">Resource tags.</span></span>

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

### <span data-ttu-id="20048-148">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="20048-148">-VirtualNetworkId</span></span>
<span data-ttu-id="20048-149">Die ID eines virtuellen Netzwerks, in dem dieser Datenknotencluster erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="20048-149">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="20048-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20048-150">-Confirm</span></span>
<span data-ttu-id="20048-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20048-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20048-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="20048-152">-WhatIf</span></span>
<span data-ttu-id="20048-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20048-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20048-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20048-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20048-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20048-155">CommonParameters</span></span>
<span data-ttu-id="20048-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20048-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20048-157">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20048-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20048-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20048-158">INPUTS</span></span>

## <span data-ttu-id="20048-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20048-159">OUTPUTS</span></span>

### <span data-ttu-id="20048-160">Microsoft.Azure.PowerShell.Cmdlets.Databpersonenbezogenes.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="20048-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="20048-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="20048-161">NOTES</span></span>

<span data-ttu-id="20048-162">ALIASE</span><span class="sxs-lookup"><span data-stu-id="20048-162">ALIASES</span></span>

## <span data-ttu-id="20048-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="20048-163">RELATED LINKS</span></span>

