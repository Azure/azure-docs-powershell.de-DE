---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166139"
---
# <span data-ttu-id="d110b-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="d110b-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="d110b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d110b-102">SYNOPSIS</span></span>
<span data-ttu-id="d110b-103">Erstellt oder aktualisiert eine Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="d110b-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="d110b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d110b-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d110b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d110b-105">DESCRIPTION</span></span>
<span data-ttu-id="d110b-106">Erstellt oder aktualisiert eine Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="d110b-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="d110b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d110b-107">EXAMPLES</span></span>

### <span data-ttu-id="d110b-108">Beispiel 1: Erstellen einer neuen Move-Sammlung</span><span class="sxs-lookup"><span data-stu-id="d110b-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="d110b-109">Erstellen Sie eine neue Move-Sammlung in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d110b-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="d110b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d110b-110">PARAMETERS</span></span>

### <span data-ttu-id="d110b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d110b-111">-DefaultProfile</span></span>
<span data-ttu-id="d110b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d110b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d110b-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="d110b-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="d110b-114">Ruft die Prinzipal-ID ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="d110b-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="d110b-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="d110b-115">-IdentityTenantId</span></span>
<span data-ttu-id="d110b-116">Ruft die Mandanten-ID ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="d110b-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="d110b-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d110b-117">-IdentityType</span></span>
<span data-ttu-id="d110b-118">Der Typ der Identität, die für den Bereichs Verschiebungs Dienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d110b-118">The type of identity used for the region move service.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.ResourceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d110b-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="d110b-119">-Location</span></span>
<span data-ttu-id="d110b-120">Die Geo-Position, an der die Ressource wohnt.</span><span class="sxs-lookup"><span data-stu-id="d110b-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="d110b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d110b-121">-Name</span></span>
<span data-ttu-id="d110b-122">Der Name der verschieben-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="d110b-122">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d110b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d110b-123">-ResourceGroupName</span></span>
<span data-ttu-id="d110b-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d110b-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="d110b-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="d110b-125">-SourceRegion</span></span>
<span data-ttu-id="d110b-126">Ruft den Quellbereich ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="d110b-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="d110b-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d110b-127">-SubscriptionId</span></span>
<span data-ttu-id="d110b-128">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="d110b-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="d110b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="d110b-129">-Tag</span></span>
<span data-ttu-id="d110b-130">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="d110b-130">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d110b-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="d110b-131">-TargetRegion</span></span>
<span data-ttu-id="d110b-132">Ruft den Zielbereich ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="d110b-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="d110b-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d110b-133">-Confirm</span></span>
<span data-ttu-id="d110b-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d110b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d110b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d110b-135">-WhatIf</span></span>
<span data-ttu-id="d110b-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d110b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d110b-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d110b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d110b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d110b-138">CommonParameters</span></span>
<span data-ttu-id="d110b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d110b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d110b-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d110b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d110b-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d110b-141">INPUTS</span></span>

## <span data-ttu-id="d110b-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d110b-142">OUTPUTS</span></span>

### <span data-ttu-id="d110b-143">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="d110b-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="d110b-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d110b-144">NOTES</span></span>

<span data-ttu-id="d110b-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="d110b-145">ALIASES</span></span>

## <span data-ttu-id="d110b-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d110b-146">RELATED LINKS</span></span>

