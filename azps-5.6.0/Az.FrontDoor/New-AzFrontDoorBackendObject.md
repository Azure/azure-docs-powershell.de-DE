---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: d5b7a2d0713fec7c11f33d778cf9708c253f153a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925571"
---
# <span data-ttu-id="72b37-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="72b37-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="72b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72b37-102">SYNOPSIS</span></span>
<span data-ttu-id="72b37-103">Erstellen eines PSBackend-Objekts</span><span class="sxs-lookup"><span data-stu-id="72b37-103">Create a PSBackend object</span></span>

## <span data-ttu-id="72b37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72b37-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72b37-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72b37-105">DESCRIPTION</span></span>
<span data-ttu-id="72b37-106">Erstellen eines PSBackend-Objekts für die Erstellung von Vordertüren</span><span class="sxs-lookup"><span data-stu-id="72b37-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="72b37-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72b37-107">EXAMPLES</span></span>

### <span data-ttu-id="72b37-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72b37-108">Example 1</span></span>
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

<span data-ttu-id="72b37-109">Erstellen eines PSBackend-Objekts für die Erstellung von Vordertüren</span><span class="sxs-lookup"><span data-stu-id="72b37-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="72b37-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="72b37-110">PARAMETERS</span></span>

### <span data-ttu-id="72b37-111">-Adresse</span><span class="sxs-lookup"><span data-stu-id="72b37-111">-Address</span></span>
<span data-ttu-id="72b37-112">Speicherort des Back-Ends (IP-Adresse oder FQDN)</span><span class="sxs-lookup"><span data-stu-id="72b37-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="72b37-113">-Back-EndHostHeader</span><span class="sxs-lookup"><span data-stu-id="72b37-113">-BackendHostHeader</span></span>
<span data-ttu-id="72b37-114">Der Wert, der als Hostheader verwendet werden soll, der an das Back-End gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="72b37-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="72b37-115">Standardwert ist die Back-End-Adresse.</span><span class="sxs-lookup"><span data-stu-id="72b37-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="72b37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b37-116">-DefaultProfile</span></span>
<span data-ttu-id="72b37-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72b37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72b37-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="72b37-118">-EnabledState</span></span>
<span data-ttu-id="72b37-119">Gibt an, ob die Verwendung dieses Back-Ends aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="72b37-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="72b37-120">Standardwert ist Aktiviert</span><span class="sxs-lookup"><span data-stu-id="72b37-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="72b37-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="72b37-121">-HttpPort</span></span>
<span data-ttu-id="72b37-122">Die HTTP-TCP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="72b37-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="72b37-123">Muss zwischen 1 und 65535 liegen.</span><span class="sxs-lookup"><span data-stu-id="72b37-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="72b37-124">Der Standardwert ist 80.</span><span class="sxs-lookup"><span data-stu-id="72b37-124">Default value is 80.</span></span>

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

### <span data-ttu-id="72b37-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="72b37-125">-HttpsPort</span></span>
<span data-ttu-id="72b37-126">Die HTTPS TCP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="72b37-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="72b37-127">Muss zwischen 1 und 65535 liegen.</span><span class="sxs-lookup"><span data-stu-id="72b37-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="72b37-128">Standardwert ist 443</span><span class="sxs-lookup"><span data-stu-id="72b37-128">Default value is 443</span></span>

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

### <span data-ttu-id="72b37-129">-Priorität</span><span class="sxs-lookup"><span data-stu-id="72b37-129">-Priority</span></span>
<span data-ttu-id="72b37-130">Priorität, die für den Lastenausgleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72b37-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="72b37-131">Muss zwischen 1 und 5 liegen.</span><span class="sxs-lookup"><span data-stu-id="72b37-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="72b37-132">Standardwert ist 1</span><span class="sxs-lookup"><span data-stu-id="72b37-132">Default value is 1</span></span>

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

### <span data-ttu-id="72b37-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="72b37-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="72b37-134">Der Alias der Ressource "Privater Link".</span><span class="sxs-lookup"><span data-stu-id="72b37-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="72b37-135">Durch Auffüllen dieses optionalen Felds wird angegeben, dass dieses Back-End "Privat" ist.</span><span class="sxs-lookup"><span data-stu-id="72b37-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="72b37-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="72b37-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="72b37-137">Eine benutzerdefinierte Nachricht, die in die Genehmigungsanforderung aufgenommen werden soll, um eine Verbindung mit dem privaten Link herzustellen</span><span class="sxs-lookup"><span data-stu-id="72b37-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="72b37-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="72b37-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="72b37-139">Der Speicherort der Ressource "Privater Link".</span><span class="sxs-lookup"><span data-stu-id="72b37-139">The Location of Private Link resource.</span></span> <span data-ttu-id="72b37-140">Speicherort ist erforderlich, wenn PrivateLinkResourceId festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="72b37-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="72b37-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="72b37-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="72b37-142">Die Ressourcen-ID des privaten Links.</span><span class="sxs-lookup"><span data-stu-id="72b37-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="72b37-143">Durch Auffüllen dieses optionalen Felds wird angegeben, dass dieses Back-End "Privat" ist.</span><span class="sxs-lookup"><span data-stu-id="72b37-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="72b37-144">-Weight</span><span class="sxs-lookup"><span data-stu-id="72b37-144">-Weight</span></span>
<span data-ttu-id="72b37-145">Gewichtung dieses Endpunkts zum Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="72b37-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="72b37-146">Muss zwischen 1 und 1000 liegen.</span><span class="sxs-lookup"><span data-stu-id="72b37-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="72b37-147">Standardwert ist 50</span><span class="sxs-lookup"><span data-stu-id="72b37-147">Default value is 50</span></span>

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

### <span data-ttu-id="72b37-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b37-148">CommonParameters</span></span>
<span data-ttu-id="72b37-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72b37-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b37-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72b37-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b37-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72b37-151">INPUTS</span></span>

### <span data-ttu-id="72b37-152">Keine</span><span class="sxs-lookup"><span data-stu-id="72b37-152">None</span></span>

## <span data-ttu-id="72b37-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72b37-153">OUTPUTS</span></span>

### <span data-ttu-id="72b37-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span><span class="sxs-lookup"><span data-stu-id="72b37-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="72b37-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="72b37-155">NOTES</span></span>

## <span data-ttu-id="72b37-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="72b37-156">RELATED LINKS</span></span>

[<span data-ttu-id="72b37-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="72b37-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
