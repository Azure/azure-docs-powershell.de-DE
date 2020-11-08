---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 09f1cd27e9af0c6442afa00d5301975cae8fbdeb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008017"
---
# <span data-ttu-id="c33d4-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="c33d4-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="c33d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c33d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c33d4-103">Erstellt einen neuen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="c33d4-103">Creates a new workspace.</span></span>

## <span data-ttu-id="c33d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c33d4-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c33d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c33d4-105">DESCRIPTION</span></span>
<span data-ttu-id="c33d4-106">Erstellt einen neuen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="c33d4-106">Creates a new workspace.</span></span>

## <span data-ttu-id="c33d4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c33d4-107">EXAMPLES</span></span>

### <span data-ttu-id="c33d4-108">Beispiel 1: Erstellen eines databricks-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="c33d4-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="c33d4-109">Mit diesem Befehl wird ein databricks-Arbeitsbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="c33d4-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="c33d4-110">Beispiel 2: Erstellen eines databricks-Arbeitsbereichs mit einem angepassten virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="c33d4-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
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

<span data-ttu-id="c33d4-111">Mit diesem Befehl wird ein databricks-Arbeitsbereich mit angepasstem virtuellen Netzwerk in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="c33d4-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="c33d4-112">Beispiel 3: Erstellen eines databricks-Arbeitsbereichs mit enable Encryption</span><span class="sxs-lookup"><span data-stu-id="c33d4-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="c33d4-113">Mit diesem Befehl wird ein databricks-Arbeitsbereich erstellt und für die Verschlüsselung vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="c33d4-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="c33d4-114">Weitere Einstellungen für die Verschlüsselung finden Sie in den Beispielen Update-AzDatabricksWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c33d4-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="c33d4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c33d4-115">PARAMETERS</span></span>

### <span data-ttu-id="c33d4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c33d4-116">-AsJob</span></span>
<span data-ttu-id="c33d4-117">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="c33d4-117">Run the command as a job</span></span>

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

### <span data-ttu-id="c33d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c33d4-118">-DefaultProfile</span></span>
<span data-ttu-id="c33d4-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c33d4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c33d4-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="c33d4-120">-Location</span></span>
<span data-ttu-id="c33d4-121">Der Geo-Standort, an dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="c33d4-121">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="c33d4-122">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c33d4-122">-ManagedResourceGroupName</span></span>
<span data-ttu-id="c33d4-123">Der Name der verwalteten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c33d4-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="c33d4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c33d4-124">-Name</span></span>
<span data-ttu-id="c33d4-125">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c33d4-125">The name of the workspace.</span></span>

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

### <span data-ttu-id="c33d4-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c33d4-126">-NoWait</span></span>
<span data-ttu-id="c33d4-127">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="c33d4-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c33d4-128">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="c33d4-128">-PrepareEncryption</span></span>
<span data-ttu-id="c33d4-129">Bereiten Sie den Arbeitsbereich für die Verschlüsselung vor.</span><span class="sxs-lookup"><span data-stu-id="c33d4-129">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="c33d4-130">Aktiviert die verwaltete Identität für das verwaltete Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="c33d4-130">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="c33d4-131">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="c33d4-131">-PrivateSubnetName</span></span>
<span data-ttu-id="c33d4-132">Der Name des privaten Subnetzes im virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c33d4-132">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="c33d4-133">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="c33d4-133">-PublicSubnetName</span></span>
<span data-ttu-id="c33d4-134">Der Name eines öffentlichen Subnetzes im virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c33d4-134">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="c33d4-135">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="c33d4-135">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="c33d4-136">Ein boolescher Wert, der angibt, ob das dBFS-Root-Dateisystem mit der sekundären Verschlüsselungsebene mit Platt Form verwalteten Schlüsseln für Daten im Ruhezustand aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c33d4-136">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="c33d4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c33d4-137">-ResourceGroupName</span></span>
<span data-ttu-id="c33d4-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c33d4-138">The name of the resource group.</span></span>
<span data-ttu-id="c33d4-139">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="c33d4-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c33d4-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="c33d4-140">-Sku</span></span>
<span data-ttu-id="c33d4-141">Der SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="c33d4-141">The SKU name.</span></span>

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

### <span data-ttu-id="c33d4-142">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c33d4-142">-SubscriptionId</span></span>
<span data-ttu-id="c33d4-143">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c33d4-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c33d4-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="c33d4-144">-Tag</span></span>
<span data-ttu-id="c33d4-145">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="c33d4-145">Resource tags.</span></span>

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

### <span data-ttu-id="c33d4-146">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c33d4-146">-VirtualNetworkId</span></span>
<span data-ttu-id="c33d4-147">Die ID eines virtuellen Netzwerks, in dem dieser databricks-Cluster erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c33d4-147">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="c33d4-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c33d4-148">-Confirm</span></span>
<span data-ttu-id="c33d4-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c33d4-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c33d4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c33d4-150">-WhatIf</span></span>
<span data-ttu-id="c33d4-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c33d4-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c33d4-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c33d4-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c33d4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33d4-153">CommonParameters</span></span>
<span data-ttu-id="c33d4-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c33d4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33d4-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c33d4-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33d4-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c33d4-156">INPUTS</span></span>

## <span data-ttu-id="c33d4-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c33d4-157">OUTPUTS</span></span>

### <span data-ttu-id="c33d4-158">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="c33d4-158">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="c33d4-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="c33d4-159">NOTES</span></span>

<span data-ttu-id="c33d4-160">Aliase</span><span class="sxs-lookup"><span data-stu-id="c33d4-160">ALIASES</span></span>

## <span data-ttu-id="c33d4-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c33d4-161">RELATED LINKS</span></span>

