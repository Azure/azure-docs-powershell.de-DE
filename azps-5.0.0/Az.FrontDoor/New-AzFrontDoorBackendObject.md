---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177636"
---
# <span data-ttu-id="4dfd0-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="4dfd0-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="4dfd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4dfd0-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfd0-103">Erstellen eines PSBackend-Objekts</span><span class="sxs-lookup"><span data-stu-id="4dfd0-103">Create a PSBackend object</span></span>

## <span data-ttu-id="4dfd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dfd0-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dfd0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4dfd0-105">DESCRIPTION</span></span>
<span data-ttu-id="4dfd0-106">Erstellen eines PSBackend-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="4dfd0-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="4dfd0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4dfd0-107">EXAMPLES</span></span>

### <span data-ttu-id="4dfd0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4dfd0-108">Example 1</span></span>
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

<span data-ttu-id="4dfd0-109">Erstellen eines PSBackend-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="4dfd0-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="4dfd0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4dfd0-110">PARAMETERS</span></span>

### <span data-ttu-id="4dfd0-111">-Adresse</span><span class="sxs-lookup"><span data-stu-id="4dfd0-111">-Address</span></span>
<span data-ttu-id="4dfd0-112">Speicherort des Back-Ends (IP-Adresse oder FQDN)</span><span class="sxs-lookup"><span data-stu-id="4dfd0-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="4dfd0-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="4dfd0-113">-BackendHostHeader</span></span>
<span data-ttu-id="4dfd0-114">Der Wert, der als Hostheader verwendet werden soll, der an das Back-End gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="4dfd0-115">Der Standardwert ist die Back-End-Adresse.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="4dfd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dfd0-116">-DefaultProfile</span></span>
<span data-ttu-id="4dfd0-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dfd0-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="4dfd0-118">-EnabledState</span></span>
<span data-ttu-id="4dfd0-119">Gibt an, ob die Verwendung dieses Back-Ends aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="4dfd0-120">Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="4dfd0-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="4dfd0-121">-Wert von HTTPPort</span><span class="sxs-lookup"><span data-stu-id="4dfd0-121">-HttpPort</span></span>
<span data-ttu-id="4dfd0-122">Die http-TCP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="4dfd0-123">Muss zwischen 1 und 65535 sein.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="4dfd0-124">Der Standardwert ist 80.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-124">Default value is 80.</span></span>

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

### <span data-ttu-id="4dfd0-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="4dfd0-125">-HttpsPort</span></span>
<span data-ttu-id="4dfd0-126">Die HTTPS-TCP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="4dfd0-127">Muss zwischen 1 und 65535 sein.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="4dfd0-128">Der Standardwert ist 443.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-128">Default value is 443</span></span>

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

### <span data-ttu-id="4dfd0-129">-Priorität</span><span class="sxs-lookup"><span data-stu-id="4dfd0-129">-Priority</span></span>
<span data-ttu-id="4dfd0-130">Die für den Lastenausgleich zu verwendende Priorität.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="4dfd0-131">Muss zwischen 1 und 5 liegen.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="4dfd0-132">Standardwert ist 1</span><span class="sxs-lookup"><span data-stu-id="4dfd0-132">Default value is 1</span></span>

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

### <span data-ttu-id="4dfd0-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="4dfd0-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="4dfd0-134">Der Alias der privaten Link Ressource.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="4dfd0-135">Durch Auffüllen dieses optionalen Felds wird angegeben, dass dieses Back-End "Privat" ist.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="4dfd0-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="4dfd0-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="4dfd0-137">Eine benutzerdefinierte Nachricht, die in die Genehmigungsanforderung aufgenommen werden soll, um eine Verbindung mit dem privaten Link herzustellen</span><span class="sxs-lookup"><span data-stu-id="4dfd0-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="4dfd0-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="4dfd0-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="4dfd0-139">Der Speicherort der Ressource für private Links.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-139">The Location of Private Link resource.</span></span> <span data-ttu-id="4dfd0-140">Speicherort ist erforderlich, wenn PrivateLinkResourceId eingestellt ist</span><span class="sxs-lookup"><span data-stu-id="4dfd0-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="4dfd0-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="4dfd0-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="4dfd0-142">Die Ressourcen-ID des privaten Links.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="4dfd0-143">Durch Auffüllen dieses optionalen Felds wird angegeben, dass dieses Back-End "Privat" ist.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="4dfd0-144">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="4dfd0-144">-Weight</span></span>
<span data-ttu-id="4dfd0-145">Die Gewichtung dieses Endpunkts für Lastenausgleichs Zwecke.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="4dfd0-146">Muss zwischen 1 und 1000 sein.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="4dfd0-147">Der Standardwert ist 50.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-147">Default value is 50</span></span>

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

### <span data-ttu-id="4dfd0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfd0-148">CommonParameters</span></span>
<span data-ttu-id="4dfd0-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dfd0-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dfd0-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dfd0-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4dfd0-151">INPUTS</span></span>

### <span data-ttu-id="4dfd0-152">Keine</span><span class="sxs-lookup"><span data-stu-id="4dfd0-152">None</span></span>

## <span data-ttu-id="4dfd0-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4dfd0-153">OUTPUTS</span></span>

### <span data-ttu-id="4dfd0-154">Microsoft. Azure. Commands. Haustür. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="4dfd0-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="4dfd0-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="4dfd0-155">NOTES</span></span>

## <span data-ttu-id="4dfd0-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4dfd0-156">RELATED LINKS</span></span>

[<span data-ttu-id="4dfd0-157">Neu – AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="4dfd0-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
