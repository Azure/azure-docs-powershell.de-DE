---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 418786855833164c3f9c15dcd2716ad00c8c6d8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920051"
---
# <span data-ttu-id="c0dd5-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="c0dd5-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="c0dd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="c0dd5-103">Regenerieren Sie die API-Schlüssel für das Element für die Blockierkette.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="c0dd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0dd5-104">SYNTAX</span></span>

### <span data-ttu-id="c0dd5-105">RegenerateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c0dd5-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c0dd5-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c0dd5-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c0dd5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0dd5-107">DESCRIPTION</span></span>
<span data-ttu-id="c0dd5-108">Regenerieren Sie die API-Schlüssel für das Element für die Blockierkette.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="c0dd5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c0dd5-109">EXAMPLES</span></span>

### <span data-ttu-id="c0dd5-110">Beispiel 1: Neu generieren von Api-Schlüsseln für einen Transaktionsknoten mithilfe des Namens.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="c0dd5-111">Mit diesem Befehl werden api keys für einen Transaktionsknoten mithilfe von Name, Ressourcengruppe generiert.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="c0dd5-112">Beispiel 2: Neu generieren von API-Schlüsseln für einen Transaktionsknoten</span><span class="sxs-lookup"><span data-stu-id="c0dd5-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="c0dd5-113">Mit diesem Befehl werden api keys für einen Transaktionsknoten mithilfe von idenity generiert.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="c0dd5-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c0dd5-114">PARAMETERS</span></span>

### <span data-ttu-id="c0dd5-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="c0dd5-115">-BlockchainMemberName</span></span>
<span data-ttu-id="c0dd5-116">Name des Mitgliedes der Blockkette.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="c0dd5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0dd5-117">-DefaultProfile</span></span>
<span data-ttu-id="c0dd5-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0dd5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0dd5-119">-InputObject</span></span>
<span data-ttu-id="c0dd5-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c0dd5-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c0dd5-121">-KeyName</span></span>
<span data-ttu-id="c0dd5-122">Ruft den Namen des API-Schlüssels ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="c0dd5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0dd5-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0dd5-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c0dd5-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c0dd5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0dd5-126">-SubscriptionId</span></span>
<span data-ttu-id="c0dd5-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c0dd5-128">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c0dd5-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="c0dd5-129">-TransactionNodeName</span></span>
<span data-ttu-id="c0dd5-130">Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-130">Transaction node name.</span></span>

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

### <span data-ttu-id="c0dd5-131">-Wert</span><span class="sxs-lookup"><span data-stu-id="c0dd5-131">-Value</span></span>
<span data-ttu-id="c0dd5-132">Ruft den API-Schlüsselwert ab oder legt den Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="c0dd5-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0dd5-133">-Confirm</span></span>
<span data-ttu-id="c0dd5-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0dd5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0dd5-135">-WhatIf</span></span>
<span data-ttu-id="c0dd5-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0dd5-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0dd5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0dd5-138">CommonParameters</span></span>
<span data-ttu-id="c0dd5-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0dd5-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0dd5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0dd5-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c0dd5-141">INPUTS</span></span>

### <span data-ttu-id="c0dd5-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="c0dd5-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="c0dd5-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c0dd5-143">OUTPUTS</span></span>

### <span data-ttu-id="c0dd5-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="c0dd5-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="c0dd5-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c0dd5-145">NOTES</span></span>

<span data-ttu-id="c0dd5-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c0dd5-146">ALIASES</span></span>

<span data-ttu-id="c0dd5-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c0dd5-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c0dd5-148">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c0dd5-149">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c0dd5-150">INPUTOBJECT <IBlockchainIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="c0dd5-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c0dd5-151">`[BlockchainMemberName <String>]`: Name des Mitgliedes der Blockkette.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="c0dd5-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="c0dd5-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c0dd5-153">`[Location <String>]`: Ortsname.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="c0dd5-154">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="c0dd5-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c0dd5-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c0dd5-157">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="c0dd5-158">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="c0dd5-159">`[TransactionNodeName <String>]`: Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="c0dd5-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="c0dd5-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c0dd5-160">RELATED LINKS</span></span>

