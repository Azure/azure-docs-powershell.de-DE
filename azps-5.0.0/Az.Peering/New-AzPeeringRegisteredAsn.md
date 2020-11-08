---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177423"
---
# <span data-ttu-id="a2898-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="a2898-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="a2898-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2898-102">SYNOPSIS</span></span>
<span data-ttu-id="a2898-103">Erstellen eines registrierten ASN für Peering</span><span class="sxs-lookup"><span data-stu-id="a2898-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="a2898-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2898-104">SYNTAX</span></span>

### <span data-ttu-id="a2898-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2898-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2898-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a2898-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2898-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2898-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2898-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2898-108">DESCRIPTION</span></span>
<span data-ttu-id="a2898-109">Erstellen Sie registrierte Lieferavise für Peering-Objekte.</span><span class="sxs-lookup"><span data-stu-id="a2898-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="a2898-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2898-110">EXAMPLES</span></span>

### <span data-ttu-id="a2898-111">Abrufen von Peering und Erstellen eines registrierten ASN</span><span class="sxs-lookup"><span data-stu-id="a2898-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="a2898-112">Rufen Sie das Peering ab, dem Sie einen registrierten ASN hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="a2898-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="a2898-113">Übergeben Sie diese dann an die Unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="a2898-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="a2898-114">Verwenden der Peering-Quell Codeerstellung zum Erstellen eines registrierten ASN-Codes</span><span class="sxs-lookup"><span data-stu-id="a2898-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="a2898-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2898-115">PARAMETERS</span></span>

### <span data-ttu-id="a2898-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2898-116">-AsJob</span></span>
<span data-ttu-id="a2898-117">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a2898-117">Run in the background.</span></span>

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

### <span data-ttu-id="a2898-118">-ASN</span><span class="sxs-lookup"><span data-stu-id="a2898-118">-Asn</span></span>
<span data-ttu-id="a2898-119">Die zu Registrier-ASN</span><span class="sxs-lookup"><span data-stu-id="a2898-119">The ASN to be registered</span></span>

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

### <span data-ttu-id="a2898-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2898-120">-DefaultProfile</span></span>
<span data-ttu-id="a2898-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2898-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2898-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a2898-122">-InputObject</span></span>
<span data-ttu-id="a2898-123">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a2898-123">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2898-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a2898-124">-Name</span></span>
<span data-ttu-id="a2898-125">Die zu Registrier-ASN</span><span class="sxs-lookup"><span data-stu-id="a2898-125">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2898-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="a2898-126">-PeeringName</span></span>
<span data-ttu-id="a2898-127">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a2898-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a2898-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2898-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2898-129">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="a2898-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="a2898-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a2898-130">-ResourceId</span></span>
<span data-ttu-id="a2898-131">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a2898-131">The resource id string name.</span></span>

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

### <span data-ttu-id="a2898-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2898-132">-Confirm</span></span>
<span data-ttu-id="a2898-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2898-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2898-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2898-134">-WhatIf</span></span>
<span data-ttu-id="a2898-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2898-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2898-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2898-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2898-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2898-137">CommonParameters</span></span>
<span data-ttu-id="a2898-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2898-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2898-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2898-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2898-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2898-140">INPUTS</span></span>

### <span data-ttu-id="a2898-141">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="a2898-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="a2898-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a2898-142">System.String</span></span>

## <span data-ttu-id="a2898-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2898-143">OUTPUTS</span></span>

### <span data-ttu-id="a2898-144">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="a2898-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="a2898-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2898-145">NOTES</span></span>

## <span data-ttu-id="a2898-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2898-146">RELATED LINKS</span></span>
