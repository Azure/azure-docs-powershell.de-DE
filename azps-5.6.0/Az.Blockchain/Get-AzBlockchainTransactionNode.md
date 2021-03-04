---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 53178cf8e9eb38024e264aaeb2378349ba3dfa03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928347"
---
# <span data-ttu-id="782ac-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="782ac-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="782ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="782ac-102">SYNOPSIS</span></span>
<span data-ttu-id="782ac-103">Hier erhalten Sie die Details des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="782ac-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="782ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="782ac-104">SYNTAX</span></span>

### <span data-ttu-id="782ac-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="782ac-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="782ac-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="782ac-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="782ac-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="782ac-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="782ac-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="782ac-108">DESCRIPTION</span></span>
<span data-ttu-id="782ac-109">Hier erhalten Sie die Details des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="782ac-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="782ac-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="782ac-110">EXAMPLES</span></span>

### <span data-ttu-id="782ac-111">Beispiel 1: Listentransaktionsknoten für ein Element der Blockkette</span><span class="sxs-lookup"><span data-stu-id="782ac-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="782ac-112">Mit diesem Befehl werden Transaktionsknoten für ein Element der Blockkette aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="782ac-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="782ac-113">Beispiel 2: Erhalten eines Transaktionsknotens</span><span class="sxs-lookup"><span data-stu-id="782ac-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="782ac-114">Dieser Befehl ruft einen Transaktionsknoten ab.</span><span class="sxs-lookup"><span data-stu-id="782ac-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="782ac-115">Beispiel 3: Erhalten eines Transaktionsknotens</span><span class="sxs-lookup"><span data-stu-id="782ac-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="782ac-116">Dieser Befehl ruft einen Transaktionsknoten ab.</span><span class="sxs-lookup"><span data-stu-id="782ac-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="782ac-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="782ac-117">PARAMETERS</span></span>

### <span data-ttu-id="782ac-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="782ac-118">-BlockchainMemberName</span></span>
<span data-ttu-id="782ac-119">Name des Mitgliedes der Blockkette.</span><span class="sxs-lookup"><span data-stu-id="782ac-119">Blockchain member name.</span></span>

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

### <span data-ttu-id="782ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="782ac-120">-DefaultProfile</span></span>
<span data-ttu-id="782ac-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="782ac-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="782ac-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="782ac-122">-InputObject</span></span>
<span data-ttu-id="782ac-123">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="782ac-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="782ac-124">-Name</span><span class="sxs-lookup"><span data-stu-id="782ac-124">-Name</span></span>
<span data-ttu-id="782ac-125">Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="782ac-125">Transaction node name.</span></span>

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

### <span data-ttu-id="782ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="782ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="782ac-127">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="782ac-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="782ac-128">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="782ac-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="782ac-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="782ac-129">-SubscriptionId</span></span>
<span data-ttu-id="782ac-130">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="782ac-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="782ac-131">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="782ac-131">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="782ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782ac-132">CommonParameters</span></span>
<span data-ttu-id="782ac-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="782ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782ac-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="782ac-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782ac-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="782ac-135">INPUTS</span></span>

### <span data-ttu-id="782ac-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="782ac-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="782ac-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="782ac-137">OUTPUTS</span></span>

### <span data-ttu-id="782ac-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="782ac-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="782ac-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="782ac-139">NOTES</span></span>

<span data-ttu-id="782ac-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="782ac-140">ALIASES</span></span>

<span data-ttu-id="782ac-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="782ac-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="782ac-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="782ac-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="782ac-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="782ac-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="782ac-144">INPUTOBJECT <IBlockchainIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="782ac-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="782ac-145">`[BlockchainMemberName <String>]`: Name des Mitgliedes der Blockkette.</span><span class="sxs-lookup"><span data-stu-id="782ac-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="782ac-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="782ac-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="782ac-147">`[Location <String>]`: Ortsname.</span><span class="sxs-lookup"><span data-stu-id="782ac-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="782ac-148">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="782ac-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="782ac-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="782ac-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="782ac-150">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="782ac-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="782ac-151">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="782ac-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="782ac-152">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="782ac-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="782ac-153">`[TransactionNodeName <String>]`: Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="782ac-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="782ac-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="782ac-154">RELATED LINKS</span></span>

