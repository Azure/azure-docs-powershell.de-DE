---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: 15af3a6bb7e80020cd014bfbdd8ff944cafd187a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947291"
---
# <span data-ttu-id="dcaab-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="dcaab-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="dcaab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcaab-102">SYNOPSIS</span></span>
<span data-ttu-id="dcaab-103">Erstellen Sie ein Element für die Blockokette.</span><span class="sxs-lookup"><span data-stu-id="dcaab-103">Create a blockchain member.</span></span>

## <span data-ttu-id="dcaab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcaab-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dcaab-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcaab-105">DESCRIPTION</span></span>
<span data-ttu-id="dcaab-106">Erstellen Sie ein Element für die Blockokette.</span><span class="sxs-lookup"><span data-stu-id="dcaab-106">Create a blockchain member.</span></span>

## <span data-ttu-id="dcaab-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dcaab-107">EXAMPLES</span></span>

### <span data-ttu-id="dcaab-108">Beispiel 1: Erstellen eines neuen Mitglieds der Blockkette</span><span class="sxs-lookup"><span data-stu-id="dcaab-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="dcaab-109">Mit diesem Befehl wird ein neues Element für die Blockkette erstellt.</span><span class="sxs-lookup"><span data-stu-id="dcaab-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="dcaab-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dcaab-110">PARAMETERS</span></span>

### <span data-ttu-id="dcaab-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcaab-111">-AsJob</span></span>
<span data-ttu-id="dcaab-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="dcaab-112">Run the command as a job</span></span>

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

### <span data-ttu-id="dcaab-113">-Consortium</span><span class="sxs-lookup"><span data-stu-id="dcaab-113">-Consortium</span></span>
<span data-ttu-id="dcaab-114">Ruft das Consortium für das Mitglied der Blockkette ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="dcaab-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="dcaab-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="dcaab-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="dcaab-116">Legt das Kennwort für das verwaltete Konsortialverwaltungskonto fest.</span><span class="sxs-lookup"><span data-stu-id="dcaab-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="dcaab-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="dcaab-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="dcaab-118">Ruft den Anzeigenamen des Mitglieds im Consortium ab.</span><span class="sxs-lookup"><span data-stu-id="dcaab-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="dcaab-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="dcaab-119">-ConsortiumRole</span></span>
<span data-ttu-id="dcaab-120">Ruft die Rolle des Mitglieds im Consortium ab.</span><span class="sxs-lookup"><span data-stu-id="dcaab-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="dcaab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcaab-121">-DefaultProfile</span></span>
<span data-ttu-id="dcaab-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dcaab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcaab-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="dcaab-123">-FirewallRule</span></span>
<span data-ttu-id="dcaab-124">Ruft Firewallregeln ab oder legt diese fest: Erstellen finden Sie im Abschnitt NOTIZEN für FIREWALLRULE-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dcaab-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="dcaab-125">-Location</span><span class="sxs-lookup"><span data-stu-id="dcaab-125">-Location</span></span>
<span data-ttu-id="dcaab-126">Der GEO-Standort des Blockchain-Diensts.</span><span class="sxs-lookup"><span data-stu-id="dcaab-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="dcaab-127">-Name</span><span class="sxs-lookup"><span data-stu-id="dcaab-127">-Name</span></span>
<span data-ttu-id="dcaab-128">Name des Mitgliedes der Blockkette.</span><span class="sxs-lookup"><span data-stu-id="dcaab-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="dcaab-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dcaab-129">-NoWait</span></span>
<span data-ttu-id="dcaab-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="dcaab-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dcaab-131">-Password</span><span class="sxs-lookup"><span data-stu-id="dcaab-131">-Password</span></span>
<span data-ttu-id="dcaab-132">Legt das grundlegende Authentifizierungskennwort des Elements für die Auth fest.</span><span class="sxs-lookup"><span data-stu-id="dcaab-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="dcaab-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="dcaab-133">-Protocol</span></span>
<span data-ttu-id="dcaab-134">Ruft das Protokoll für die Blockkette ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="dcaab-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="dcaab-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcaab-135">-ResourceGroupName</span></span>
<span data-ttu-id="dcaab-136">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="dcaab-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="dcaab-137">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="dcaab-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="dcaab-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="dcaab-138">-Sku</span></span>
<span data-ttu-id="dcaab-139">Ruft den Namen der Sku ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="dcaab-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="dcaab-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="dcaab-140">-SkuTier</span></span>
<span data-ttu-id="dcaab-141">Ruft die Sku-Ebene ab oder legt sie fest</span><span class="sxs-lookup"><span data-stu-id="dcaab-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="dcaab-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dcaab-142">-SubscriptionId</span></span>
<span data-ttu-id="dcaab-143">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dcaab-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="dcaab-144">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="dcaab-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dcaab-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="dcaab-145">-Tag</span></span>
<span data-ttu-id="dcaab-146">Tags des Diensts, bei dem es sich um eine Liste von Schlüsselwertpaaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="dcaab-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="dcaab-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="dcaab-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="dcaab-148">Ruft die Knotenkapazität ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="dcaab-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="dcaab-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dcaab-149">-Confirm</span></span>
<span data-ttu-id="dcaab-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dcaab-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcaab-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcaab-151">-WhatIf</span></span>
<span data-ttu-id="dcaab-152">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dcaab-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcaab-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dcaab-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcaab-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcaab-154">CommonParameters</span></span>
<span data-ttu-id="dcaab-155">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcaab-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcaab-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcaab-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcaab-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dcaab-157">INPUTS</span></span>

## <span data-ttu-id="dcaab-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dcaab-158">OUTPUTS</span></span>

### <span data-ttu-id="dcaab-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="dcaab-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="dcaab-160">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dcaab-160">NOTES</span></span>

<span data-ttu-id="dcaab-161">ALIASE</span><span class="sxs-lookup"><span data-stu-id="dcaab-161">ALIASES</span></span>

<span data-ttu-id="dcaab-162">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="dcaab-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dcaab-163">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="dcaab-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dcaab-164">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dcaab-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dcaab-165">FIREWALLRULE <IFirewallRule[]>: Ruft Firewallregeln ab oder legt sie fest</span><span class="sxs-lookup"><span data-stu-id="dcaab-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="dcaab-166">`[EndIPAddress <String>]`: Ruft die End-IP-Adresse des Firewallregelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="dcaab-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="dcaab-167">`[RuleName <String>]`: Ruft den Namen der Firewallregeln ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="dcaab-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="dcaab-168">`[StartIPAddress <String>]`: Ruft die Start-IP-Adresse des Firewallregelbereichs ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="dcaab-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="dcaab-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dcaab-169">RELATED LINKS</span></span>

