---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 6ec33665bfa8a7f369c90c71fe9b8141682641e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923851"
---
# <span data-ttu-id="74276-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="74276-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="74276-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74276-102">SYNOPSIS</span></span>
<span data-ttu-id="74276-103">Hier erhalten Sie Details zu einem Mitglied der Blockkette.</span><span class="sxs-lookup"><span data-stu-id="74276-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="74276-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74276-104">SYNTAX</span></span>

### <span data-ttu-id="74276-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="74276-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="74276-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="74276-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="74276-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="74276-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="74276-108">Liste</span><span class="sxs-lookup"><span data-stu-id="74276-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="74276-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74276-109">DESCRIPTION</span></span>
<span data-ttu-id="74276-110">Hier erhalten Sie Details zu einem Mitglied der Blockkette.</span><span class="sxs-lookup"><span data-stu-id="74276-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="74276-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74276-111">EXAMPLES</span></span>

### <span data-ttu-id="74276-112">Beispiel 1: Auflisten von Mitgliedern der Blockkette</span><span class="sxs-lookup"><span data-stu-id="74276-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="74276-113">Mit diesem Befehl werden die Mitglieder der Blockkette unter einem Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="74276-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="74276-114">Beispiel 2: Auflisten von Mitgliedern der Blockkette</span><span class="sxs-lookup"><span data-stu-id="74276-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="74276-115">Mit diesem Befehl werden die Mitglieder der Blockkette unter einer Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="74276-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="74276-116">Beispiel 3: Holen Sie sich ein Mitglied der Blockkette</span><span class="sxs-lookup"><span data-stu-id="74276-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="74276-117">Mit diesem Befehl wird ein Mitglied der Blockkette unter einer Ressourcengruppe bekommt.</span><span class="sxs-lookup"><span data-stu-id="74276-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="74276-118">Beispiel 4: Holen Sie sich ein Mitglied der Blockkette</span><span class="sxs-lookup"><span data-stu-id="74276-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="74276-119">Mit diesem Befehl wird ein Mitglied der Blockkette unter einer Ressourcengruppe bekommt.</span><span class="sxs-lookup"><span data-stu-id="74276-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="74276-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="74276-120">PARAMETERS</span></span>

### <span data-ttu-id="74276-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74276-121">-DefaultProfile</span></span>
<span data-ttu-id="74276-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74276-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74276-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74276-123">-InputObject</span></span>
<span data-ttu-id="74276-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="74276-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="74276-125">-Name</span><span class="sxs-lookup"><span data-stu-id="74276-125">-Name</span></span>
<span data-ttu-id="74276-126">Name des Mitgliedes der Blockkette.</span><span class="sxs-lookup"><span data-stu-id="74276-126">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74276-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74276-127">-ResourceGroupName</span></span>
<span data-ttu-id="74276-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="74276-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="74276-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="74276-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="74276-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74276-130">-SubscriptionId</span></span>
<span data-ttu-id="74276-131">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="74276-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="74276-132">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="74276-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74276-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74276-133">CommonParameters</span></span>
<span data-ttu-id="74276-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74276-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74276-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74276-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74276-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74276-136">INPUTS</span></span>

### <span data-ttu-id="74276-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="74276-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="74276-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74276-138">OUTPUTS</span></span>

### <span data-ttu-id="74276-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="74276-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="74276-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="74276-140">NOTES</span></span>

<span data-ttu-id="74276-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="74276-141">ALIASES</span></span>

<span data-ttu-id="74276-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="74276-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="74276-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="74276-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74276-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="74276-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="74276-145">INPUTOBJECT <IBlockchainIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="74276-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="74276-146">`[BlockchainMemberName <String>]`: Name des Mitgliedes der Blockkette.</span><span class="sxs-lookup"><span data-stu-id="74276-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="74276-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="74276-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="74276-148">`[Location <String>]`: Ortsname.</span><span class="sxs-lookup"><span data-stu-id="74276-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="74276-149">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="74276-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="74276-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="74276-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="74276-151">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="74276-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="74276-152">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="74276-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="74276-153">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="74276-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="74276-154">`[TransactionNodeName <String>]`: Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="74276-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="74276-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="74276-155">RELATED LINKS</span></span>

