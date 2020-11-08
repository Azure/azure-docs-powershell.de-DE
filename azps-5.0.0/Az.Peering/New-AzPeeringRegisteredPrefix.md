---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177082"
---
# <span data-ttu-id="4f7e5-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="4f7e5-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="4f7e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f7e5-102">SYNOPSIS</span></span>
<span data-ttu-id="4f7e5-103">Erstellen von registrierten Präfixen für Peering-Objekte</span><span class="sxs-lookup"><span data-stu-id="4f7e5-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="4f7e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f7e5-104">SYNTAX</span></span>

### <span data-ttu-id="4f7e5-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f7e5-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f7e5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4f7e5-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f7e5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f7e5-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f7e5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f7e5-108">DESCRIPTION</span></span>
<span data-ttu-id="4f7e5-109">Erstellen von registrierten Präfixen für Peering-Objekte</span><span class="sxs-lookup"><span data-stu-id="4f7e5-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="4f7e5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f7e5-110">EXAMPLES</span></span>

### <span data-ttu-id="4f7e5-111">Abrufen von Peering und Erstellen eines registrierten Präfixes</span><span class="sxs-lookup"><span data-stu-id="4f7e5-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="4f7e5-112">Rufen Sie das Peering ab, dem Sie ein registriertes Präfix hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f7e5-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="4f7e5-113">Übergeben Sie diese dann an die Unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="4f7e5-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="4f7e5-114">Verwenden der Peering-Quell Codeerstellung zum Erstellen eines registrierten ASN-Codes</span><span class="sxs-lookup"><span data-stu-id="4f7e5-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="4f7e5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f7e5-115">PARAMETERS</span></span>

### <span data-ttu-id="4f7e5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f7e5-116">-AsJob</span></span>
<span data-ttu-id="4f7e5-117">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4f7e5-117">Run in the background.</span></span>

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

### <span data-ttu-id="4f7e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f7e5-118">-DefaultProfile</span></span>
<span data-ttu-id="4f7e5-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f7e5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f7e5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4f7e5-120">-InputObject</span></span>
<span data-ttu-id="4f7e5-121">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="4f7e5-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="4f7e5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4f7e5-122">-Name</span></span>
<span data-ttu-id="4f7e5-123">Der Name des Präfixes.</span><span class="sxs-lookup"><span data-stu-id="4f7e5-123">The name of prefix.</span></span>

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

### <span data-ttu-id="4f7e5-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="4f7e5-124">-PeeringName</span></span>
<span data-ttu-id="4f7e5-125">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="4f7e5-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="4f7e5-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="4f7e5-126">-Prefix</span></span>
<span data-ttu-id="4f7e5-127">Das IPv4-Präfix der Sitzung</span><span class="sxs-lookup"><span data-stu-id="4f7e5-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="4f7e5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f7e5-128">-ResourceGroupName</span></span>
<span data-ttu-id="4f7e5-129">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="4f7e5-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="4f7e5-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4f7e5-130">-ResourceId</span></span>
<span data-ttu-id="4f7e5-131">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4f7e5-131">The resource id string name.</span></span>

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

### <span data-ttu-id="4f7e5-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4f7e5-132">-Confirm</span></span>
<span data-ttu-id="4f7e5-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f7e5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f7e5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f7e5-134">-WhatIf</span></span>
<span data-ttu-id="4f7e5-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f7e5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f7e5-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f7e5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f7e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f7e5-137">CommonParameters</span></span>
<span data-ttu-id="4f7e5-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f7e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f7e5-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f7e5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f7e5-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f7e5-140">INPUTS</span></span>

### <span data-ttu-id="4f7e5-141">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="4f7e5-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="4f7e5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4f7e5-142">System.String</span></span>

## <span data-ttu-id="4f7e5-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f7e5-143">OUTPUTS</span></span>

### <span data-ttu-id="4f7e5-144">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="4f7e5-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="4f7e5-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f7e5-145">NOTES</span></span>

## <span data-ttu-id="4f7e5-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f7e5-146">RELATED LINKS</span></span>
