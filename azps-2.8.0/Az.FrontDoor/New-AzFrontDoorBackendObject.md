---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 5cf730c5ba450978730617b7ddb270c0fdec2bf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651129"
---
# <span data-ttu-id="9be09-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="9be09-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="9be09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9be09-102">SYNOPSIS</span></span>
<span data-ttu-id="9be09-103">Erstellen eines PSBackend-Objekts</span><span class="sxs-lookup"><span data-stu-id="9be09-103">Create a PSBackend object</span></span>

## <span data-ttu-id="9be09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9be09-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9be09-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9be09-105">DESCRIPTION</span></span>
<span data-ttu-id="9be09-106">Erstellen eines PSBackend-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="9be09-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="9be09-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9be09-107">EXAMPLES</span></span>

### <span data-ttu-id="9be09-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9be09-108">Example 1</span></span>
```powershell
PS C:\>New-AzFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="9be09-109">Erstellen eines PSBackend-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="9be09-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="9be09-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9be09-110">PARAMETERS</span></span>

### <span data-ttu-id="9be09-111">-Adresse</span><span class="sxs-lookup"><span data-stu-id="9be09-111">-Address</span></span>
<span data-ttu-id="9be09-112">Speicherort des Back-Ends (IP-Adresse oder FQDN)</span><span class="sxs-lookup"><span data-stu-id="9be09-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="9be09-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="9be09-113">-BackendHostHeader</span></span>
<span data-ttu-id="9be09-114">Der Wert, der als Hostheader verwendet werden soll, der an das Back-End gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9be09-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="9be09-115">Der Standardwert ist die Back-End-Adresse.</span><span class="sxs-lookup"><span data-stu-id="9be09-115">Default value is the backend address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9be09-116">-DefaultProfile</span></span>
<span data-ttu-id="9be09-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9be09-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9be09-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="9be09-118">-EnabledState</span></span>
<span data-ttu-id="9be09-119">Gibt an, ob die Verwendung dieses Back-Ends aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9be09-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="9be09-120">Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="9be09-120">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be09-121">-Wert von HTTPPort</span><span class="sxs-lookup"><span data-stu-id="9be09-121">-HttpPort</span></span>
<span data-ttu-id="9be09-122">Die http-TCP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="9be09-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="9be09-123">Muss zwischen 1 und 65535 sein.</span><span class="sxs-lookup"><span data-stu-id="9be09-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="9be09-124">Der Standardwert ist 80.</span><span class="sxs-lookup"><span data-stu-id="9be09-124">Default value is 80.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be09-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="9be09-125">-HttpsPort</span></span>
<span data-ttu-id="9be09-126">Die HTTPS-TCP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="9be09-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="9be09-127">Muss zwischen 1 und 65535 sein.</span><span class="sxs-lookup"><span data-stu-id="9be09-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="9be09-128">Der Standardwert ist 443.</span><span class="sxs-lookup"><span data-stu-id="9be09-128">Default value is 443</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be09-129">-Priorität</span><span class="sxs-lookup"><span data-stu-id="9be09-129">-Priority</span></span>
<span data-ttu-id="9be09-130">Die für den Lastenausgleich zu verwendende Priorität.</span><span class="sxs-lookup"><span data-stu-id="9be09-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="9be09-131">Muss zwischen 1 und 5 liegen.</span><span class="sxs-lookup"><span data-stu-id="9be09-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="9be09-132">Standardwert ist 1</span><span class="sxs-lookup"><span data-stu-id="9be09-132">Default value is 1</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be09-133">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="9be09-133">-Weight</span></span>
<span data-ttu-id="9be09-134">Die Gewichtung dieses Endpunkts für Lastenausgleichs Zwecke.</span><span class="sxs-lookup"><span data-stu-id="9be09-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="9be09-135">Muss zwischen 1 und 1000 sein.</span><span class="sxs-lookup"><span data-stu-id="9be09-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="9be09-136">Der Standardwert ist 50.</span><span class="sxs-lookup"><span data-stu-id="9be09-136">Default value is 50</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be09-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be09-137">CommonParameters</span></span>
<span data-ttu-id="9be09-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9be09-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be09-139">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9be09-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be09-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9be09-140">INPUTS</span></span>

### <span data-ttu-id="9be09-141">Keine</span><span class="sxs-lookup"><span data-stu-id="9be09-141">None</span></span>

## <span data-ttu-id="9be09-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9be09-142">OUTPUTS</span></span>

### <span data-ttu-id="9be09-143">Microsoft. Azure. Commands. Haustür. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="9be09-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="9be09-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="9be09-144">NOTES</span></span>

## <span data-ttu-id="9be09-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9be09-145">RELATED LINKS</span></span>

[<span data-ttu-id="9be09-146">Neu – AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="9be09-146">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
