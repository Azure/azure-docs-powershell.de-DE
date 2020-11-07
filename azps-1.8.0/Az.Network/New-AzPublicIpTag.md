---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 7e4bfae0479d4f37f6a73c8e07239112267ac182
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660491"
---
# <span data-ttu-id="25ee5-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="25ee5-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="25ee5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="25ee5-103">Erstellt ein IP-Tag.</span><span class="sxs-lookup"><span data-stu-id="25ee5-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="25ee5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25ee5-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25ee5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25ee5-105">DESCRIPTION</span></span>
<span data-ttu-id="25ee5-106">Das Cmdlet **New-AzPublicIpTag** erstellt ein IP-Tag.</span><span class="sxs-lookup"><span data-stu-id="25ee5-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="25ee5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25ee5-107">EXAMPLES</span></span>

### <span data-ttu-id="25ee5-108">1: Erstellen eines neuen IP-Tags</span><span class="sxs-lookup"><span data-stu-id="25ee5-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="25ee5-109">Dieser Befehl erstellt ein neues IP-Tag mit dem TagType wie "FirstPartyUsage" und Tag wie "/SQL".</span><span class="sxs-lookup"><span data-stu-id="25ee5-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="25ee5-110">Dieser wird in der publicIpAddress-Erstellung mit diesen speziellen Tags für die Zuweisung verwendet.</span><span class="sxs-lookup"><span data-stu-id="25ee5-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="25ee5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="25ee5-111">PARAMETERS</span></span>

### <span data-ttu-id="25ee5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ee5-112">-DefaultProfile</span></span>
<span data-ttu-id="25ee5-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25ee5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25ee5-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="25ee5-114">-IpTagType</span></span>
<span data-ttu-id="25ee5-115">Beispiel für einen IpTag: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="25ee5-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="25ee5-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="25ee5-116">-Tag</span></span>
<span data-ttu-id="25ee5-117">Beispiel für einen IpTag-Wert:/SQL</span><span class="sxs-lookup"><span data-stu-id="25ee5-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="25ee5-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25ee5-118">-Confirm</span></span>
<span data-ttu-id="25ee5-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25ee5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25ee5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25ee5-120">-WhatIf</span></span>
<span data-ttu-id="25ee5-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25ee5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25ee5-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25ee5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25ee5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ee5-123">CommonParameters</span></span>
<span data-ttu-id="25ee5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25ee5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ee5-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25ee5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ee5-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25ee5-126">INPUTS</span></span>

### <span data-ttu-id="25ee5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="25ee5-127">System.String</span></span>

## <span data-ttu-id="25ee5-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25ee5-128">OUTPUTS</span></span>

### <span data-ttu-id="25ee5-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="25ee5-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="25ee5-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="25ee5-130">NOTES</span></span>

## <span data-ttu-id="25ee5-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25ee5-131">RELATED LINKS</span></span>
