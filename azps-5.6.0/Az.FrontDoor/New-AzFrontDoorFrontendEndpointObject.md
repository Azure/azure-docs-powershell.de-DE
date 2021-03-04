---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: a106295a883cc6729ddf7c5d4235a87ff036f066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928152"
---
# <span data-ttu-id="40450-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="40450-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="40450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40450-102">SYNOPSIS</span></span>
<span data-ttu-id="40450-103">Erstellen eines PSFrontendEndpoint-Objekts für die Erstellung von Vordertüren</span><span class="sxs-lookup"><span data-stu-id="40450-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="40450-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40450-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40450-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40450-105">DESCRIPTION</span></span>
<span data-ttu-id="40450-106">Erstellen eines PSFrontendEndpoint-Objekts für die Erstellung von Vordertüren</span><span class="sxs-lookup"><span data-stu-id="40450-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="40450-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40450-107">EXAMPLES</span></span>

### <span data-ttu-id="40450-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40450-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName "frontendendpoint1"


HostName                         : frontendendpoint1
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                :
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
ProtocolType                     : ServerNameIndication
```

<span data-ttu-id="40450-109">Erstellen Sie ein PSFrontendEndpoint-Objekt für die Erstellung von Vordertüren.</span><span class="sxs-lookup"><span data-stu-id="40450-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="40450-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="40450-110">PARAMETERS</span></span>

### <span data-ttu-id="40450-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="40450-111">-CertificateSource</span></span>
<span data-ttu-id="40450-112">Quelle des SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="40450-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="40450-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="40450-113">-CertificateType</span></span>
<span data-ttu-id="40450-114">der Typ des Zertifikats, das für sichere Verbindungen mit einem frontendEndpoint verwendet wird</span><span class="sxs-lookup"><span data-stu-id="40450-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="40450-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40450-115">-DefaultProfile</span></span>
<span data-ttu-id="40450-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40450-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40450-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="40450-117">-HostName</span></span>
<span data-ttu-id="40450-118">Der Hostname des frontendEndpoints.</span><span class="sxs-lookup"><span data-stu-id="40450-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="40450-119">Muss ein Domänenname sein.</span><span class="sxs-lookup"><span data-stu-id="40450-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="40450-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="40450-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="40450-121">Die mindeste TLS-Version, die von den Clients benötigt wird, um einen SSL-Handshake mit Front Door zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="40450-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="40450-122">-Name</span><span class="sxs-lookup"><span data-stu-id="40450-122">-Name</span></span>
<span data-ttu-id="40450-123">Name des Frontend-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="40450-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="40450-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="40450-124">-ProtocolType</span></span>
<span data-ttu-id="40450-125">Das TLS-Erweiterungsprotokoll, das für die sichere Übermittlung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="40450-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="40450-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="40450-126">-SecretName</span></span>
<span data-ttu-id="40450-127">Der Name des Schlüsseltresorschlüssels, der das vollständige ZERTIFIKAT PFX darstellt</span><span class="sxs-lookup"><span data-stu-id="40450-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="40450-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="40450-128">-SecretVersion</span></span>
<span data-ttu-id="40450-129">Die Version des Schlüsseltresorschlüssels, der das vollständige Zertifikat PFX darstellt</span><span class="sxs-lookup"><span data-stu-id="40450-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="40450-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="40450-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="40450-131">Gibt an, ob die Sitzungsaffinität auf diesem Host zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="40450-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="40450-132">Standardwert ist deaktiviert</span><span class="sxs-lookup"><span data-stu-id="40450-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="40450-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="40450-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="40450-134">Die TTL, die ggf. in Sekunden für die Sitzungsaffinität verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="40450-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="40450-135">Standardwert ist 0</span><span class="sxs-lookup"><span data-stu-id="40450-135">Default value is 0</span></span>

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

### <span data-ttu-id="40450-136">-Vault</span><span class="sxs-lookup"><span data-stu-id="40450-136">-Vault</span></span>
<span data-ttu-id="40450-137">Der Schlüsseltresor, der das SSL-Zertifikat enthält</span><span class="sxs-lookup"><span data-stu-id="40450-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="40450-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="40450-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="40450-139">Die Ressourcen-ID der Webanwendungsfirewallrichtlinie für jeden Host (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="40450-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="40450-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40450-140">CommonParameters</span></span>
<span data-ttu-id="40450-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40450-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40450-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40450-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40450-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40450-143">INPUTS</span></span>

### <span data-ttu-id="40450-144">Keine</span><span class="sxs-lookup"><span data-stu-id="40450-144">None</span></span>
## <span data-ttu-id="40450-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40450-145">OUTPUTS</span></span>

### <span data-ttu-id="40450-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="40450-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="40450-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="40450-147">NOTES</span></span>

## <span data-ttu-id="40450-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="40450-148">RELATED LINKS</span></span>

<span data-ttu-id="40450-149">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="40450-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
