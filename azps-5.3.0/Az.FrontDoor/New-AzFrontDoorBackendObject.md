---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469808"
---
# <span data-ttu-id="6942f-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="6942f-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="6942f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6942f-102">SYNOPSIS</span></span>
<span data-ttu-id="6942f-103">Erstellen eines "PSBackend"-Objekts</span><span class="sxs-lookup"><span data-stu-id="6942f-103">Create a PSBackend object</span></span>

## <span data-ttu-id="6942f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6942f-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6942f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6942f-105">DESCRIPTION</span></span>
<span data-ttu-id="6942f-106">Erstellen eines "PSBackend"-Objekts für die Erstellung von "Front Door"</span><span class="sxs-lookup"><span data-stu-id="6942f-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="6942f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6942f-107">EXAMPLES</span></span>

### <span data-ttu-id="6942f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6942f-108">Example 1</span></span>
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

<span data-ttu-id="6942f-109">Erstellen eines "PSBackend"-Objekts für die Erstellung von "Front Door"</span><span class="sxs-lookup"><span data-stu-id="6942f-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="6942f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6942f-110">PARAMETERS</span></span>

### <span data-ttu-id="6942f-111">-Address</span><span class="sxs-lookup"><span data-stu-id="6942f-111">-Address</span></span>
<span data-ttu-id="6942f-112">Position des Backends (IP-Adresse oder FQDN)</span><span class="sxs-lookup"><span data-stu-id="6942f-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="6942f-113">-Back-EndHostHeader</span><span class="sxs-lookup"><span data-stu-id="6942f-113">-BackendHostHeader</span></span>
<span data-ttu-id="6942f-114">Der Wert, der als Hostheader verwendet werden soll, der an das Back-End gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="6942f-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="6942f-115">Der Standardwert ist die Back-End-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6942f-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="6942f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6942f-116">-DefaultProfile</span></span>
<span data-ttu-id="6942f-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6942f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6942f-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="6942f-118">-EnabledState</span></span>
<span data-ttu-id="6942f-119">Gibt an, ob die Verwendung dieses Backends aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6942f-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="6942f-120">Der Standardwert ist "Enabled".</span><span class="sxs-lookup"><span data-stu-id="6942f-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="6942f-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="6942f-121">-HttpPort</span></span>
<span data-ttu-id="6942f-122">Die HTTP-TCP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="6942f-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="6942f-123">Muss zwischen 1 und 65535 liegen.</span><span class="sxs-lookup"><span data-stu-id="6942f-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="6942f-124">Der Standardwert ist 80.</span><span class="sxs-lookup"><span data-stu-id="6942f-124">Default value is 80.</span></span>

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

### <span data-ttu-id="6942f-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="6942f-125">-HttpsPort</span></span>
<span data-ttu-id="6942f-126">Die HTTPS-TCP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="6942f-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="6942f-127">Muss zwischen 1 und 65535 liegen.</span><span class="sxs-lookup"><span data-stu-id="6942f-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="6942f-128">Der Standardwert ist 443.</span><span class="sxs-lookup"><span data-stu-id="6942f-128">Default value is 443</span></span>

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

### <span data-ttu-id="6942f-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="6942f-129">-Priority</span></span>
<span data-ttu-id="6942f-130">Priorität für den Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="6942f-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="6942f-131">muss zwischen 1 und 5 liegen.</span><span class="sxs-lookup"><span data-stu-id="6942f-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="6942f-132">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="6942f-132">Default value is 1</span></span>

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

### <span data-ttu-id="6942f-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="6942f-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="6942f-134">Der Alias der Ressource "Privater Link".</span><span class="sxs-lookup"><span data-stu-id="6942f-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="6942f-135">Das Auffüllen dieses optionalen Felds gibt an, dass dieses Back-End "Privat" ist.</span><span class="sxs-lookup"><span data-stu-id="6942f-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="6942f-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="6942f-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="6942f-137">Eine benutzerdefinierte Nachricht, die in die Genehmigungsanforderung eingeschlossen werden soll, um eine Verbindung mit dem privaten Link herzustellen</span><span class="sxs-lookup"><span data-stu-id="6942f-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="6942f-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="6942f-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="6942f-139">Der Speicherort der Ressource "Private Verknüpfung".</span><span class="sxs-lookup"><span data-stu-id="6942f-139">The Location of Private Link resource.</span></span> <span data-ttu-id="6942f-140">Der Speicherort ist erforderlich, wenn "PrivateLinkResourceId" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6942f-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="6942f-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="6942f-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="6942f-142">Die Ressourcen-ID des privaten Links.</span><span class="sxs-lookup"><span data-stu-id="6942f-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="6942f-143">Das Auffüllen dieses optionalen Felds gibt an, dass dieses Back-End "Privat" ist.</span><span class="sxs-lookup"><span data-stu-id="6942f-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="6942f-144">-Weight</span><span class="sxs-lookup"><span data-stu-id="6942f-144">-Weight</span></span>
<span data-ttu-id="6942f-145">Gewichtung dieses Endpunkts zum Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="6942f-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="6942f-146">muss zwischen 1 und 1000 liegen.</span><span class="sxs-lookup"><span data-stu-id="6942f-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="6942f-147">Der Standardwert ist 50.</span><span class="sxs-lookup"><span data-stu-id="6942f-147">Default value is 50</span></span>

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

### <span data-ttu-id="6942f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6942f-148">CommonParameters</span></span>
<span data-ttu-id="6942f-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6942f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6942f-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6942f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6942f-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6942f-151">INPUTS</span></span>

### <span data-ttu-id="6942f-152">Keine</span><span class="sxs-lookup"><span data-stu-id="6942f-152">None</span></span>

## <span data-ttu-id="6942f-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6942f-153">OUTPUTS</span></span>

### <span data-ttu-id="6942f-154">Microsoft.Azure.Commands.FrontDando.Models.PSBackend</span><span class="sxs-lookup"><span data-stu-id="6942f-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="6942f-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6942f-155">NOTES</span></span>

## <span data-ttu-id="6942f-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6942f-156">RELATED LINKS</span></span>

[<span data-ttu-id="6942f-157">New-AzFrontDobjectBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="6942f-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
