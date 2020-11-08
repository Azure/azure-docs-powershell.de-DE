---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010252"
---
# <span data-ttu-id="e5c14-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="e5c14-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="e5c14-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5c14-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c14-103">Aktualisieren des Transaktions Knotens</span><span class="sxs-lookup"><span data-stu-id="e5c14-103">Update the transaction node.</span></span>

## <span data-ttu-id="e5c14-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5c14-104">SYNTAX</span></span>

### <span data-ttu-id="e5c14-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5c14-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e5c14-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e5c14-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e5c14-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5c14-107">DESCRIPTION</span></span>
<span data-ttu-id="e5c14-108">Aktualisieren des Transaktions Knotens</span><span class="sxs-lookup"><span data-stu-id="e5c14-108">Update the transaction node.</span></span>

## <span data-ttu-id="e5c14-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5c14-109">EXAMPLES</span></span>

### <span data-ttu-id="e5c14-110">Beispiel 1: Aktualisieren eines Transkations-Knotens</span><span class="sxs-lookup"><span data-stu-id="e5c14-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="e5c14-111">Mit diesem Befehl wird ein Transaktions Knoten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e5c14-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="e5c14-112">Beispiel 2: Aktualisieren eines Transkations-Knotens</span><span class="sxs-lookup"><span data-stu-id="e5c14-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="e5c14-113">Mit diesem Befehl wird ein Transaktions Knoten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e5c14-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="e5c14-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5c14-114">PARAMETERS</span></span>

### <span data-ttu-id="e5c14-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="e5c14-115">-BlockchainMemberName</span></span>
<span data-ttu-id="e5c14-116">Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="e5c14-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="e5c14-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c14-117">-DefaultProfile</span></span>
<span data-ttu-id="e5c14-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5c14-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5c14-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5c14-119">-FirewallRule</span></span>
<span data-ttu-id="e5c14-120">Ruft die Firewallregeln ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e5c14-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="e5c14-121">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für FIREWALLRULE-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e5c14-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e5c14-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e5c14-122">-InputObject</span></span>
<span data-ttu-id="e5c14-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e5c14-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e5c14-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e5c14-124">-Name</span></span>
<span data-ttu-id="e5c14-125">Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="e5c14-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c14-126">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="e5c14-126">-Password</span></span>
<span data-ttu-id="e5c14-127">Legt das Kennwort für den Transaktions Knoten-DNS-Endpunkt Basic Auth fest.</span><span class="sxs-lookup"><span data-stu-id="e5c14-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="e5c14-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c14-128">-ResourceGroupName</span></span>
<span data-ttu-id="e5c14-129">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="e5c14-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e5c14-130">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="e5c14-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e5c14-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e5c14-131">-SubscriptionId</span></span>
<span data-ttu-id="e5c14-132">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e5c14-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e5c14-133">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="e5c14-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e5c14-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5c14-134">-Confirm</span></span>
<span data-ttu-id="e5c14-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5c14-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5c14-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5c14-136">-WhatIf</span></span>
<span data-ttu-id="e5c14-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5c14-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5c14-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5c14-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5c14-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c14-139">CommonParameters</span></span>
<span data-ttu-id="e5c14-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c14-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c14-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5c14-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c14-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5c14-142">INPUTS</span></span>

### <span data-ttu-id="e5c14-143">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="e5c14-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="e5c14-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5c14-144">OUTPUTS</span></span>

### <span data-ttu-id="e5c14-145">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="e5c14-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="e5c14-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5c14-146">NOTES</span></span>

<span data-ttu-id="e5c14-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="e5c14-147">ALIASES</span></span>

<span data-ttu-id="e5c14-148">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5c14-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e5c14-149">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e5c14-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e5c14-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="e5c14-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e5c14-151">FIREWALLRULE <IFirewallRule [] >: Ruft die Firewallregeln ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e5c14-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="e5c14-152">`[EndIPAddress <String>]`: Ruft die End-IP-Adresse des Firewall-Regelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e5c14-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="e5c14-153">`[RuleName <String>]`: Ruft den Namen der Firewallregeln ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="e5c14-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="e5c14-154">`[StartIPAddress <String>]`: Ruft die Start-IP-Adresse des Firewall-Regelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e5c14-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="e5c14-155">Inputobject <IBlockchainIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="e5c14-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e5c14-156">`[BlockchainMemberName <String>]`: Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="e5c14-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="e5c14-157">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="e5c14-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e5c14-158">`[Location <String>]`: Standortname.</span><span class="sxs-lookup"><span data-stu-id="e5c14-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="e5c14-159">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="e5c14-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="e5c14-160">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="e5c14-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e5c14-161">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="e5c14-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e5c14-162">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e5c14-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="e5c14-163">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="e5c14-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="e5c14-164">`[TransactionNodeName <String>]`: Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="e5c14-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="e5c14-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5c14-165">RELATED LINKS</span></span>

