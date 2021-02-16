---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145180"
---
# <span data-ttu-id="f03b5-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="f03b5-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="f03b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f03b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f03b5-103">Erstellen oder aktualisieren Sie den Transaktionsknoten.</span><span class="sxs-lookup"><span data-stu-id="f03b5-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="f03b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f03b5-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f03b5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f03b5-105">DESCRIPTION</span></span>
<span data-ttu-id="f03b5-106">Erstellen oder aktualisieren Sie den Transaktionsknoten.</span><span class="sxs-lookup"><span data-stu-id="f03b5-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="f03b5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f03b5-107">EXAMPLES</span></span>

### <span data-ttu-id="f03b5-108">Beispiel 1: Erstellen eines Knotens für eine Transaktion</span><span class="sxs-lookup"><span data-stu-id="f03b5-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="f03b5-109">Mit diesem Befehl wird ein Knoten für eine Transaktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="f03b5-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="f03b5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f03b5-110">PARAMETERS</span></span>

### <span data-ttu-id="f03b5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f03b5-111">-AsJob</span></span>
<span data-ttu-id="f03b5-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f03b5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f03b5-113">-DestemberName</span><span class="sxs-lookup"><span data-stu-id="f03b5-113">-BlockchainMemberName</span></span>
<span data-ttu-id="f03b5-114">Name des Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="f03b5-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="f03b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03b5-115">-DefaultProfile</span></span>
<span data-ttu-id="f03b5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f03b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f03b5-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="f03b5-117">-FirewallRule</span></span>
<span data-ttu-id="f03b5-118">Ruft die Firewallregeln ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="f03b5-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="f03b5-119">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f03b5-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="f03b5-120">-Location</span><span class="sxs-lookup"><span data-stu-id="f03b5-120">-Location</span></span>
<span data-ttu-id="f03b5-121">Ruft den Transaktionsknotenspeicherort ab oder legt den Speicherort fest.</span><span class="sxs-lookup"><span data-stu-id="f03b5-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="f03b5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f03b5-122">-Name</span></span>
<span data-ttu-id="f03b5-123">Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="f03b5-123">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f03b5-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f03b5-124">-NoWait</span></span>
<span data-ttu-id="f03b5-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f03b5-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f03b5-126">-Password</span><span class="sxs-lookup"><span data-stu-id="f03b5-126">-Password</span></span>
<span data-ttu-id="f03b5-127">Legt das grundlegende Kennwort für den Transaktionsknoten-DNS-Endpunkt fest.</span><span class="sxs-lookup"><span data-stu-id="f03b5-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="f03b5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f03b5-128">-ResourceGroupName</span></span>
<span data-ttu-id="f03b5-129">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="f03b5-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f03b5-130">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="f03b5-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f03b5-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f03b5-131">-SubscriptionId</span></span>
<span data-ttu-id="f03b5-132">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f03b5-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f03b5-133">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="f03b5-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f03b5-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f03b5-134">-Confirm</span></span>
<span data-ttu-id="f03b5-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f03b5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f03b5-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f03b5-136">-WhatIf</span></span>
<span data-ttu-id="f03b5-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f03b5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f03b5-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f03b5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f03b5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03b5-139">CommonParameters</span></span>
<span data-ttu-id="f03b5-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f03b5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03b5-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f03b5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03b5-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f03b5-142">INPUTS</span></span>

## <span data-ttu-id="f03b5-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f03b5-143">OUTPUTS</span></span>

### <span data-ttu-id="f03b5-144">Microsoft.Azure.PowerShell.Cmdlets.Deser.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="f03b5-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="f03b5-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f03b5-145">NOTES</span></span>

<span data-ttu-id="f03b5-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f03b5-146">ALIASES</span></span>

<span data-ttu-id="f03b5-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f03b5-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f03b5-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f03b5-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f03b5-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f03b5-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f03b5-150">FIREWALLRULE <IFirewallRule[]>: Ruft die Firewallregeln ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="f03b5-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="f03b5-151">`[EndIPAddress <String>]`: Ruft die End-IP-Adresse des Firewallregelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f03b5-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="f03b5-152">`[RuleName <String>]`: Ruft den Namen der Firewallregeln ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="f03b5-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="f03b5-153">`[StartIPAddress <String>]`: Ruft die Start-IP-Adresse des Firewallregelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f03b5-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="f03b5-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f03b5-154">RELATED LINKS</span></span>

