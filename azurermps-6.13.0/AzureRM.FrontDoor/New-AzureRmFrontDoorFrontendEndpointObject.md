---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 638617cfe55e01121b46c7fe283d3664948e76b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476061"
---
# <span data-ttu-id="cf2bc-101">New-AzureRmFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="cf2bc-101">New-AzureRmFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="cf2bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2bc-103">Erstellen eines PSFrontendEndpoint-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="cf2bc-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf2bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf2bc-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <PSCertificateSource>]
 [-ProtocolType <PSProtocolType>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <PSCertificateType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf2bc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf2bc-105">DESCRIPTION</span></span>
<span data-ttu-id="cf2bc-106">Erstellen eines PSFrontendEndpoint-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="cf2bc-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="cf2bc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf2bc-107">EXAMPLES</span></span>

### <span data-ttu-id="cf2bc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cf2bc-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


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

<span data-ttu-id="cf2bc-109">Erstellen eines PSFrontendEndpoint-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="cf2bc-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="cf2bc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf2bc-110">PARAMETERS</span></span>

### <span data-ttu-id="cf2bc-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="cf2bc-111">-CertificateSource</span></span>
<span data-ttu-id="cf2bc-112">Die Quelle des SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="cf2bc-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="cf2bc-113">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="cf2bc-113">-CertificateType</span></span>
<span data-ttu-id="cf2bc-114">der Typ des Zertifikats, das für sichere Verbindungen mit einem frontendEndpoint verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf2bc-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="cf2bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf2bc-115">-DefaultProfile</span></span>
<span data-ttu-id="cf2bc-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf2bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2bc-117">-Hostname</span><span class="sxs-lookup"><span data-stu-id="cf2bc-117">-HostName</span></span>
<span data-ttu-id="cf2bc-118">Der Hostname des frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cf2bc-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="cf2bc-119">Muss ein Domänenname sein.</span><span class="sxs-lookup"><span data-stu-id="cf2bc-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="cf2bc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cf2bc-120">-Name</span></span>
<span data-ttu-id="cf2bc-121">Frontend-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="cf2bc-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="cf2bc-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="cf2bc-122">-ProtocolType</span></span>
<span data-ttu-id="cf2bc-123">Das TLS-Erweiterungsprotokoll, das für die sichere Zustellung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="cf2bc-123">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="cf2bc-124">-Secretname</span><span class="sxs-lookup"><span data-stu-id="cf2bc-124">-SecretName</span></span>
<span data-ttu-id="cf2bc-125">Der Name des Schlüssel Tresors, der die vollständige Zertifikat-PFX-Datei darstellt</span><span class="sxs-lookup"><span data-stu-id="cf2bc-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="cf2bc-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="cf2bc-126">-SecretVersion</span></span>
<span data-ttu-id="cf2bc-127">Die Version des Schlüssels Vault Secret, die das vollständige Zertifikat PFX darstellt</span><span class="sxs-lookup"><span data-stu-id="cf2bc-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="cf2bc-128">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="cf2bc-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="cf2bc-129">Gibt an, ob die Sitzungsaffinität für diesen Host zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="cf2bc-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="cf2bc-130">Standardwert ist deaktiviert</span><span class="sxs-lookup"><span data-stu-id="cf2bc-130">Default value is Disabled</span></span>

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

### <span data-ttu-id="cf2bc-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="cf2bc-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="cf2bc-132">Die TTL, die in Sekunden für die Sitzungsaffinität verwendet werden soll (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="cf2bc-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="cf2bc-133">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="cf2bc-133">Default value is 0</span></span>

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

### <span data-ttu-id="cf2bc-134">-Vault</span><span class="sxs-lookup"><span data-stu-id="cf2bc-134">-Vault</span></span>
<span data-ttu-id="cf2bc-135">Der schlüsseltresor mit dem SSL-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="cf2bc-135">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="cf2bc-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="cf2bc-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="cf2bc-137">Die Ressourcen-ID der Webanwendungs-Firewall-Richtlinie für jeden Host (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="cf2bc-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="cf2bc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2bc-138">CommonParameters</span></span>
<span data-ttu-id="cf2bc-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf2bc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf2bc-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf2bc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2bc-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf2bc-141">INPUTS</span></span>

### <span data-ttu-id="cf2bc-142">Keine</span><span class="sxs-lookup"><span data-stu-id="cf2bc-142">None</span></span>

## <span data-ttu-id="cf2bc-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf2bc-143">OUTPUTS</span></span>

### <span data-ttu-id="cf2bc-144">Microsoft. Azure. Commands. Haustür. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf2bc-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="cf2bc-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf2bc-145">NOTES</span></span>

## <span data-ttu-id="cf2bc-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf2bc-146">RELATED LINKS</span></span>

<span data-ttu-id="cf2bc-147">[Neu – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Satz-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="cf2bc-147">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
