---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
ms.openlocfilehash: 6d46be31d443bdfeeda850cd03ce2a050e25549f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505309"
---
# <span data-ttu-id="c9e3a-101">New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="c9e3a-101">New-AzureRmPublicIpTag</span></span>

## <span data-ttu-id="c9e3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e3a-103">Erstellt ein IP-Tag.</span><span class="sxs-lookup"><span data-stu-id="c9e3a-103">Creates an IP Tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9e3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9e3a-104">SYNTAX</span></span>

```
New-AzureRmPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9e3a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9e3a-105">DESCRIPTION</span></span>
<span data-ttu-id="c9e3a-106">Das Cmdlet **New-AzureRmPublicIpTag** erstellt ein IP-Tag.</span><span class="sxs-lookup"><span data-stu-id="c9e3a-106">The **New-AzureRmPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="c9e3a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9e3a-107">EXAMPLES</span></span>

### <span data-ttu-id="c9e3a-108">1: Erstellen eines neuen IP-Tags</span><span class="sxs-lookup"><span data-stu-id="c9e3a-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="c9e3a-109">Dieser Befehl erstellt ein neues IP-Tag mit dem TagType wie "FirstPartyUsage" und Tag wie "/SQL".</span><span class="sxs-lookup"><span data-stu-id="c9e3a-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="c9e3a-110">Dieser wird in der publicIpAddress-Erstellung mit diesen speziellen Tags für die Zuweisung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9e3a-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="c9e3a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9e3a-111">PARAMETERS</span></span>

### <span data-ttu-id="c9e3a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e3a-112">-DefaultProfile</span></span>
<span data-ttu-id="c9e3a-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9e3a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e3a-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="c9e3a-114">-IpTagType</span></span>
<span data-ttu-id="c9e3a-115">Beispiel für einen IpTag: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="c9e3a-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e3a-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="c9e3a-116">-Tag</span></span>
<span data-ttu-id="c9e3a-117">Beispiel für einen IpTag-Wert:/SQL</span><span class="sxs-lookup"><span data-stu-id="c9e3a-117">IpTag value Example:/Sql</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e3a-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c9e3a-118">-Confirm</span></span>
<span data-ttu-id="c9e3a-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9e3a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9e3a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9e3a-120">-WhatIf</span></span>
<span data-ttu-id="c9e3a-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9e3a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9e3a-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9e3a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9e3a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e3a-123">CommonParameters</span></span>
<span data-ttu-id="c9e3a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9e3a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e3a-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9e3a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e3a-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9e3a-126">INPUTS</span></span>

### <span data-ttu-id="c9e3a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c9e3a-127">System.String</span></span>

## <span data-ttu-id="c9e3a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9e3a-128">OUTPUTS</span></span>

### <span data-ttu-id="c9e3a-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="c9e3a-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="c9e3a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9e3a-130">NOTES</span></span>

## <span data-ttu-id="c9e3a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9e3a-131">RELATED LINKS</span></span>
