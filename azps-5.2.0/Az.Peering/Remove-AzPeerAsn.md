---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360952"
---
# <span data-ttu-id="254b2-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="254b2-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="254b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="254b2-102">SYNOPSIS</span></span>
<span data-ttu-id="254b2-103">Peer Asn entfernen</span><span class="sxs-lookup"><span data-stu-id="254b2-103">Remove Peer Asn</span></span>

## <span data-ttu-id="254b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="254b2-104">SYNTAX</span></span>

### <span data-ttu-id="254b2-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="254b2-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="254b2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="254b2-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="254b2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="254b2-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="254b2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="254b2-108">DESCRIPTION</span></span>
<span data-ttu-id="254b2-109">Entfernen Sie einen PeerAsn aus dem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="254b2-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="254b2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="254b2-110">EXAMPLES</span></span>

### <span data-ttu-id="254b2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="254b2-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="254b2-112">Entfernt "Peer Asn"</span><span class="sxs-lookup"><span data-stu-id="254b2-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="254b2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="254b2-113">PARAMETERS</span></span>

### <span data-ttu-id="254b2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="254b2-114">-AsJob</span></span>
<span data-ttu-id="254b2-115">Führen Sie die Ausführung im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="254b2-115">Run in the background.</span></span>

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

### <span data-ttu-id="254b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="254b2-116">-DefaultProfile</span></span>
<span data-ttu-id="254b2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="254b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="254b2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="254b2-118">-Force</span></span>
<span data-ttu-id="254b2-119">{{ Fill Force Description }}</span><span class="sxs-lookup"><span data-stu-id="254b2-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="254b2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="254b2-120">-InputObject</span></span>
<span data-ttu-id="254b2-121">Das PeerAsn-Objekt.</span><span class="sxs-lookup"><span data-stu-id="254b2-121">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="254b2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="254b2-122">-Name</span></span>
<span data-ttu-id="254b2-123">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="254b2-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="254b2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="254b2-124">-PassThru</span></span>
<span data-ttu-id="254b2-125">"True" zurückgeben, wenn dies abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="254b2-125">Return true if complete</span></span>

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

### <span data-ttu-id="254b2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="254b2-126">-ResourceId</span></span>
<span data-ttu-id="254b2-127">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="254b2-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="254b2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="254b2-128">-Confirm</span></span>
<span data-ttu-id="254b2-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="254b2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="254b2-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="254b2-130">-WhatIf</span></span>
<span data-ttu-id="254b2-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="254b2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="254b2-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="254b2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="254b2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="254b2-133">CommonParameters</span></span>
<span data-ttu-id="254b2-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="254b2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="254b2-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="254b2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="254b2-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="254b2-136">INPUTS</span></span>

### <span data-ttu-id="254b2-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="254b2-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="254b2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="254b2-138">System.String</span></span>

## <span data-ttu-id="254b2-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="254b2-139">OUTPUTS</span></span>

### <span data-ttu-id="254b2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="254b2-140">System.Boolean</span></span>

## <span data-ttu-id="254b2-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="254b2-141">NOTES</span></span>

## <span data-ttu-id="254b2-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="254b2-142">RELATED LINKS</span></span>
