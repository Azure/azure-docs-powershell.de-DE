---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363192"
---
# <span data-ttu-id="753c5-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="753c5-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="753c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="753c5-102">SYNOPSIS</span></span>
<span data-ttu-id="753c5-103">Aktualisieren Sie den Transaktionsknoten.</span><span class="sxs-lookup"><span data-stu-id="753c5-103">Update the transaction node.</span></span>

## <span data-ttu-id="753c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="753c5-104">SYNTAX</span></span>

### <span data-ttu-id="753c5-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="753c5-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="753c5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="753c5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="753c5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="753c5-107">DESCRIPTION</span></span>
<span data-ttu-id="753c5-108">Aktualisieren Sie den Transaktionsknoten.</span><span class="sxs-lookup"><span data-stu-id="753c5-108">Update the transaction node.</span></span>

## <span data-ttu-id="753c5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="753c5-109">EXAMPLES</span></span>

### <span data-ttu-id="753c5-110">Beispiel 1: Aktualisieren eines Transcationknotens</span><span class="sxs-lookup"><span data-stu-id="753c5-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="753c5-111">Mit diesem Befehl wird ein Transaktionsknoten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="753c5-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="753c5-112">Beispiel 2: Aktualisieren eines Transcationknotens</span><span class="sxs-lookup"><span data-stu-id="753c5-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="753c5-113">Mit diesem Befehl wird ein Transaktionsknoten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="753c5-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="753c5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="753c5-114">PARAMETERS</span></span>

### <span data-ttu-id="753c5-115">-DestemberName</span><span class="sxs-lookup"><span data-stu-id="753c5-115">-BlockchainMemberName</span></span>
<span data-ttu-id="753c5-116">Name des Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="753c5-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="753c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="753c5-117">-DefaultProfile</span></span>
<span data-ttu-id="753c5-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="753c5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="753c5-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="753c5-119">-FirewallRule</span></span>
<span data-ttu-id="753c5-120">Ruft die Firewallregeln ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="753c5-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="753c5-121">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="753c5-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="753c5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="753c5-122">-InputObject</span></span>
<span data-ttu-id="753c5-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="753c5-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="753c5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="753c5-124">-Name</span></span>
<span data-ttu-id="753c5-125">Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="753c5-125">Transaction node name.</span></span>

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

### <span data-ttu-id="753c5-126">-Password</span><span class="sxs-lookup"><span data-stu-id="753c5-126">-Password</span></span>
<span data-ttu-id="753c5-127">Legt das grundlegende Kennwort für den Transaktionsknoten-DNS-Endpunkt fest.</span><span class="sxs-lookup"><span data-stu-id="753c5-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="753c5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="753c5-128">-ResourceGroupName</span></span>
<span data-ttu-id="753c5-129">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="753c5-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="753c5-130">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="753c5-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="753c5-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="753c5-131">-SubscriptionId</span></span>
<span data-ttu-id="753c5-132">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="753c5-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="753c5-133">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="753c5-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="753c5-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="753c5-134">-Confirm</span></span>
<span data-ttu-id="753c5-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="753c5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="753c5-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="753c5-136">-WhatIf</span></span>
<span data-ttu-id="753c5-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="753c5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="753c5-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="753c5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="753c5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="753c5-139">CommonParameters</span></span>
<span data-ttu-id="753c5-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="753c5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="753c5-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="753c5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="753c5-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="753c5-142">INPUTS</span></span>

### <span data-ttu-id="753c5-143">Microsoft.Azure.PowerShell.Cmdlets.Essel.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="753c5-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="753c5-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="753c5-144">OUTPUTS</span></span>

### <span data-ttu-id="753c5-145">Microsoft.Azure.PowerShell.Cmdlets.Deser.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="753c5-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="753c5-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="753c5-146">NOTES</span></span>

<span data-ttu-id="753c5-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="753c5-147">ALIASES</span></span>

<span data-ttu-id="753c5-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="753c5-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="753c5-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="753c5-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="753c5-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="753c5-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="753c5-151">FIREWALLRULE <IFirewallRule[]>: Ruft die Firewallregeln ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="753c5-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="753c5-152">`[EndIPAddress <String>]`: Ruft die End-IP-Adresse des Firewallregelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="753c5-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="753c5-153">`[RuleName <String>]`: Ruft den Namen der Firewallregeln ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="753c5-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="753c5-154">`[StartIPAddress <String>]`: Ruft die Start-IP-Adresse des Firewallregelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="753c5-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="753c5-155">INPUTOBJECT <IBlockchainIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="753c5-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="753c5-156">`[BlockchainMemberName <String>]`: Name eines Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="753c5-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="753c5-157">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="753c5-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="753c5-158">`[Location <String>]`: Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="753c5-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="753c5-159">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="753c5-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="753c5-160">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="753c5-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="753c5-161">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="753c5-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="753c5-162">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="753c5-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="753c5-163">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="753c5-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="753c5-164">`[TransactionNodeName <String>]`: Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="753c5-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="753c5-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="753c5-165">RELATED LINKS</span></span>

