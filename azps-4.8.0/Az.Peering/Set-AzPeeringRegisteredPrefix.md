---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173138"
---
# <span data-ttu-id="b9850-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="b9850-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="b9850-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9850-102">SYNOPSIS</span></span>
<span data-ttu-id="b9850-103">Legt ein registriertes Präfix für die übergeordnete Peering-Ressource fest oder aktualisiert es.</span><span class="sxs-lookup"><span data-stu-id="b9850-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="b9850-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9850-104">SYNTAX</span></span>

### <span data-ttu-id="b9850-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9850-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9850-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b9850-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9850-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b9850-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9850-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9850-108">DESCRIPTION</span></span>
<span data-ttu-id="b9850-109">Ermöglicht die Aktualisierung eines registrierten Präfixes aus der übergeordneten Peering-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b9850-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="b9850-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9850-110">EXAMPLES</span></span>

### <span data-ttu-id="b9850-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9850-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="b9850-112">Aktualisiert das Präfix nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b9850-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="b9850-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9850-113">PARAMETERS</span></span>

### <span data-ttu-id="b9850-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9850-114">-AsJob</span></span>
<span data-ttu-id="b9850-115">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b9850-115">Run in the background.</span></span>

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

### <span data-ttu-id="b9850-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9850-116">-DefaultProfile</span></span>
<span data-ttu-id="b9850-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9850-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9850-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b9850-118">-InputObject</span></span>
<span data-ttu-id="b9850-119">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="b9850-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9850-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b9850-120">-Name</span></span>
<span data-ttu-id="b9850-121">Der Name des Präfixes.</span><span class="sxs-lookup"><span data-stu-id="b9850-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9850-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="b9850-122">-PeeringName</span></span>
<span data-ttu-id="b9850-123">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b9850-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b9850-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="b9850-124">-Prefix</span></span>
<span data-ttu-id="b9850-125">Das IPv4-Präfix der Sitzung</span><span class="sxs-lookup"><span data-stu-id="b9850-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="b9850-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9850-126">-ResourceGroupName</span></span>
<span data-ttu-id="b9850-127">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="b9850-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="b9850-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b9850-128">-ResourceId</span></span>
<span data-ttu-id="b9850-129">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b9850-129">The resource id string name.</span></span>

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

### <span data-ttu-id="b9850-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9850-130">-Confirm</span></span>
<span data-ttu-id="b9850-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9850-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9850-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9850-132">-WhatIf</span></span>
<span data-ttu-id="b9850-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9850-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9850-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9850-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9850-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9850-135">CommonParameters</span></span>
<span data-ttu-id="b9850-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9850-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9850-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9850-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9850-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9850-138">INPUTS</span></span>

### <span data-ttu-id="b9850-139">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="b9850-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="b9850-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b9850-140">System.String</span></span>

## <span data-ttu-id="b9850-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9850-141">OUTPUTS</span></span>

### <span data-ttu-id="b9850-142">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="b9850-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="b9850-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9850-143">NOTES</span></span>

## <span data-ttu-id="b9850-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9850-144">RELATED LINKS</span></span>
