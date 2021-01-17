---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458651"
---
# <span data-ttu-id="39e6b-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="39e6b-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="39e6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="39e6b-103">Erstellen eines "PSFrontendEndpoint-Objekts" für die Erstellung von "Front Door"</span><span class="sxs-lookup"><span data-stu-id="39e6b-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="39e6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39e6b-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39e6b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39e6b-105">DESCRIPTION</span></span>
<span data-ttu-id="39e6b-106">Erstellen eines "PSFrontendEndpoint-Objekts" für die Erstellung von "Front Door"</span><span class="sxs-lookup"><span data-stu-id="39e6b-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="39e6b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39e6b-107">EXAMPLES</span></span>

### <span data-ttu-id="39e6b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39e6b-108">Example 1</span></span>
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

<span data-ttu-id="39e6b-109">Erstellen Sie ein "PSFrontendEndpoint-Objekt" für die Erstellung von "Front Door".</span><span class="sxs-lookup"><span data-stu-id="39e6b-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="39e6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39e6b-110">PARAMETERS</span></span>

### <span data-ttu-id="39e6b-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="39e6b-111">-CertificateSource</span></span>
<span data-ttu-id="39e6b-112">Die Quelle des SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="39e6b-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="39e6b-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="39e6b-113">-CertificateType</span></span>
<span data-ttu-id="39e6b-114">Der Typ des Zertifikats, das für sichere Verbindungen mit einem frontendEndpoint verwendet wird</span><span class="sxs-lookup"><span data-stu-id="39e6b-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="39e6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e6b-115">-DefaultProfile</span></span>
<span data-ttu-id="39e6b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39e6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39e6b-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="39e6b-117">-HostName</span></span>
<span data-ttu-id="39e6b-118">Der Hostname des frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="39e6b-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="39e6b-119">Muss ein Domänenname sein.</span><span class="sxs-lookup"><span data-stu-id="39e6b-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="39e6b-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="39e6b-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="39e6b-121">Die minimale TLS-Version, die von den Clients benötigt wird, um einen SSL-Handshake mit Eingangstür zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39e6b-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="39e6b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="39e6b-122">-Name</span></span>
<span data-ttu-id="39e6b-123">Name des Frontend-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="39e6b-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="39e6b-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="39e6b-124">-ProtocolType</span></span>
<span data-ttu-id="39e6b-125">Das TLS-Erweiterungsprotokoll, das für die sichere Übermittlung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="39e6b-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="39e6b-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="39e6b-126">-SecretName</span></span>
<span data-ttu-id="39e6b-127">Der Name des geheimen Schlüsseltresor, der das vollständige Zertifikat "PFX" darstellt</span><span class="sxs-lookup"><span data-stu-id="39e6b-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="39e6b-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="39e6b-128">-SecretVersion</span></span>
<span data-ttu-id="39e6b-129">Die Version des geheimen Schlüsseltresor, der das vollständige Zertifikat "PFX" darstellt</span><span class="sxs-lookup"><span data-stu-id="39e6b-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="39e6b-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="39e6b-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="39e6b-131">Gibt an, ob sitzungsaffinität auf diesem Host zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="39e6b-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="39e6b-132">Der Standardwert ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="39e6b-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="39e6b-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="39e6b-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="39e6b-134">Die TTL, die in Sekunden für die Sitzungsaffinität verwendet werden soll (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="39e6b-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="39e6b-135">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="39e6b-135">Default value is 0</span></span>

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

### <span data-ttu-id="39e6b-136">-Vault</span><span class="sxs-lookup"><span data-stu-id="39e6b-136">-Vault</span></span>
<span data-ttu-id="39e6b-137">Der Schlüsseltresor mit dem SSL-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="39e6b-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="39e6b-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="39e6b-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="39e6b-139">Die Ressourcen-ID der Webanwendungsfirewallrichtlinie für jeden Host (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="39e6b-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="39e6b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e6b-140">CommonParameters</span></span>
<span data-ttu-id="39e6b-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39e6b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e6b-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39e6b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e6b-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39e6b-143">INPUTS</span></span>

### <span data-ttu-id="39e6b-144">Keine</span><span class="sxs-lookup"><span data-stu-id="39e6b-144">None</span></span>
## <span data-ttu-id="39e6b-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39e6b-145">OUTPUTS</span></span>

### <span data-ttu-id="39e6b-146">Microsoft.Azure.Commands.FrontDando.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="39e6b-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="39e6b-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39e6b-147">NOTES</span></span>

## <span data-ttu-id="39e6b-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39e6b-148">RELATED LINKS</span></span>

<span data-ttu-id="39e6b-149">[New-AzFrontD verankert](./New-AzFrontDoor.md) 
 [Set-AzFrontD verankert](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="39e6b-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
