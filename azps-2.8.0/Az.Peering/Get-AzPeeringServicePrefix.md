---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: 4bbd6e491d67e9ef3dd4fae0adc92561aa01c866
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824040"
---
# <span data-ttu-id="9b543-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="9b543-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="9b543-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b543-102">SYNOPSIS</span></span>
<span data-ttu-id="9b543-103">Ruft eine Liste mit Peering-Dienst Präfixen für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="9b543-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="9b543-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b543-104">SYNTAX</span></span>

### <span data-ttu-id="9b543-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b543-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b543-106">Standard</span><span class="sxs-lookup"><span data-stu-id="9b543-106">Default</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b543-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b543-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b543-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b543-108">DESCRIPTION</span></span>
<span data-ttu-id="9b543-109">Listen peeringdienst-Präfixe für Peering-Dienstobjekte</span><span class="sxs-lookup"><span data-stu-id="9b543-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="9b543-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b543-110">EXAMPLES</span></span>

### <span data-ttu-id="9b543-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9b543-111">Example 1</span></span>
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

<span data-ttu-id="9b543-112">Ruft die Präfixe für einen peeringdienst auf der Grundlage von Rohrleitungs Befehlen ab.</span><span class="sxs-lookup"><span data-stu-id="9b543-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="9b543-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9b543-113">Example 2</span></span>
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

<span data-ttu-id="9b543-114">Ruft ein bestimmtes Präfix für einen peeringdienst nach Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="9b543-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="9b543-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="9b543-115">Example 3</span></span>
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

<span data-ttu-id="9b543-116">Ruft ein bestimmtes Präfix für einen peeringdienst nach Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="9b543-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="9b543-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="9b543-117">Example 4</span></span>
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

<span data-ttu-id="9b543-118">Ruft ein bestimmtes Präfix für einen peeringdienst mit erweiterten Attributen ab.</span><span class="sxs-lookup"><span data-stu-id="9b543-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="9b543-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b543-119">PARAMETERS</span></span>

### <span data-ttu-id="9b543-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b543-120">-DefaultProfile</span></span>
<span data-ttu-id="9b543-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b543-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b543-122">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="9b543-122">-Expand</span></span>
<span data-ttu-id="9b543-123">Anzeigen der Ereignisse für ein Peering-Dienst Präfix</span><span class="sxs-lookup"><span data-stu-id="9b543-123">View the events for a peering service prefix</span></span>

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

### <span data-ttu-id="9b543-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9b543-124">-Name</span></span>
<span data-ttu-id="9b543-125">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="9b543-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b543-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="9b543-126">-PeeringServiceName</span></span>
<span data-ttu-id="9b543-127">Der Name des Peering Diensts.</span><span class="sxs-lookup"><span data-stu-id="9b543-127">The peering service name.</span></span> <span data-ttu-id="9b543-128">Verwenden Sie New-AzPeeringService-Cmdlet für einen neuen peeringdienst oder Get-AzPeeringService für eine Liste.</span><span class="sxs-lookup"><span data-stu-id="9b543-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="9b543-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="9b543-129">-PeeringServiceObject</span></span>
<span data-ttu-id="9b543-130">Verwenden eines Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="9b543-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b543-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b543-131">-ResourceGroupName</span></span>
<span data-ttu-id="9b543-132">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="9b543-132">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="9b543-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9b543-133">-ResourceId</span></span>
<span data-ttu-id="9b543-134">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9b543-134">The resource id string name.</span></span>

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

### <span data-ttu-id="9b543-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b543-135">CommonParameters</span></span>
<span data-ttu-id="9b543-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b543-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b543-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b543-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b543-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b543-138">INPUTS</span></span>

### <span data-ttu-id="9b543-139">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="9b543-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="9b543-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9b543-140">System.String</span></span>

## <span data-ttu-id="9b543-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b543-141">OUTPUTS</span></span>

### <span data-ttu-id="9b543-142">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="9b543-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="9b543-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b543-143">NOTES</span></span>

## <span data-ttu-id="9b543-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b543-144">RELATED LINKS</span></span>
