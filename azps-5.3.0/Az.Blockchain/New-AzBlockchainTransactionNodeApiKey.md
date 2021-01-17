---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471057"
---
# <span data-ttu-id="906f2-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="906f2-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="906f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="906f2-102">SYNOPSIS</span></span>
<span data-ttu-id="906f2-103">Generieren Sie die API-Schlüssel für das Mitglied erneut.</span><span class="sxs-lookup"><span data-stu-id="906f2-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="906f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="906f2-104">SYNTAX</span></span>

### <span data-ttu-id="906f2-105">RegenerateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="906f2-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="906f2-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="906f2-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="906f2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="906f2-107">DESCRIPTION</span></span>
<span data-ttu-id="906f2-108">Generieren Sie die API-Schlüssel für das Mitglied erneut.</span><span class="sxs-lookup"><span data-stu-id="906f2-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="906f2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="906f2-109">EXAMPLES</span></span>

### <span data-ttu-id="906f2-110">Beispiel 1: Neuer generieren Sie die API-Schlüssel für einen Transaktionsknoten mithilfe des Namens.</span><span class="sxs-lookup"><span data-stu-id="906f2-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="906f2-111">Dieser Befehl generiert mithilfe von Name, Ressourcengruppe API-Schlüssel für einen Transaktionsknoten.</span><span class="sxs-lookup"><span data-stu-id="906f2-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="906f2-112">Beispiel 2: Neuer generieren von API-Schlüsseln für einen Transaktionsknoten</span><span class="sxs-lookup"><span data-stu-id="906f2-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="906f2-113">Dieser Befehl generiert mithilfe von idenity api keys für einen Transaktionsknoten.</span><span class="sxs-lookup"><span data-stu-id="906f2-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="906f2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="906f2-114">PARAMETERS</span></span>

### <span data-ttu-id="906f2-115">-DestemberName</span><span class="sxs-lookup"><span data-stu-id="906f2-115">-BlockchainMemberName</span></span>
<span data-ttu-id="906f2-116">Name des Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="906f2-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="906f2-117">-DefaultProfile</span></span>
<span data-ttu-id="906f2-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="906f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="906f2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="906f2-119">-InputObject</span></span>
<span data-ttu-id="906f2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="906f2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="906f2-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="906f2-121">-KeyName</span></span>
<span data-ttu-id="906f2-122">Ruft den Namen des API-Schlüssels ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="906f2-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="906f2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="906f2-123">-ResourceGroupName</span></span>
<span data-ttu-id="906f2-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="906f2-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="906f2-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="906f2-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f2-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="906f2-126">-SubscriptionId</span></span>
<span data-ttu-id="906f2-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="906f2-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="906f2-128">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="906f2-128">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f2-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="906f2-129">-TransactionNodeName</span></span>
<span data-ttu-id="906f2-130">Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="906f2-130">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="906f2-131">-Value</span><span class="sxs-lookup"><span data-stu-id="906f2-131">-Value</span></span>
<span data-ttu-id="906f2-132">Ruft den Wert des API-Schlüssels ab oder legt den Wert fest.</span><span class="sxs-lookup"><span data-stu-id="906f2-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="906f2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="906f2-133">-Confirm</span></span>
<span data-ttu-id="906f2-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="906f2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="906f2-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="906f2-135">-WhatIf</span></span>
<span data-ttu-id="906f2-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="906f2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="906f2-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="906f2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="906f2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="906f2-138">CommonParameters</span></span>
<span data-ttu-id="906f2-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="906f2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="906f2-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="906f2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="906f2-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="906f2-141">INPUTS</span></span>

### <span data-ttu-id="906f2-142">Microsoft.Azure.PowerShell.Cmdlets.Essel.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="906f2-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="906f2-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="906f2-143">OUTPUTS</span></span>

### <span data-ttu-id="906f2-144">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="906f2-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="906f2-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="906f2-145">NOTES</span></span>

<span data-ttu-id="906f2-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="906f2-146">ALIASES</span></span>

<span data-ttu-id="906f2-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="906f2-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="906f2-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="906f2-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="906f2-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="906f2-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="906f2-150">INPUTOBJECT <IBlockchainIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="906f2-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="906f2-151">`[BlockchainMemberName <String>]`: Name eines Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="906f2-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="906f2-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="906f2-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="906f2-153">`[Location <String>]`: Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="906f2-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="906f2-154">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="906f2-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="906f2-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="906f2-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="906f2-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="906f2-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="906f2-157">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="906f2-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="906f2-158">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="906f2-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="906f2-159">`[TransactionNodeName <String>]`: Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="906f2-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="906f2-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="906f2-160">RELATED LINKS</span></span>

