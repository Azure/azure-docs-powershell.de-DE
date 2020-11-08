---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997210"
---
# <span data-ttu-id="e034a-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e034a-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="e034a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e034a-102">SYNOPSIS</span></span>
<span data-ttu-id="e034a-103">Speichert eine geänderte Firewall.</span><span class="sxs-lookup"><span data-stu-id="e034a-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="e034a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e034a-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e034a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e034a-105">DESCRIPTION</span></span>
<span data-ttu-id="e034a-106">Das Cmdlet " **Satz-AzIpGroup** " aktualisiert ein Azure-IpGroup</span><span class="sxs-lookup"><span data-stu-id="e034a-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="e034a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e034a-107">EXAMPLES</span></span>

### <span data-ttu-id="e034a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e034a-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="e034a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e034a-109">PARAMETERS</span></span>

### <span data-ttu-id="e034a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e034a-110">-AsJob</span></span>
<span data-ttu-id="e034a-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e034a-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e034a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e034a-112">-DefaultProfile</span></span>
<span data-ttu-id="e034a-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e034a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e034a-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="e034a-114">-IpGroup</span></span>
<span data-ttu-id="e034a-115">Die IpGroup</span><span class="sxs-lookup"><span data-stu-id="e034a-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e034a-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e034a-116">-Confirm</span></span>
<span data-ttu-id="e034a-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e034a-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e034a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e034a-118">-WhatIf</span></span>
<span data-ttu-id="e034a-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e034a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e034a-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e034a-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e034a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e034a-121">CommonParameters</span></span>
<span data-ttu-id="e034a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e034a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e034a-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e034a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e034a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e034a-124">INPUTS</span></span>

### <span data-ttu-id="e034a-125">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="e034a-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="e034a-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e034a-126">OUTPUTS</span></span>

### <span data-ttu-id="e034a-127">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="e034a-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="e034a-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="e034a-128">NOTES</span></span>

## <span data-ttu-id="e034a-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e034a-129">RELATED LINKS</span></span>
