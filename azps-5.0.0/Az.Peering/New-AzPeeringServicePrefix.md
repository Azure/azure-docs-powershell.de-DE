---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178441"
---
# <span data-ttu-id="a93ea-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="a93ea-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="a93ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a93ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a93ea-103">Erstellt ein neues Peering-Dienst Präfix</span><span class="sxs-lookup"><span data-stu-id="a93ea-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="a93ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a93ea-104">SYNTAX</span></span>

### <span data-ttu-id="a93ea-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="a93ea-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a93ea-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a93ea-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a93ea-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a93ea-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a93ea-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a93ea-108">DESCRIPTION</span></span>
<span data-ttu-id="a93ea-109">Erstellt ein Peer-Service-Präfix, das einem Peering-Dienstobjekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a93ea-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="a93ea-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a93ea-110">EXAMPLES</span></span>

### <span data-ttu-id="a93ea-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a93ea-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | New-AzPeeringServicePrefix -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="a93ea-112">Erstellt ein Präfix aus einem Peering-Dienstobjekt</span><span class="sxs-lookup"><span data-stu-id="a93ea-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="a93ea-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a93ea-113">Example 2</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -PeeringServiceId $peeringServiceResourceId -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="a93ea-114">Erstellt ein Präfix aus der Ressourcen-ID des Peering-Diensts.</span><span class="sxs-lookup"><span data-stu-id="a93ea-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="a93ea-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a93ea-115">Example 3</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="a93ea-116">Erstellt ein Präfix aus dem Namen und dem Namen eines Peering Service-Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="a93ea-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="a93ea-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a93ea-117">PARAMETERS</span></span>

### <span data-ttu-id="a93ea-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a93ea-118">-AsJob</span></span>
<span data-ttu-id="a93ea-119">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a93ea-119">Run in the background.</span></span>

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

### <span data-ttu-id="a93ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93ea-120">-DefaultProfile</span></span>
<span data-ttu-id="a93ea-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a93ea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a93ea-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a93ea-122">-Name</span></span>
<span data-ttu-id="a93ea-123">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a93ea-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ea-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="a93ea-124">-PeeringServiceId</span></span>
<span data-ttu-id="a93ea-125">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a93ea-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ea-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="a93ea-126">-PeeringServiceName</span></span>
<span data-ttu-id="a93ea-127">Der Name des Peering Diensts.</span><span class="sxs-lookup"><span data-stu-id="a93ea-127">The peering service name.</span></span>
<span data-ttu-id="a93ea-128">Verwenden Sie New-AzPeeringService-Cmdlet für einen neuen peeringdienst oder Get-AzPeeringService für eine Liste.</span><span class="sxs-lookup"><span data-stu-id="a93ea-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ea-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="a93ea-129">-PeeringServiceObject</span></span>
<span data-ttu-id="a93ea-130">Verwenden eines Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="a93ea-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a93ea-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="a93ea-131">-Prefix</span></span>
<span data-ttu-id="a93ea-132">Das IPv4-Präfix der Sitzung</span><span class="sxs-lookup"><span data-stu-id="a93ea-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="a93ea-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a93ea-133">-ResourceGroupName</span></span>
<span data-ttu-id="a93ea-134">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="a93ea-134">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ea-135">-ServiceKey verwenden</span><span class="sxs-lookup"><span data-stu-id="a93ea-135">-ServiceKey</span></span>
<span data-ttu-id="a93ea-136">Dies ist eine eindeutige GUID, die von Ihrem Dienstanbieter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a93ea-136">This is a unique GUID provided by your service provider</span></span>

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

### <span data-ttu-id="a93ea-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a93ea-137">-Confirm</span></span>
<span data-ttu-id="a93ea-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a93ea-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a93ea-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a93ea-139">-WhatIf</span></span>
<span data-ttu-id="a93ea-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a93ea-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a93ea-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a93ea-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a93ea-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93ea-142">CommonParameters</span></span>
<span data-ttu-id="a93ea-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a93ea-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93ea-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a93ea-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93ea-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a93ea-145">INPUTS</span></span>

### <span data-ttu-id="a93ea-146">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="a93ea-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="a93ea-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a93ea-147">OUTPUTS</span></span>

### <span data-ttu-id="a93ea-148">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="a93ea-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="a93ea-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="a93ea-149">NOTES</span></span>

## <span data-ttu-id="a93ea-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a93ea-150">RELATED LINKS</span></span>
