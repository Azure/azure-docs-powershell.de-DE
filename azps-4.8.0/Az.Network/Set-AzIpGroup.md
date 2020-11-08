---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009045"
---
# <span data-ttu-id="66ae8-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="66ae8-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="66ae8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="66ae8-103">Speichert eine geänderte Firewall.</span><span class="sxs-lookup"><span data-stu-id="66ae8-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="66ae8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66ae8-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66ae8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66ae8-105">DESCRIPTION</span></span>
<span data-ttu-id="66ae8-106">Das Cmdlet " **Satz-AzIpGroup** " aktualisiert ein Azure-IpGroup</span><span class="sxs-lookup"><span data-stu-id="66ae8-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="66ae8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66ae8-107">EXAMPLES</span></span>

### <span data-ttu-id="66ae8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66ae8-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="66ae8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="66ae8-109">PARAMETERS</span></span>

### <span data-ttu-id="66ae8-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66ae8-110">-AsJob</span></span>
<span data-ttu-id="66ae8-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="66ae8-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66ae8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ae8-112">-DefaultProfile</span></span>
<span data-ttu-id="66ae8-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66ae8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66ae8-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="66ae8-114">-IpGroup</span></span>
<span data-ttu-id="66ae8-115">Die IpGroup</span><span class="sxs-lookup"><span data-stu-id="66ae8-115">The IpGroup</span></span>

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

### <span data-ttu-id="66ae8-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66ae8-116">-Confirm</span></span>
<span data-ttu-id="66ae8-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66ae8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66ae8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66ae8-118">-WhatIf</span></span>
<span data-ttu-id="66ae8-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66ae8-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66ae8-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66ae8-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66ae8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ae8-121">CommonParameters</span></span>
<span data-ttu-id="66ae8-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66ae8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ae8-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66ae8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ae8-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66ae8-124">INPUTS</span></span>

### <span data-ttu-id="66ae8-125">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="66ae8-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="66ae8-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66ae8-126">OUTPUTS</span></span>

### <span data-ttu-id="66ae8-127">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="66ae8-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="66ae8-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="66ae8-128">NOTES</span></span>

## <span data-ttu-id="66ae8-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66ae8-129">RELATED LINKS</span></span>
