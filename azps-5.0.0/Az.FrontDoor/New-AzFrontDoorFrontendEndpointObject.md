---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177624"
---
# <span data-ttu-id="8fa9a-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="8fa9a-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="8fa9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fa9a-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa9a-103">Erstellen eines PSFrontendEndpoint-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="8fa9a-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="8fa9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fa9a-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fa9a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fa9a-105">DESCRIPTION</span></span>
<span data-ttu-id="8fa9a-106">Erstellen eines PSFrontendEndpoint-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="8fa9a-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="8fa9a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fa9a-107">EXAMPLES</span></span>

### <span data-ttu-id="8fa9a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8fa9a-108">Example 1</span></span>
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

<span data-ttu-id="8fa9a-109">Erstellen Sie ein PSFrontendEndpoint-Objekt für die Haustür Erstellung.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="8fa9a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fa9a-110">PARAMETERS</span></span>

### <span data-ttu-id="8fa9a-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="8fa9a-111">-CertificateSource</span></span>
<span data-ttu-id="8fa9a-112">Die Quelle des SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="8fa9a-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="8fa9a-113">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="8fa9a-113">-CertificateType</span></span>
<span data-ttu-id="8fa9a-114">der Typ des Zertifikats, das für sichere Verbindungen mit einem frontendEndpoint verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="8fa9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa9a-115">-DefaultProfile</span></span>
<span data-ttu-id="8fa9a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fa9a-117">-Hostname</span><span class="sxs-lookup"><span data-stu-id="8fa9a-117">-HostName</span></span>
<span data-ttu-id="8fa9a-118">Der Hostname des frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="8fa9a-119">Muss ein Domänenname sein.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="8fa9a-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8fa9a-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="8fa9a-121">Die für die Clients erforderliche minimale TLS-Version, um einen SSL-Handshake mit Haustür einzurichten.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="8fa9a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8fa9a-122">-Name</span></span>
<span data-ttu-id="8fa9a-123">Frontend-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="8fa9a-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="8fa9a-124">-ProtocolType</span></span>
<span data-ttu-id="8fa9a-125">Das TLS-Erweiterungsprotokoll, das für die sichere Zustellung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="8fa9a-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="8fa9a-126">-Secretname</span><span class="sxs-lookup"><span data-stu-id="8fa9a-126">-SecretName</span></span>
<span data-ttu-id="8fa9a-127">Der Name des Schlüssel Tresors, der die vollständige Zertifikat-PFX-Datei darstellt</span><span class="sxs-lookup"><span data-stu-id="8fa9a-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="8fa9a-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="8fa9a-128">-SecretVersion</span></span>
<span data-ttu-id="8fa9a-129">Die Version des Schlüssels Vault Secret, die das vollständige Zertifikat PFX darstellt</span><span class="sxs-lookup"><span data-stu-id="8fa9a-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="8fa9a-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="8fa9a-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="8fa9a-131">Gibt an, ob die Sitzungsaffinität für diesen Host zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="8fa9a-132">Standardwert ist deaktiviert</span><span class="sxs-lookup"><span data-stu-id="8fa9a-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="8fa9a-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="8fa9a-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="8fa9a-134">Die TTL, die in Sekunden für die Sitzungsaffinität verwendet werden soll (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="8fa9a-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="8fa9a-135">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-135">Default value is 0</span></span>

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

### <span data-ttu-id="8fa9a-136">-Vault</span><span class="sxs-lookup"><span data-stu-id="8fa9a-136">-Vault</span></span>
<span data-ttu-id="8fa9a-137">Der schlüsseltresor mit dem SSL-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="8fa9a-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="8fa9a-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="8fa9a-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="8fa9a-139">Die Ressourcen-ID der Webanwendungs-Firewall-Richtlinie für jeden Host (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="8fa9a-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="8fa9a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa9a-140">CommonParameters</span></span>
<span data-ttu-id="8fa9a-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa9a-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fa9a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa9a-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fa9a-143">INPUTS</span></span>

### <span data-ttu-id="8fa9a-144">Keine</span><span class="sxs-lookup"><span data-stu-id="8fa9a-144">None</span></span>
## <span data-ttu-id="8fa9a-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fa9a-145">OUTPUTS</span></span>

### <span data-ttu-id="8fa9a-146">Microsoft. Azure. Commands. Haustür. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fa9a-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="8fa9a-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fa9a-147">NOTES</span></span>

## <span data-ttu-id="8fa9a-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fa9a-148">RELATED LINKS</span></span>

<span data-ttu-id="8fa9a-149">[Neu – AzFrontDoor](./New-AzFrontDoor.md) 
 [Satz-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="8fa9a-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
