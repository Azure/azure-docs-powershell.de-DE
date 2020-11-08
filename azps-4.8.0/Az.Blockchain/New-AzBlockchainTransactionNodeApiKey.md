---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009364"
---
# <span data-ttu-id="a316c-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="a316c-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="a316c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a316c-102">SYNOPSIS</span></span>
<span data-ttu-id="a316c-103">Generieren Sie die API-Schlüssel für das blockchain-Mitglied neu.</span><span class="sxs-lookup"><span data-stu-id="a316c-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="a316c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a316c-104">SYNTAX</span></span>

### <span data-ttu-id="a316c-105">RegenerateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a316c-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a316c-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a316c-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a316c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a316c-107">DESCRIPTION</span></span>
<span data-ttu-id="a316c-108">Generieren Sie die API-Schlüssel für das blockchain-Mitglied neu.</span><span class="sxs-lookup"><span data-stu-id="a316c-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="a316c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a316c-109">EXAMPLES</span></span>

### <span data-ttu-id="a316c-110">Beispiel 1: Erneutes Generieren von API-Schlüsseln für einen Transaktions Knoten mithilfe von Name.</span><span class="sxs-lookup"><span data-stu-id="a316c-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="a316c-111">Dieser Befehl generiert API-Schlüssel für einen Transaktions Knoten unter Verwendung von Name, Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a316c-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="a316c-112">Beispiel 2: Erneutes Generieren von API-Schlüsseln für einen Transaktions Knoten</span><span class="sxs-lookup"><span data-stu-id="a316c-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="a316c-113">Dieser Befehl generiert API-Schlüssel für einen Transaktions Knoten mithilfe von idenity.</span><span class="sxs-lookup"><span data-stu-id="a316c-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="a316c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a316c-114">PARAMETERS</span></span>

### <span data-ttu-id="a316c-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="a316c-115">-BlockchainMemberName</span></span>
<span data-ttu-id="a316c-116">Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="a316c-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="a316c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a316c-117">-DefaultProfile</span></span>
<span data-ttu-id="a316c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a316c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a316c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a316c-119">-InputObject</span></span>
<span data-ttu-id="a316c-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a316c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a316c-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a316c-121">-KeyName</span></span>
<span data-ttu-id="a316c-122">Ruft den Namen des API-Schlüssels ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="a316c-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="a316c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a316c-123">-ResourceGroupName</span></span>
<span data-ttu-id="a316c-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a316c-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a316c-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="a316c-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a316c-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a316c-126">-SubscriptionId</span></span>
<span data-ttu-id="a316c-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a316c-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a316c-128">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a316c-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a316c-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="a316c-129">-TransactionNodeName</span></span>
<span data-ttu-id="a316c-130">Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="a316c-130">Transaction node name.</span></span>

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

### <span data-ttu-id="a316c-131">-Wert</span><span class="sxs-lookup"><span data-stu-id="a316c-131">-Value</span></span>
<span data-ttu-id="a316c-132">Ruft den API-Schlüsselwert ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="a316c-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="a316c-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a316c-133">-Confirm</span></span>
<span data-ttu-id="a316c-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a316c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a316c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a316c-135">-WhatIf</span></span>
<span data-ttu-id="a316c-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a316c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a316c-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a316c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a316c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a316c-138">CommonParameters</span></span>
<span data-ttu-id="a316c-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a316c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a316c-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a316c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a316c-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a316c-141">INPUTS</span></span>

### <span data-ttu-id="a316c-142">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="a316c-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="a316c-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a316c-143">OUTPUTS</span></span>

### <span data-ttu-id="a316c-144">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="a316c-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="a316c-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="a316c-145">NOTES</span></span>

<span data-ttu-id="a316c-146">Aliase</span><span class="sxs-lookup"><span data-stu-id="a316c-146">ALIASES</span></span>

<span data-ttu-id="a316c-147">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a316c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a316c-148">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a316c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a316c-149">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a316c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a316c-150">Inputobject <IBlockchainIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a316c-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a316c-151">`[BlockchainMemberName <String>]`: Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="a316c-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="a316c-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a316c-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a316c-153">`[Location <String>]`: Standortname.</span><span class="sxs-lookup"><span data-stu-id="a316c-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="a316c-154">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="a316c-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="a316c-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a316c-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a316c-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="a316c-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a316c-157">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a316c-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="a316c-158">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a316c-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="a316c-159">`[TransactionNodeName <String>]`: Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="a316c-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="a316c-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a316c-160">RELATED LINKS</span></span>

