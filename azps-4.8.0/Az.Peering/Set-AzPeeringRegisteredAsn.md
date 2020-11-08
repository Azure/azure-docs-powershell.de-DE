---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174925"
---
# <span data-ttu-id="16b6d-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="16b6d-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="16b6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="16b6d-103">Legt einen registrierten ASN-Wert von der übergeordneten Peering Ressource fest oder aktualisiert ihn.</span><span class="sxs-lookup"><span data-stu-id="16b6d-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="16b6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16b6d-104">SYNTAX</span></span>

### <span data-ttu-id="16b6d-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="16b6d-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b6d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="16b6d-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b6d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16b6d-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16b6d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16b6d-108">DESCRIPTION</span></span>
<span data-ttu-id="16b6d-109">Ermöglicht die Aktualisierung eines registrierten ASN von übergeordneten Peering-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="16b6d-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="16b6d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16b6d-110">EXAMPLES</span></span>

### <span data-ttu-id="16b6d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16b6d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="16b6d-112">Aktualisiert die ASN by-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="16b6d-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="16b6d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="16b6d-113">PARAMETERS</span></span>

### <span data-ttu-id="16b6d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16b6d-114">-AsJob</span></span>
<span data-ttu-id="16b6d-115">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="16b6d-115">Run in the background.</span></span>

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

### <span data-ttu-id="16b6d-116">-ASN</span><span class="sxs-lookup"><span data-stu-id="16b6d-116">-Asn</span></span>
<span data-ttu-id="16b6d-117">Die zu Registrier-ASN</span><span class="sxs-lookup"><span data-stu-id="16b6d-117">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16b6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b6d-118">-DefaultProfile</span></span>
<span data-ttu-id="16b6d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16b6d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16b6d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="16b6d-120">-InputObject</span></span>
<span data-ttu-id="16b6d-121">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="16b6d-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16b6d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="16b6d-122">-Name</span></span>
<span data-ttu-id="16b6d-123">Die zu Registrier-ASN</span><span class="sxs-lookup"><span data-stu-id="16b6d-123">The ASN to be registered</span></span>

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

### <span data-ttu-id="16b6d-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="16b6d-124">-PeeringName</span></span>
<span data-ttu-id="16b6d-125">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="16b6d-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="16b6d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b6d-126">-ResourceGroupName</span></span>
<span data-ttu-id="16b6d-127">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="16b6d-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="16b6d-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="16b6d-128">-ResourceId</span></span>
<span data-ttu-id="16b6d-129">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="16b6d-129">The resource id string name.</span></span>

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

### <span data-ttu-id="16b6d-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16b6d-130">-Confirm</span></span>
<span data-ttu-id="16b6d-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16b6d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16b6d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16b6d-132">-WhatIf</span></span>
<span data-ttu-id="16b6d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16b6d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16b6d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16b6d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16b6d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b6d-135">CommonParameters</span></span>
<span data-ttu-id="16b6d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16b6d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b6d-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16b6d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b6d-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16b6d-138">INPUTS</span></span>

### <span data-ttu-id="16b6d-139">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="16b6d-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="16b6d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="16b6d-140">System.String</span></span>

## <span data-ttu-id="16b6d-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16b6d-141">OUTPUTS</span></span>

### <span data-ttu-id="16b6d-142">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="16b6d-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="16b6d-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="16b6d-143">NOTES</span></span>

## <span data-ttu-id="16b6d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16b6d-144">RELATED LINKS</span></span>
