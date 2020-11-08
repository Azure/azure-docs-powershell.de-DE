---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179750"
---
# <span data-ttu-id="d4d9d-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="d4d9d-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="d4d9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d9d-103">Erstellen Sie ein blockchain-Mitglied.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-103">Create a blockchain member.</span></span>

## <span data-ttu-id="d4d9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4d9d-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d4d9d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4d9d-105">DESCRIPTION</span></span>
<span data-ttu-id="d4d9d-106">Erstellen Sie ein blockchain-Mitglied.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-106">Create a blockchain member.</span></span>

## <span data-ttu-id="d4d9d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4d9d-107">EXAMPLES</span></span>

### <span data-ttu-id="d4d9d-108">Beispiel 1: Erstellen eines neuen blockchain-Mitglieds</span><span class="sxs-lookup"><span data-stu-id="d4d9d-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="d4d9d-109">Dieser Befehl erstellt ein neues blockchain-Mitglied.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="d4d9d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4d9d-110">PARAMETERS</span></span>

### <span data-ttu-id="d4d9d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4d9d-111">-AsJob</span></span>
<span data-ttu-id="d4d9d-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d4d9d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d4d9d-113">-Konsortium</span><span class="sxs-lookup"><span data-stu-id="d4d9d-113">-Consortium</span></span>
<span data-ttu-id="d4d9d-114">Ruft das Konsortium für das blockchain-Element ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="d4d9d-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="d4d9d-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="d4d9d-116">Legt das Kennwort des verwalteten Consortium-Verwaltungskontos fest.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="d4d9d-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="d4d9d-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="d4d9d-118">Ruft den Anzeigenamen des Mitglieds im Konsortium ab.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="d4d9d-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="d4d9d-119">-ConsortiumRole</span></span>
<span data-ttu-id="d4d9d-120">Ruft die Rolle des Mitglieds im Konsortium ab.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="d4d9d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d9d-121">-DefaultProfile</span></span>
<span data-ttu-id="d4d9d-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4d9d-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="d4d9d-123">-FirewallRule</span></span>
<span data-ttu-id="d4d9d-124">Ruft Firewallregeln zum Erstellen ab oder legt diese fest, lesen Sie den Abschnitt "Notizen" für FIREWALLRULE-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="d4d9d-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="d4d9d-125">-Location</span></span>
<span data-ttu-id="d4d9d-126">Der Geo-Speicherort des blockchain-Diensts.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="d4d9d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d4d9d-127">-Name</span></span>
<span data-ttu-id="d4d9d-128">Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="d4d9d-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d4d9d-129">-NoWait</span></span>
<span data-ttu-id="d4d9d-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d4d9d-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d4d9d-131">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="d4d9d-131">-Password</span></span>
<span data-ttu-id="d4d9d-132">Legt das grundlegende Auth-Kennwort des blockchain-Members fest.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="d4d9d-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d4d9d-133">-Protocol</span></span>
<span data-ttu-id="d4d9d-134">Ruft das blockchain-Protokoll ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="d4d9d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4d9d-135">-ResourceGroupName</span></span>
<span data-ttu-id="d4d9d-136">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d4d9d-137">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d4d9d-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="d4d9d-138">-Sku</span></span>
<span data-ttu-id="d4d9d-139">Ruft den SKU-Namen ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="d4d9d-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d4d9d-140">-SkuTier</span></span>
<span data-ttu-id="d4d9d-141">Abrufen oder Festlegen der SKU-Ebene</span><span class="sxs-lookup"><span data-stu-id="d4d9d-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="d4d9d-142">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d4d9d-142">-SubscriptionId</span></span>
<span data-ttu-id="d4d9d-143">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d4d9d-144">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d4d9d-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4d9d-145">-Tag</span></span>
<span data-ttu-id="d4d9d-146">Tags des Diensts, bei denen es sich um eine Liste von Schlüsselwert Paaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="d4d9d-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d4d9d-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="d4d9d-148">Ruft die Kapazität des Knotens ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="d4d9d-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4d9d-149">-Confirm</span></span>
<span data-ttu-id="d4d9d-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4d9d-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4d9d-151">-WhatIf</span></span>
<span data-ttu-id="d4d9d-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4d9d-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4d9d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d9d-154">CommonParameters</span></span>
<span data-ttu-id="d4d9d-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d9d-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4d9d-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d9d-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4d9d-157">INPUTS</span></span>

## <span data-ttu-id="d4d9d-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4d9d-158">OUTPUTS</span></span>

### <span data-ttu-id="d4d9d-159">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="d4d9d-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="d4d9d-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4d9d-160">NOTES</span></span>

<span data-ttu-id="d4d9d-161">Aliase</span><span class="sxs-lookup"><span data-stu-id="d4d9d-161">ALIASES</span></span>

<span data-ttu-id="d4d9d-162">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4d9d-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4d9d-163">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4d9d-164">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4d9d-165">FIREWALLRULE <IFirewallRule [] >: Ruft Firewallregeln ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="d4d9d-166">`[EndIPAddress <String>]`: Ruft die End-IP-Adresse des Firewall-Regelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="d4d9d-167">`[RuleName <String>]`: Ruft den Namen der Firewallregeln ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="d4d9d-168">`[StartIPAddress <String>]`: Ruft die Start-IP-Adresse des Firewall-Regelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="d4d9d-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4d9d-169">RELATED LINKS</span></span>

