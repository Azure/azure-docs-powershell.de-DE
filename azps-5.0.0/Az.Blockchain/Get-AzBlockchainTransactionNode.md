---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179756"
---
# <span data-ttu-id="dc039-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="dc039-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="dc039-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc039-102">SYNOPSIS</span></span>
<span data-ttu-id="dc039-103">Rufen Sie die Details des Transaktions Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="dc039-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="dc039-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc039-104">SYNTAX</span></span>

### <span data-ttu-id="dc039-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc039-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc039-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="dc039-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc039-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc039-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc039-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc039-108">DESCRIPTION</span></span>
<span data-ttu-id="dc039-109">Rufen Sie die Details des Transaktions Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="dc039-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="dc039-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc039-110">EXAMPLES</span></span>

### <span data-ttu-id="dc039-111">Beispiel 1: Auflisten von Transaktions Knoten für ein blockchain-Mitglied</span><span class="sxs-lookup"><span data-stu-id="dc039-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="dc039-112">Dieser Befehl listet Transaktions Knoten für ein blockchain-Element auf.</span><span class="sxs-lookup"><span data-stu-id="dc039-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="dc039-113">Beispiel 2: Abrufen eines Transaktions Knotens</span><span class="sxs-lookup"><span data-stu-id="dc039-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="dc039-114">Dieser Befehl ruft einen Transaktions Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="dc039-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="dc039-115">Beispiel 3: Abrufen eines Transaktions Knotens</span><span class="sxs-lookup"><span data-stu-id="dc039-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="dc039-116">Dieser Befehl ruft einen Transaktions Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="dc039-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="dc039-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc039-117">PARAMETERS</span></span>

### <span data-ttu-id="dc039-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="dc039-118">-BlockchainMemberName</span></span>
<span data-ttu-id="dc039-119">Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="dc039-119">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc039-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc039-120">-DefaultProfile</span></span>
<span data-ttu-id="dc039-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc039-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc039-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dc039-122">-InputObject</span></span>
<span data-ttu-id="dc039-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dc039-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc039-124">-Name</span><span class="sxs-lookup"><span data-stu-id="dc039-124">-Name</span></span>
<span data-ttu-id="dc039-125">Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="dc039-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc039-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc039-126">-ResourceGroupName</span></span>
<span data-ttu-id="dc039-127">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="dc039-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="dc039-128">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="dc039-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc039-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="dc039-129">-SubscriptionId</span></span>
<span data-ttu-id="dc039-130">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dc039-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="dc039-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="dc039-131">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc039-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc039-132">CommonParameters</span></span>
<span data-ttu-id="dc039-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc039-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc039-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc039-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc039-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc039-135">INPUTS</span></span>

### <span data-ttu-id="dc039-136">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="dc039-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="dc039-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc039-137">OUTPUTS</span></span>

### <span data-ttu-id="dc039-138">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="dc039-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="dc039-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc039-139">NOTES</span></span>

<span data-ttu-id="dc039-140">Aliase</span><span class="sxs-lookup"><span data-stu-id="dc039-140">ALIASES</span></span>

<span data-ttu-id="dc039-141">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc039-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc039-142">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc039-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc039-143">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="dc039-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc039-144">Inputobject <IBlockchainIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="dc039-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc039-145">`[BlockchainMemberName <String>]`: Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="dc039-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="dc039-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="dc039-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc039-147">`[Location <String>]`: Standortname.</span><span class="sxs-lookup"><span data-stu-id="dc039-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="dc039-148">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="dc039-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="dc039-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="dc039-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="dc039-150">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="dc039-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="dc039-151">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dc039-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="dc039-152">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="dc039-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="dc039-153">`[TransactionNodeName <String>]`: Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="dc039-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="dc039-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc039-154">RELATED LINKS</span></span>

