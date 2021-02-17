---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: fef6f1615bb2e3dd9d3bb19738ea6cef393235aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169516"
---
# <span data-ttu-id="5a763-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="5a763-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="5a763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a763-102">SYNOPSIS</span></span>
<span data-ttu-id="5a763-103">Ruft eine Liste der Peeringdienstpräfixe für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5a763-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="5a763-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a763-104">SYNTAX</span></span>

### <span data-ttu-id="5a763-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a763-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a763-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5a763-106">InputObject</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a763-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a763-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a763-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a763-108">DESCRIPTION</span></span>
<span data-ttu-id="5a763-109">Listen peeringdienstpräfixe für Peeringdienstobjekte</span><span class="sxs-lookup"><span data-stu-id="5a763-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="5a763-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a763-110">EXAMPLES</span></span>

### <span data-ttu-id="5a763-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a763-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="5a763-112">Ruft die Präfixe für einen Peeringdienst basierend auf Pipingbefehlen ab.</span><span class="sxs-lookup"><span data-stu-id="5a763-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="5a763-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5a763-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="5a763-114">Ruft ein bestimmtes Präfix für einen Peeringdienst nach Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="5a763-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="5a763-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5a763-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="5a763-116">Ruft ein bestimmtes Präfix für einen Peeringdienst nach Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="5a763-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="5a763-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="5a763-117">Example 4</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="5a763-118">Ruft ein bestimmtes Präfix für einen Peeringdienst mit erweiterten Attributen ab.</span><span class="sxs-lookup"><span data-stu-id="5a763-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="5a763-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a763-119">PARAMETERS</span></span>

### <span data-ttu-id="5a763-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a763-120">-DefaultProfile</span></span>
<span data-ttu-id="5a763-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a763-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a763-122">-Expand</span><span class="sxs-lookup"><span data-stu-id="5a763-122">-Expand</span></span>
<span data-ttu-id="5a763-123">Anzeigen der Ereignisse für ein Peeringdienstpräfix</span><span class="sxs-lookup"><span data-stu-id="5a763-123">View the events for a peering service prefix</span></span>

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

### <span data-ttu-id="5a763-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5a763-124">-Name</span></span>
<span data-ttu-id="5a763-125">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="5a763-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a763-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="5a763-126">-PeeringServiceName</span></span>
<span data-ttu-id="5a763-127">Der Name des Peeringdiensts.</span><span class="sxs-lookup"><span data-stu-id="5a763-127">The peering service name.</span></span> <span data-ttu-id="5a763-128">Verwenden New-AzPeeringService cmdlet für einen neuen Peeringdienst oder Get-AzPeeringService für eine Liste.</span><span class="sxs-lookup"><span data-stu-id="5a763-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a763-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="5a763-129">-PeeringServiceObject</span></span>
<span data-ttu-id="5a763-130">Verwenden eines Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="5a763-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a763-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a763-131">-ResourceGroupName</span></span>
<span data-ttu-id="5a763-132">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5a763-132">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a763-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a763-133">-ResourceId</span></span>
<span data-ttu-id="5a763-134">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5a763-134">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a763-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a763-135">CommonParameters</span></span>
<span data-ttu-id="5a763-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a763-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a763-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a763-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a763-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a763-138">INPUTS</span></span>

### <span data-ttu-id="5a763-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="5a763-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="5a763-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5a763-140">System.String</span></span>

## <span data-ttu-id="5a763-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a763-141">OUTPUTS</span></span>

### <span data-ttu-id="5a763-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="5a763-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="5a763-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5a763-143">NOTES</span></span>

## <span data-ttu-id="5a763-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5a763-144">RELATED LINKS</span></span>
