---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299040"
---
# <span data-ttu-id="e0750-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="e0750-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="e0750-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0750-102">SYNOPSIS</span></span>
<span data-ttu-id="e0750-103">Erstellen Sie ein zusätzliches Mitglied.</span><span class="sxs-lookup"><span data-stu-id="e0750-103">Create a blockchain member.</span></span>

## <span data-ttu-id="e0750-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0750-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0750-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0750-105">DESCRIPTION</span></span>
<span data-ttu-id="e0750-106">Erstellen Sie ein benutzerdefiniertes Mitglied.</span><span class="sxs-lookup"><span data-stu-id="e0750-106">Create a blockchain member.</span></span>

## <span data-ttu-id="e0750-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0750-107">EXAMPLES</span></span>

### <span data-ttu-id="e0750-108">Beispiel 1: Erstellen eines neuen Mitglieds</span><span class="sxs-lookup"><span data-stu-id="e0750-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="e0750-109">Mit diesem Befehl wird ein neues Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0750-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="e0750-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0750-110">PARAMETERS</span></span>

### <span data-ttu-id="e0750-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0750-111">-AsJob</span></span>
<span data-ttu-id="e0750-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e0750-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e0750-113">-Consortium</span><span class="sxs-lookup"><span data-stu-id="e0750-113">-Consortium</span></span>
<span data-ttu-id="e0750-114">Ruft das Consortium für das neue Mitglied ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="e0750-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="e0750-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="e0750-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="e0750-116">Legt das Kennwort für das Verwaltungskonto des Managed Consortiums fest.</span><span class="sxs-lookup"><span data-stu-id="e0750-116">Sets the managed consortium management account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0750-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="e0750-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="e0750-118">Ruft den Anzeigenamen des Mitglieds im Consortium ab.</span><span class="sxs-lookup"><span data-stu-id="e0750-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="e0750-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="e0750-119">-ConsortiumRole</span></span>
<span data-ttu-id="e0750-120">Ruft die Rolle des Mitglieds im Consortium ab.</span><span class="sxs-lookup"><span data-stu-id="e0750-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="e0750-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0750-121">-DefaultProfile</span></span>
<span data-ttu-id="e0750-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0750-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0750-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="e0750-123">-FirewallRule</span></span>
<span data-ttu-id="e0750-124">Ruft Firewallregeln ab oder legt diese fest. Informationen zu #A0 und zum Erstellen einer Hashtabelle finden Sie im Abschnitt "NOTIZEN".</span><span class="sxs-lookup"><span data-stu-id="e0750-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0750-125">-Location</span><span class="sxs-lookup"><span data-stu-id="e0750-125">-Location</span></span>
<span data-ttu-id="e0750-126">Die GEO-Position des Kundendiensts.</span><span class="sxs-lookup"><span data-stu-id="e0750-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="e0750-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e0750-127">-Name</span></span>
<span data-ttu-id="e0750-128">Name des Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="e0750-128">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0750-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e0750-129">-NoWait</span></span>
<span data-ttu-id="e0750-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e0750-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e0750-131">-Password</span><span class="sxs-lookup"><span data-stu-id="e0750-131">-Password</span></span>
<span data-ttu-id="e0750-132">Legt das grundlegende Authentifizierungskennwort des Mitglieds fest.</span><span class="sxs-lookup"><span data-stu-id="e0750-132">Sets the basic auth password of the blockchain member.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0750-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e0750-133">-Protocol</span></span>
<span data-ttu-id="e0750-134">Ruft das Protokoll ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="e0750-134">Gets or sets the blockchain protocol.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Support.BlockchainProtocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0750-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0750-135">-ResourceGroupName</span></span>
<span data-ttu-id="e0750-136">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="e0750-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e0750-137">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="e0750-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e0750-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="e0750-138">-Sku</span></span>
<span data-ttu-id="e0750-139">Ruft den Namen der SKU ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e0750-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="e0750-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e0750-140">-SkuTier</span></span>
<span data-ttu-id="e0750-141">Ruft die SKU- Stufe ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e0750-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="e0750-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0750-142">-SubscriptionId</span></span>
<span data-ttu-id="e0750-143">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e0750-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e0750-144">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="e0750-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e0750-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0750-145">-Tag</span></span>
<span data-ttu-id="e0750-146">Tags des Diensts, bei dem es sich um eine Liste von Schlüsselwertpaaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e0750-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="e0750-147">-ValidatorNodeSku1</span><span class="sxs-lookup"><span data-stu-id="e0750-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="e0750-148">Ruft die Knotenkapazität ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e0750-148">Gets or sets the nodes capacity.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0750-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0750-149">-Confirm</span></span>
<span data-ttu-id="e0750-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0750-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0750-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e0750-151">-WhatIf</span></span>
<span data-ttu-id="e0750-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0750-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0750-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0750-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0750-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0750-154">CommonParameters</span></span>
<span data-ttu-id="e0750-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0750-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0750-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0750-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0750-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0750-157">INPUTS</span></span>

## <span data-ttu-id="e0750-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0750-158">OUTPUTS</span></span>

### <span data-ttu-id="e0750-159">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="e0750-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="e0750-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e0750-160">NOTES</span></span>

<span data-ttu-id="e0750-161">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e0750-161">ALIASES</span></span>

<span data-ttu-id="e0750-162">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e0750-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0750-163">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e0750-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0750-164">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0750-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0750-165">FIREWALLRULE <IFirewallRule[]>: Ruft Firewallregeln ab oder legt sie fest</span><span class="sxs-lookup"><span data-stu-id="e0750-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="e0750-166">`[EndIPAddress <String>]`: Ruft die End-IP-Adresse des Firewallregelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e0750-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="e0750-167">`[RuleName <String>]`: Ruft den Namen der Firewallregeln ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="e0750-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="e0750-168">`[StartIPAddress <String>]`: Ruft die Start-IP-Adresse des Firewallregelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e0750-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="e0750-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e0750-169">RELATED LINKS</span></span>

