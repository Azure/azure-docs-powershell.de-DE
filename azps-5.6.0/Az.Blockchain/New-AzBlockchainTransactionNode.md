---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: 78d3d6449eb5a487c6c4a8a60a732c30fa502600
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925176"
---
# <span data-ttu-id="388c2-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="388c2-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="388c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="388c2-102">SYNOPSIS</span></span>
<span data-ttu-id="388c2-103">Erstellen oder Aktualisieren des Transaktionsknotens</span><span class="sxs-lookup"><span data-stu-id="388c2-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="388c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="388c2-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="388c2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="388c2-105">DESCRIPTION</span></span>
<span data-ttu-id="388c2-106">Erstellen oder Aktualisieren des Transaktionsknotens</span><span class="sxs-lookup"><span data-stu-id="388c2-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="388c2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="388c2-107">EXAMPLES</span></span>

### <span data-ttu-id="388c2-108">Beispiel 1: Erstellen eines Transaktionsknotens für die Blockkette</span><span class="sxs-lookup"><span data-stu-id="388c2-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="388c2-109">Mit diesem Befehl wird ein Transaktionsknoten für die Blockkette erstellt.</span><span class="sxs-lookup"><span data-stu-id="388c2-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="388c2-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="388c2-110">PARAMETERS</span></span>

### <span data-ttu-id="388c2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="388c2-111">-AsJob</span></span>
<span data-ttu-id="388c2-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="388c2-112">Run the command as a job</span></span>

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

### <span data-ttu-id="388c2-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="388c2-113">-BlockchainMemberName</span></span>
<span data-ttu-id="388c2-114">Name des Mitgliedes der Blockkette.</span><span class="sxs-lookup"><span data-stu-id="388c2-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="388c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388c2-115">-DefaultProfile</span></span>
<span data-ttu-id="388c2-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="388c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="388c2-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="388c2-117">-FirewallRule</span></span>
<span data-ttu-id="388c2-118">Ruft die Firewallregeln ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="388c2-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="388c2-119">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu FIREWALLRULE-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="388c2-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="388c2-120">-Location</span><span class="sxs-lookup"><span data-stu-id="388c2-120">-Location</span></span>
<span data-ttu-id="388c2-121">Ruft den Speicherort des Transaktionsknotens ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="388c2-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="388c2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="388c2-122">-Name</span></span>
<span data-ttu-id="388c2-123">Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="388c2-123">Transaction node name.</span></span>

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

### <span data-ttu-id="388c2-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="388c2-124">-NoWait</span></span>
<span data-ttu-id="388c2-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="388c2-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="388c2-126">-Password</span><span class="sxs-lookup"><span data-stu-id="388c2-126">-Password</span></span>
<span data-ttu-id="388c2-127">Legt das grundlegende Authentifizierungskennwort für den Transaktionsknoten-DNS-Endpunkt fest.</span><span class="sxs-lookup"><span data-stu-id="388c2-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="388c2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="388c2-128">-ResourceGroupName</span></span>
<span data-ttu-id="388c2-129">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="388c2-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="388c2-130">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="388c2-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="388c2-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="388c2-131">-SubscriptionId</span></span>
<span data-ttu-id="388c2-132">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="388c2-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="388c2-133">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="388c2-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="388c2-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="388c2-134">-Confirm</span></span>
<span data-ttu-id="388c2-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="388c2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="388c2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="388c2-136">-WhatIf</span></span>
<span data-ttu-id="388c2-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="388c2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="388c2-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="388c2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="388c2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388c2-139">CommonParameters</span></span>
<span data-ttu-id="388c2-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="388c2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388c2-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="388c2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388c2-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="388c2-142">INPUTS</span></span>

## <span data-ttu-id="388c2-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="388c2-143">OUTPUTS</span></span>

### <span data-ttu-id="388c2-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="388c2-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="388c2-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="388c2-145">NOTES</span></span>

<span data-ttu-id="388c2-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="388c2-146">ALIASES</span></span>

<span data-ttu-id="388c2-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="388c2-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="388c2-148">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="388c2-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="388c2-149">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="388c2-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="388c2-150">FIREWALLRULE <IFirewallRule[]>: Ruft die Firewallregeln ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="388c2-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="388c2-151">`[EndIPAddress <String>]`: Ruft die End-IP-Adresse des Firewallregelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="388c2-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="388c2-152">`[RuleName <String>]`: Ruft den Namen der Firewallregeln ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="388c2-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="388c2-153">`[StartIPAddress <String>]`: Ruft die Start-IP-Adresse des Firewallregelbereichs ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="388c2-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="388c2-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="388c2-154">RELATED LINKS</span></span>

