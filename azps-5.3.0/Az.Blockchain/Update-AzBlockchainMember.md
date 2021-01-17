---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471046"
---
# <span data-ttu-id="c1df4-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="c1df4-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="c1df4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1df4-102">SYNOPSIS</span></span>
<span data-ttu-id="c1df4-103">Aktualisieren Sie ein mitglied.</span><span class="sxs-lookup"><span data-stu-id="c1df4-103">Update a blockchain member.</span></span>

## <span data-ttu-id="c1df4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1df4-104">SYNTAX</span></span>

### <span data-ttu-id="c1df4-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1df4-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c1df4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c1df4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c1df4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1df4-107">DESCRIPTION</span></span>
<span data-ttu-id="c1df4-108">Aktualisieren Sie ein mitglied.</span><span class="sxs-lookup"><span data-stu-id="c1df4-108">Update a blockchain member.</span></span>

## <span data-ttu-id="c1df4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1df4-109">EXAMPLES</span></span>

### <span data-ttu-id="c1df4-110">Beispiel 1: Aktualisieren eines mitglieds</span><span class="sxs-lookup"><span data-stu-id="c1df4-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c1df4-111">Mit diesem Befehl wird ein ben-Member aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c1df4-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="c1df4-112">Beispiel 2: Aktualisieren eines mitglieds</span><span class="sxs-lookup"><span data-stu-id="c1df4-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c1df4-113">Mit diesem Befehl wird ein ben-Member aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c1df4-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="c1df4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1df4-114">PARAMETERS</span></span>

### <span data-ttu-id="c1df4-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="c1df4-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="c1df4-116">Legt das Kennwort für das Verwaltungskonto des Managed Consortiums fest.</span><span class="sxs-lookup"><span data-stu-id="c1df4-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="c1df4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1df4-117">-DefaultProfile</span></span>
<span data-ttu-id="c1df4-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1df4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1df4-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="c1df4-119">-FirewallRule</span></span>
<span data-ttu-id="c1df4-120">Ruft die Firewallregeln ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="c1df4-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="c1df4-121">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c1df4-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="c1df4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1df4-122">-InputObject</span></span>
<span data-ttu-id="c1df4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c1df4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1df4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c1df4-124">-Name</span></span>
<span data-ttu-id="c1df4-125">Name des Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="c1df4-125">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1df4-126">-Password</span><span class="sxs-lookup"><span data-stu-id="c1df4-126">-Password</span></span>
<span data-ttu-id="c1df4-127">Legt das grundlegende Kennwort für den Transaktionsknoten-DNS-Endpunkt fest.</span><span class="sxs-lookup"><span data-stu-id="c1df4-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="c1df4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1df4-128">-ResourceGroupName</span></span>
<span data-ttu-id="c1df4-129">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c1df4-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c1df4-130">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="c1df4-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c1df4-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1df4-131">-SubscriptionId</span></span>
<span data-ttu-id="c1df4-132">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c1df4-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c1df4-133">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="c1df4-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c1df4-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1df4-134">-Tag</span></span>
<span data-ttu-id="c1df4-135">Tags des Diensts, bei dem es sich um eine Liste von Schlüsselwertpaaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c1df4-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="c1df4-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1df4-136">-Confirm</span></span>
<span data-ttu-id="c1df4-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1df4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1df4-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c1df4-138">-WhatIf</span></span>
<span data-ttu-id="c1df4-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1df4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1df4-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1df4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1df4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1df4-141">CommonParameters</span></span>
<span data-ttu-id="c1df4-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1df4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1df4-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1df4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1df4-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1df4-144">INPUTS</span></span>

### <span data-ttu-id="c1df4-145">Microsoft.Azure.PowerShell.Cmdlets.Essel.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="c1df4-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="c1df4-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1df4-146">OUTPUTS</span></span>

### <span data-ttu-id="c1df4-147">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="c1df4-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="c1df4-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c1df4-148">NOTES</span></span>

<span data-ttu-id="c1df4-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c1df4-149">ALIASES</span></span>

<span data-ttu-id="c1df4-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c1df4-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c1df4-151">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c1df4-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c1df4-152">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c1df4-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c1df4-153">FIREWALLRULE <IFirewallRule[]>: Ruft die Firewallregeln ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="c1df4-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="c1df4-154">`[EndIPAddress <String>]`: Ruft die End-IP-Adresse des Firewallregelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="c1df4-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="c1df4-155">`[RuleName <String>]`: Ruft den Namen der Firewallregeln ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="c1df4-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="c1df4-156">`[StartIPAddress <String>]`: Ruft die Start-IP-Adresse des Firewallregelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="c1df4-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="c1df4-157">INPUTOBJECT <IBlockchainIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="c1df4-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c1df4-158">`[BlockchainMemberName <String>]`: Name eines Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="c1df4-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="c1df4-159">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="c1df4-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c1df4-160">`[Location <String>]`: Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="c1df4-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="c1df4-161">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="c1df4-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="c1df4-162">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c1df4-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c1df4-163">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="c1df4-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c1df4-164">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c1df4-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="c1df4-165">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="c1df4-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="c1df4-166">`[TransactionNodeName <String>]`: Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="c1df4-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="c1df4-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c1df4-167">RELATED LINKS</span></span>

