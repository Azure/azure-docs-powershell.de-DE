---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: e488baacb4e9412cb4e3e5be2b6a595629495b16
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002968"
---
# <span data-ttu-id="1f519-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="1f519-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="1f519-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f519-102">SYNOPSIS</span></span>
<span data-ttu-id="1f519-103">Erstellt ein neues Peering-Dienst Präfix</span><span class="sxs-lookup"><span data-stu-id="1f519-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="1f519-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f519-104">SYNTAX</span></span>

### <span data-ttu-id="1f519-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f519-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f519-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f519-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f519-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f519-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> [-PeeringServiceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f519-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f519-108">DESCRIPTION</span></span>
<span data-ttu-id="1f519-109">Erstellt ein Peer-Service-Präfix, das einem Peering-Dienstobjekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1f519-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="1f519-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f519-110">EXAMPLES</span></span>

### <span data-ttu-id="1f519-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1f519-111">Example 1</span></span>
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

<span data-ttu-id="1f519-112">Erstellt ein Präfix aus einem Peering-Dienstobjekt</span><span class="sxs-lookup"><span data-stu-id="1f519-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="1f519-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1f519-113">Example 2</span></span>
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

<span data-ttu-id="1f519-114">Erstellt ein Präfix aus der Ressourcen-ID des Peering-Diensts.</span><span class="sxs-lookup"><span data-stu-id="1f519-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="1f519-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1f519-115">Example 3</span></span>
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

<span data-ttu-id="1f519-116">Erstellt ein Präfix aus dem Namen und dem Namen eines Peering Service-Ressourcengruppen</span><span class="sxs-lookup"><span data-stu-id="1f519-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="1f519-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f519-117">PARAMETERS</span></span>

### <span data-ttu-id="1f519-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f519-118">-AsJob</span></span>
<span data-ttu-id="1f519-119">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1f519-119">Run in the background.</span></span>

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

### <span data-ttu-id="1f519-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f519-120">-DefaultProfile</span></span>
<span data-ttu-id="1f519-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f519-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f519-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1f519-122">-Name</span></span>
<span data-ttu-id="1f519-123">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="1f519-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="1f519-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="1f519-124">-PeeringServiceId</span></span>
<span data-ttu-id="1f519-125">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1f519-125">The resource id string name.</span></span>

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

### <span data-ttu-id="1f519-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="1f519-126">-PeeringServiceName</span></span>
<span data-ttu-id="1f519-127">Der Name des Peering Diensts.</span><span class="sxs-lookup"><span data-stu-id="1f519-127">The peering service name.</span></span>
<span data-ttu-id="1f519-128">Verwenden Sie New-AzPeeringService-Cmdlet für einen neuen peeringdienst oder Get-AzPeeringService für eine Liste.</span><span class="sxs-lookup"><span data-stu-id="1f519-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="1f519-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="1f519-129">-PeeringServiceObject</span></span>
<span data-ttu-id="1f519-130">Verwenden eines Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="1f519-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="1f519-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="1f519-131">-Prefix</span></span>
<span data-ttu-id="1f519-132">Das IPv4-Präfix der Sitzung</span><span class="sxs-lookup"><span data-stu-id="1f519-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="1f519-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f519-133">-ResourceGroupName</span></span>
<span data-ttu-id="1f519-134">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="1f519-134">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="1f519-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f519-135">-Confirm</span></span>
<span data-ttu-id="1f519-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f519-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f519-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f519-137">-WhatIf</span></span>
<span data-ttu-id="1f519-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f519-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f519-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f519-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f519-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f519-140">CommonParameters</span></span>
<span data-ttu-id="1f519-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f519-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f519-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f519-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f519-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f519-143">INPUTS</span></span>

### <span data-ttu-id="1f519-144">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="1f519-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="1f519-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f519-145">OUTPUTS</span></span>

### <span data-ttu-id="1f519-146">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="1f519-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="1f519-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f519-147">NOTES</span></span>

## <span data-ttu-id="1f519-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f519-148">RELATED LINKS</span></span>
