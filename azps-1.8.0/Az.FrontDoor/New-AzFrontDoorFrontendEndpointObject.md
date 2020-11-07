---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 6d6253b338bef04c39032bb29b5fb0ba300f4073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820052"
---
# <span data-ttu-id="c6a2b-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="c6a2b-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="c6a2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a2b-103">Erstellen eines PSFrontendEndpoint-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="c6a2b-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="c6a2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6a2b-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <PSCertificateSource>]
 [-ProtocolType <PSProtocolType>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <PSCertificateType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6a2b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a2b-106">Erstellen eines PSFrontendEndpoint-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="c6a2b-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="c6a2b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6a2b-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a2b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6a2b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


HostName                         : frontdoor5.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  : Shared
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
```

<span data-ttu-id="c6a2b-109">Erstellen eines PSFrontendEndpoint-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="c6a2b-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="c6a2b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6a2b-110">PARAMETERS</span></span>

### <span data-ttu-id="c6a2b-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="c6a2b-111">-CertificateSource</span></span>
<span data-ttu-id="c6a2b-112">Die Quelle des SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="c6a2b-112">The source of the SSL certificate</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateSource
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, FrontDoor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a2b-113">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="c6a2b-113">-CertificateType</span></span>
<span data-ttu-id="c6a2b-114">der Typ des Zertifikats, das für sichere Verbindungen mit einem frontendEndpoint verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6a2b-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateType
Parameter Sets: (All)
Aliases:
Accepted values: Shared, Dedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a2b-115">-DefaultProfile</span></span>
<span data-ttu-id="c6a2b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6a2b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6a2b-117">-Hostname</span><span class="sxs-lookup"><span data-stu-id="c6a2b-117">-HostName</span></span>
<span data-ttu-id="c6a2b-118">Der Hostname des frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c6a2b-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="c6a2b-119">Muss ein Domänenname sein.</span><span class="sxs-lookup"><span data-stu-id="c6a2b-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="c6a2b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c6a2b-120">-Name</span></span>
<span data-ttu-id="c6a2b-121">Frontend-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="c6a2b-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="c6a2b-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="c6a2b-122">-ProtocolType</span></span>
<span data-ttu-id="c6a2b-123">Das TLS-Erweiterungsprotokoll, das für die sichere Zustellung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="c6a2b-123">The TLS extension protocol that is used for secure delivery</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocolType
Parameter Sets: (All)
Aliases:
Accepted values: ServerNameIndication, IPBased

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a2b-124">-Secretname</span><span class="sxs-lookup"><span data-stu-id="c6a2b-124">-SecretName</span></span>
<span data-ttu-id="c6a2b-125">Der Name des Schlüssel Tresors, der die vollständige Zertifikat-PFX-Datei darstellt</span><span class="sxs-lookup"><span data-stu-id="c6a2b-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="c6a2b-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="c6a2b-126">-SecretVersion</span></span>
<span data-ttu-id="c6a2b-127">Die Version des Schlüssels Vault Secret, die das vollständige Zertifikat PFX darstellt</span><span class="sxs-lookup"><span data-stu-id="c6a2b-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="c6a2b-128">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="c6a2b-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="c6a2b-129">Gibt an, ob die Sitzungsaffinität für diesen Host zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="c6a2b-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="c6a2b-130">Standardwert ist deaktiviert</span><span class="sxs-lookup"><span data-stu-id="c6a2b-130">Default value is Disabled</span></span>

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

### <span data-ttu-id="c6a2b-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="c6a2b-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="c6a2b-132">Die TTL, die in Sekunden für die Sitzungsaffinität verwendet werden soll (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="c6a2b-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="c6a2b-133">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="c6a2b-133">Default value is 0</span></span>

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

### <span data-ttu-id="c6a2b-134">-Vault</span><span class="sxs-lookup"><span data-stu-id="c6a2b-134">-Vault</span></span>
<span data-ttu-id="c6a2b-135">Der schlüsseltresor mit dem SSL-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="c6a2b-135">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="c6a2b-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="c6a2b-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="c6a2b-137">Die Ressourcen-ID der Webanwendungs-Firewall-Richtlinie für jeden Host (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="c6a2b-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="c6a2b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a2b-138">CommonParameters</span></span>
<span data-ttu-id="c6a2b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a2b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a2b-140">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6a2b-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a2b-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6a2b-141">INPUTS</span></span>

### <span data-ttu-id="c6a2b-142">Keine</span><span class="sxs-lookup"><span data-stu-id="c6a2b-142">None</span></span>

## <span data-ttu-id="c6a2b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6a2b-143">OUTPUTS</span></span>

### <span data-ttu-id="c6a2b-144">Microsoft. Azure. Commands. Haustür. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="c6a2b-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="c6a2b-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6a2b-145">NOTES</span></span>

## <span data-ttu-id="c6a2b-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6a2b-146">RELATED LINKS</span></span>

<span data-ttu-id="c6a2b-147">[Neu – AzFrontDoor](./New-AzFrontDoor.md) 
 [Satz-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="c6a2b-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
