---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174928"
---
# <span data-ttu-id="9bdb6-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="9bdb6-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="9bdb6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9bdb6-102">SYNOPSIS</span></span>
<span data-ttu-id="9bdb6-103">Peer-ASN entfernen</span><span class="sxs-lookup"><span data-stu-id="9bdb6-103">Remove Peer Asn</span></span>

## <span data-ttu-id="9bdb6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bdb6-104">SYNTAX</span></span>

### <span data-ttu-id="9bdb6-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9bdb6-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bdb6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9bdb6-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bdb6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9bdb6-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bdb6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9bdb6-108">DESCRIPTION</span></span>
<span data-ttu-id="9bdb6-109">Entfernen eines PeerAsn aus dem Abonnement</span><span class="sxs-lookup"><span data-stu-id="9bdb6-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="9bdb6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9bdb6-110">EXAMPLES</span></span>

### <span data-ttu-id="9bdb6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9bdb6-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="9bdb6-112">Entfernt die Peer-ASN</span><span class="sxs-lookup"><span data-stu-id="9bdb6-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="9bdb6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bdb6-113">PARAMETERS</span></span>

### <span data-ttu-id="9bdb6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bdb6-114">-AsJob</span></span>
<span data-ttu-id="9bdb6-115">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9bdb6-115">Run in the background.</span></span>

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

### <span data-ttu-id="9bdb6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bdb6-116">-DefaultProfile</span></span>
<span data-ttu-id="9bdb6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9bdb6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bdb6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9bdb6-118">-Force</span></span>
<span data-ttu-id="9bdb6-119">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="9bdb6-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="9bdb6-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9bdb6-120">-InputObject</span></span>
<span data-ttu-id="9bdb6-121">Das PeerAsn-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9bdb6-121">The PeerAsn object.</span></span>

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

### <span data-ttu-id="9bdb6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9bdb6-122">-Name</span></span>
<span data-ttu-id="9bdb6-123">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="9bdb6-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="9bdb6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bdb6-124">-PassThru</span></span>
<span data-ttu-id="9bdb6-125">True zurück, wenn abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="9bdb6-125">Return true if complete</span></span>

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

### <span data-ttu-id="9bdb6-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9bdb6-126">-ResourceId</span></span>
<span data-ttu-id="9bdb6-127">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9bdb6-127">The resource id string name.</span></span>

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

### <span data-ttu-id="9bdb6-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9bdb6-128">-Confirm</span></span>
<span data-ttu-id="9bdb6-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9bdb6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bdb6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bdb6-130">-WhatIf</span></span>
<span data-ttu-id="9bdb6-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9bdb6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bdb6-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9bdb6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bdb6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bdb6-133">CommonParameters</span></span>
<span data-ttu-id="9bdb6-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bdb6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bdb6-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bdb6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bdb6-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9bdb6-136">INPUTS</span></span>

### <span data-ttu-id="9bdb6-137">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="9bdb6-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="9bdb6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9bdb6-138">System.String</span></span>

## <span data-ttu-id="9bdb6-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9bdb6-139">OUTPUTS</span></span>

### <span data-ttu-id="9bdb6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9bdb6-140">System.Boolean</span></span>

## <span data-ttu-id="9bdb6-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="9bdb6-141">NOTES</span></span>

## <span data-ttu-id="9bdb6-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9bdb6-142">RELATED LINKS</span></span>
