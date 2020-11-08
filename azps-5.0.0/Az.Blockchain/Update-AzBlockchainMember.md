---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176624"
---
# <span data-ttu-id="7b57a-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="7b57a-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="7b57a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b57a-102">SYNOPSIS</span></span>
<span data-ttu-id="7b57a-103">Aktualisieren eines blockchain-Mitglieds</span><span class="sxs-lookup"><span data-stu-id="7b57a-103">Update a blockchain member.</span></span>

## <span data-ttu-id="7b57a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b57a-104">SYNTAX</span></span>

### <span data-ttu-id="7b57a-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="7b57a-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7b57a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7b57a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7b57a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b57a-107">DESCRIPTION</span></span>
<span data-ttu-id="7b57a-108">Aktualisieren eines blockchain-Mitglieds</span><span class="sxs-lookup"><span data-stu-id="7b57a-108">Update a blockchain member.</span></span>

## <span data-ttu-id="7b57a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b57a-109">EXAMPLES</span></span>

### <span data-ttu-id="7b57a-110">Beispiel 1: Aktualisieren eines blockchain-Mitglieds</span><span class="sxs-lookup"><span data-stu-id="7b57a-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="7b57a-111">Mit diesem Befehl wird ein blockchain-Mitglied aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7b57a-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="7b57a-112">Beispiel 2: Aktualisieren eines blockchain-Mitglieds</span><span class="sxs-lookup"><span data-stu-id="7b57a-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="7b57a-113">Mit diesem Befehl wird ein blockchain-Mitglied aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7b57a-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="7b57a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b57a-114">PARAMETERS</span></span>

### <span data-ttu-id="7b57a-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="7b57a-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="7b57a-116">Legt das Kennwort des verwalteten Consortium-Verwaltungskontos fest.</span><span class="sxs-lookup"><span data-stu-id="7b57a-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="7b57a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b57a-117">-DefaultProfile</span></span>
<span data-ttu-id="7b57a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b57a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b57a-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="7b57a-119">-FirewallRule</span></span>
<span data-ttu-id="7b57a-120">Ruft die Firewallregeln ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="7b57a-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="7b57a-121">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für FIREWALLRULE-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7b57a-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="7b57a-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7b57a-122">-InputObject</span></span>
<span data-ttu-id="7b57a-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7b57a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7b57a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7b57a-124">-Name</span></span>
<span data-ttu-id="7b57a-125">Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="7b57a-125">Blockchain member name.</span></span>

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

### <span data-ttu-id="7b57a-126">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="7b57a-126">-Password</span></span>
<span data-ttu-id="7b57a-127">Legt das Kennwort für den Transaktions Knoten-DNS-Endpunkt Basic Auth fest.</span><span class="sxs-lookup"><span data-stu-id="7b57a-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="7b57a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b57a-128">-ResourceGroupName</span></span>
<span data-ttu-id="7b57a-129">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="7b57a-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7b57a-130">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="7b57a-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7b57a-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7b57a-131">-SubscriptionId</span></span>
<span data-ttu-id="7b57a-132">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7b57a-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7b57a-133">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7b57a-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7b57a-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b57a-134">-Tag</span></span>
<span data-ttu-id="7b57a-135">Tags des Diensts, bei denen es sich um eine Liste von Schlüsselwert Paaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7b57a-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="7b57a-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7b57a-136">-Confirm</span></span>
<span data-ttu-id="7b57a-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b57a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b57a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b57a-138">-WhatIf</span></span>
<span data-ttu-id="7b57a-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b57a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b57a-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b57a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b57a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b57a-141">CommonParameters</span></span>
<span data-ttu-id="7b57a-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b57a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b57a-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b57a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b57a-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b57a-144">INPUTS</span></span>

### <span data-ttu-id="7b57a-145">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="7b57a-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="7b57a-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b57a-146">OUTPUTS</span></span>

### <span data-ttu-id="7b57a-147">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="7b57a-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="7b57a-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b57a-148">NOTES</span></span>

<span data-ttu-id="7b57a-149">Aliase</span><span class="sxs-lookup"><span data-stu-id="7b57a-149">ALIASES</span></span>

<span data-ttu-id="7b57a-150">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b57a-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7b57a-151">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7b57a-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b57a-152">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="7b57a-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7b57a-153">FIREWALLRULE <IFirewallRule [] >: Ruft die Firewallregeln ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="7b57a-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="7b57a-154">`[EndIPAddress <String>]`: Ruft die End-IP-Adresse des Firewall-Regelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="7b57a-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="7b57a-155">`[RuleName <String>]`: Ruft den Namen der Firewallregeln ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="7b57a-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="7b57a-156">`[StartIPAddress <String>]`: Ruft die Start-IP-Adresse des Firewall-Regelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="7b57a-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="7b57a-157">Inputobject <IBlockchainIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="7b57a-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7b57a-158">`[BlockchainMemberName <String>]`: Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="7b57a-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="7b57a-159">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="7b57a-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7b57a-160">`[Location <String>]`: Standortname.</span><span class="sxs-lookup"><span data-stu-id="7b57a-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="7b57a-161">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="7b57a-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="7b57a-162">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="7b57a-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7b57a-163">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="7b57a-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7b57a-164">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7b57a-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="7b57a-165">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7b57a-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="7b57a-166">`[TransactionNodeName <String>]`: Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="7b57a-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="7b57a-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b57a-167">RELATED LINKS</span></span>

