---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009368"
---
# <span data-ttu-id="dc05f-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="dc05f-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="dc05f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc05f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc05f-103">Abrufen von Details zu einem blockchain-Mitglied</span><span class="sxs-lookup"><span data-stu-id="dc05f-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="dc05f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc05f-104">SYNTAX</span></span>

### <span data-ttu-id="dc05f-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc05f-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc05f-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="dc05f-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc05f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc05f-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc05f-108">Liste</span><span class="sxs-lookup"><span data-stu-id="dc05f-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc05f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc05f-109">DESCRIPTION</span></span>
<span data-ttu-id="dc05f-110">Abrufen von Details zu einem blockchain-Mitglied</span><span class="sxs-lookup"><span data-stu-id="dc05f-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="dc05f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc05f-111">EXAMPLES</span></span>

### <span data-ttu-id="dc05f-112">Beispiel 1: Auflisten von blockchain-Mitgliedern</span><span class="sxs-lookup"><span data-stu-id="dc05f-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="dc05f-113">Dieser Befehl listet blockchain-Mitglieder unter einem Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="dc05f-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="dc05f-114">Beispiel 2: Auflisten von blockchain-Mitgliedern</span><span class="sxs-lookup"><span data-stu-id="dc05f-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="dc05f-115">Dieser Befehl listet blockchain-Mitglieder unter einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="dc05f-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="dc05f-116">Beispiel 3: Abrufen eines blockchain-Members</span><span class="sxs-lookup"><span data-stu-id="dc05f-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="dc05f-117">Dieser Befehl ruft ein blockchain-Element unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="dc05f-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="dc05f-118">Beispiel 4: Abrufen eines blockchain-Members</span><span class="sxs-lookup"><span data-stu-id="dc05f-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="dc05f-119">Dieser Befehl ruft ein blockchain-Element unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="dc05f-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="dc05f-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc05f-120">PARAMETERS</span></span>

### <span data-ttu-id="dc05f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc05f-121">-DefaultProfile</span></span>
<span data-ttu-id="dc05f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc05f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc05f-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dc05f-123">-InputObject</span></span>
<span data-ttu-id="dc05f-124">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dc05f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc05f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dc05f-125">-Name</span></span>
<span data-ttu-id="dc05f-126">Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="dc05f-126">Blockchain member name.</span></span>

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

### <span data-ttu-id="dc05f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc05f-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc05f-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="dc05f-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="dc05f-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="dc05f-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="dc05f-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="dc05f-130">-SubscriptionId</span></span>
<span data-ttu-id="dc05f-131">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dc05f-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="dc05f-132">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="dc05f-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dc05f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc05f-133">CommonParameters</span></span>
<span data-ttu-id="dc05f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc05f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc05f-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc05f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc05f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc05f-136">INPUTS</span></span>

### <span data-ttu-id="dc05f-137">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="dc05f-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="dc05f-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc05f-138">OUTPUTS</span></span>

### <span data-ttu-id="dc05f-139">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="dc05f-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="dc05f-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc05f-140">NOTES</span></span>

<span data-ttu-id="dc05f-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="dc05f-141">ALIASES</span></span>

<span data-ttu-id="dc05f-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc05f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc05f-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc05f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc05f-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="dc05f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc05f-145">Inputobject <IBlockchainIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="dc05f-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc05f-146">`[BlockchainMemberName <String>]`: Blockchain-Elementname.</span><span class="sxs-lookup"><span data-stu-id="dc05f-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="dc05f-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="dc05f-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc05f-148">`[Location <String>]`: Standortname.</span><span class="sxs-lookup"><span data-stu-id="dc05f-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="dc05f-149">`[OperationId <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="dc05f-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="dc05f-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="dc05f-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="dc05f-151">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="dc05f-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="dc05f-152">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dc05f-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="dc05f-153">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="dc05f-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="dc05f-154">`[TransactionNodeName <String>]`: Name des Transaktions Knotens.</span><span class="sxs-lookup"><span data-stu-id="dc05f-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="dc05f-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc05f-155">RELATED LINKS</span></span>

