---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845499"
---
# <span data-ttu-id="3fa98-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="3fa98-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="3fa98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3fa98-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa98-103">Erstellen eines PSFrontendEndpoint-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="3fa98-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="3fa98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fa98-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fa98-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fa98-105">DESCRIPTION</span></span>
<span data-ttu-id="3fa98-106">Erstellen eines PSFrontendEndpoint-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="3fa98-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="3fa98-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3fa98-107">EXAMPLES</span></span>

### <span data-ttu-id="3fa98-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3fa98-108">Example 1</span></span>
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

<span data-ttu-id="3fa98-109">Erstellen Sie ein PSFrontendEndpoint-Objekt für die Haustür Erstellung.</span><span class="sxs-lookup"><span data-stu-id="3fa98-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="3fa98-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fa98-110">PARAMETERS</span></span>

### <span data-ttu-id="3fa98-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="3fa98-111">-CertificateSource</span></span>
<span data-ttu-id="3fa98-112">Die Quelle des SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="3fa98-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="3fa98-113">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="3fa98-113">-CertificateType</span></span>
<span data-ttu-id="3fa98-114">der Typ des Zertifikats, das für sichere Verbindungen mit einem frontendEndpoint verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3fa98-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="3fa98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa98-115">-DefaultProfile</span></span>
<span data-ttu-id="3fa98-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3fa98-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fa98-117">-Hostname</span><span class="sxs-lookup"><span data-stu-id="3fa98-117">-HostName</span></span>
<span data-ttu-id="3fa98-118">Der Hostname des frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3fa98-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="3fa98-119">Muss ein Domänenname sein.</span><span class="sxs-lookup"><span data-stu-id="3fa98-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="3fa98-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3fa98-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="3fa98-121">Die für die Clients erforderliche minimale TLS-Version, um einen SSL-Handshake mit Haustür einzurichten.</span><span class="sxs-lookup"><span data-stu-id="3fa98-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="3fa98-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3fa98-122">-Name</span></span>
<span data-ttu-id="3fa98-123">Frontend-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="3fa98-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="3fa98-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="3fa98-124">-ProtocolType</span></span>
<span data-ttu-id="3fa98-125">Das TLS-Erweiterungsprotokoll, das für die sichere Zustellung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="3fa98-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="3fa98-126">-Secretname</span><span class="sxs-lookup"><span data-stu-id="3fa98-126">-SecretName</span></span>
<span data-ttu-id="3fa98-127">Der Name des Schlüssel Tresors, der die vollständige Zertifikat-PFX-Datei darstellt</span><span class="sxs-lookup"><span data-stu-id="3fa98-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="3fa98-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="3fa98-128">-SecretVersion</span></span>
<span data-ttu-id="3fa98-129">Die Version des Schlüssels Vault Secret, die das vollständige Zertifikat PFX darstellt</span><span class="sxs-lookup"><span data-stu-id="3fa98-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="3fa98-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="3fa98-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="3fa98-131">Gibt an, ob die Sitzungsaffinität für diesen Host zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="3fa98-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="3fa98-132">Standardwert ist deaktiviert</span><span class="sxs-lookup"><span data-stu-id="3fa98-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="3fa98-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="3fa98-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="3fa98-134">Die TTL, die in Sekunden für die Sitzungsaffinität verwendet werden soll (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="3fa98-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="3fa98-135">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="3fa98-135">Default value is 0</span></span>

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

### <span data-ttu-id="3fa98-136">-Vault</span><span class="sxs-lookup"><span data-stu-id="3fa98-136">-Vault</span></span>
<span data-ttu-id="3fa98-137">Der schlüsseltresor mit dem SSL-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="3fa98-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="3fa98-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="3fa98-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="3fa98-139">Die Ressourcen-ID der Webanwendungs-Firewall-Richtlinie für jeden Host (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="3fa98-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="3fa98-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa98-140">CommonParameters</span></span>
<span data-ttu-id="3fa98-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fa98-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa98-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fa98-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa98-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3fa98-143">INPUTS</span></span>

### <span data-ttu-id="3fa98-144">Keine</span><span class="sxs-lookup"><span data-stu-id="3fa98-144">None</span></span>
## <span data-ttu-id="3fa98-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3fa98-145">OUTPUTS</span></span>

### <span data-ttu-id="3fa98-146">Microsoft. Azure. Commands. Haustür. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="3fa98-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="3fa98-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="3fa98-147">NOTES</span></span>

## <span data-ttu-id="3fa98-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3fa98-148">RELATED LINKS</span></span>

<span data-ttu-id="3fa98-149">[Neu – AzFrontDoor](./New-AzFrontDoor.md) 
 [Satz-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="3fa98-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
