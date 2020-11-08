---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179748"
---
# <span data-ttu-id="7817b-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="7817b-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="7817b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7817b-102">SYNOPSIS</span></span>
<span data-ttu-id="7817b-103">Erstellen oder Aktualisieren des Transaktions Knotens</span><span class="sxs-lookup"><span data-stu-id="7817b-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="7817b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7817b-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7817b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7817b-105">DESCRIPTION</span></span>
<span data-ttu-id="7817b-106">Erstellen oder Aktualisieren des Transaktions Knotens</span><span class="sxs-lookup"><span data-stu-id="7817b-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="7817b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7817b-107">EXAMPLES</span></span>

### <span data-ttu-id="7817b-108">Beispiel 1: Erstellen eines blockchain-Transaktions Knotens</span><span class="sxs-lookup"><span data-stu-id="7817b-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="7817b-109">Mit diesem Befehl wird ein blockchain-Transaktions Knoten erstellt.</span><span class="sxs-lookup"><span data-stu-id="7817b-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="7817b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7817b-110">PARAMETERS</span></span>

### <span data-ttu-id="7817b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7817b-111">-AsJob</span></span>
<span data-ttu-id="7817b-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="7817b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="7817b-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="7817b-113">-BlockchainMemberName</span></span>
<span data-ttu-id="7817b-114">Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="7817b-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="7817b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7817b-115">-DefaultProfile</span></span>
<span data-ttu-id="7817b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7817b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7817b-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="7817b-117">-FirewallRule</span></span>
<span data-ttu-id="7817b-118">Ruft die Firewallregeln ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="7817b-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="7817b-119">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für FIREWALLRULE-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7817b-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="7817b-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="7817b-120">-Location</span></span>
<span data-ttu-id="7817b-121">Ruft die Position des Transaktions Knotens ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="7817b-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="7817b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7817b-122">-Name</span></span>
<span data-ttu-id="7817b-123">Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="7817b-123">Transaction node name.</span></span>

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

### <span data-ttu-id="7817b-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7817b-124">-NoWait</span></span>
<span data-ttu-id="7817b-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="7817b-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7817b-126">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="7817b-126">-Password</span></span>
<span data-ttu-id="7817b-127">Legt das Kennwort für den Transaktions Knoten-DNS-Endpunkt Basic Auth fest.</span><span class="sxs-lookup"><span data-stu-id="7817b-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="7817b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7817b-128">-ResourceGroupName</span></span>
<span data-ttu-id="7817b-129">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="7817b-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7817b-130">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="7817b-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7817b-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7817b-131">-SubscriptionId</span></span>
<span data-ttu-id="7817b-132">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7817b-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7817b-133">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7817b-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7817b-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7817b-134">-Confirm</span></span>
<span data-ttu-id="7817b-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7817b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7817b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7817b-136">-WhatIf</span></span>
<span data-ttu-id="7817b-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7817b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7817b-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7817b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7817b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7817b-139">CommonParameters</span></span>
<span data-ttu-id="7817b-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7817b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7817b-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7817b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7817b-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7817b-142">INPUTS</span></span>

## <span data-ttu-id="7817b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7817b-143">OUTPUTS</span></span>

### <span data-ttu-id="7817b-144">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="7817b-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="7817b-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="7817b-145">NOTES</span></span>

<span data-ttu-id="7817b-146">Aliase</span><span class="sxs-lookup"><span data-stu-id="7817b-146">ALIASES</span></span>

<span data-ttu-id="7817b-147">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7817b-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7817b-148">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7817b-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7817b-149">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="7817b-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7817b-150">FIREWALLRULE <IFirewallRule [] >: Ruft die Firewallregeln ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="7817b-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="7817b-151">`[EndIPAddress <String>]`: Ruft die End-IP-Adresse des Firewall-Regelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="7817b-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="7817b-152">`[RuleName <String>]`: Ruft den Namen der Firewallregeln ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="7817b-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="7817b-153">`[StartIPAddress <String>]`: Ruft die Start-IP-Adresse des Firewall-Regelbereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="7817b-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="7817b-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7817b-154">RELATED LINKS</span></span>

