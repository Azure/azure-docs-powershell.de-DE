---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 89106b6474e52863514c65614d334cf5d8382f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665131"
---
# <span data-ttu-id="17e93-101">New-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="17e93-101">New-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="17e93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17e93-102">SYNOPSIS</span></span>
<span data-ttu-id="17e93-103">Mit diesem Befehl können die Benutzer das VPN-IPSec-Parameter Objekt erstellen, das einen oder alle Werte angibt, wie IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup und PfsGroup, die für das vorhandene VPN-Gateway festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="17e93-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17e93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17e93-104">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17e93-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17e93-105">DESCRIPTION</span></span>
<span data-ttu-id="17e93-106">Mit diesem Befehl können die Benutzer das VPN-IPSec-Parameter Objekt erstellen, das einen oder alle Werte angibt, wie IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup und PfsGroup, die für das vorhandene VPN-Gateway festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="17e93-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="17e93-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17e93-107">EXAMPLES</span></span>

### <span data-ttu-id="17e93-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="17e93-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="17e93-109">New-AzureRmVpnClientIpsecParameter-Cmdlet wird zum Erstellen des VPN-IPSec-Parameters-Objekts verwendet, das die Werte der übergebenen oder aller Parameter verwendet, die der Benutzer für ein vorhandenes virtuelles Netzwerkgateway in der ResourceGroup einrichten kann.</span><span class="sxs-lookup"><span data-stu-id="17e93-109">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="17e93-110">Dieses erstellte VpnClientIPsecParameters-Objekt wird an Set-AzureRmVpnClientIpsecParameter Befehl übergeben, um die angegebene VPN-IPSec-benutzerdefinierte Richtlinie auf dem virtuellen Netzwerkgateway festzulegen, wie in obigem Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="17e93-110">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="17e93-111">Dieser Befehl gibt das VpnClientIPsecParameters-Objekt zurück, das die Parameter für "Menge" anzeigt.</span><span class="sxs-lookup"><span data-stu-id="17e93-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="17e93-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="17e93-112">PARAMETERS</span></span>

### <span data-ttu-id="17e93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e93-113">-DefaultProfile</span></span>
<span data-ttu-id="17e93-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17e93-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17e93-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="17e93-115">-DhGroup</span></span>
<span data-ttu-id="17e93-116">Die vpnclient-DH-Gruppen, die in IKE Phase 1 für Initial SA verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17e93-116">The Vpnclient DH Groups used in IKE Phase 1 for initial SA.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e93-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="17e93-117">-IkeEncryption</span></span>
<span data-ttu-id="17e93-118">Der vpnclient-IKE-Verschlüsselungsalgorithmus (IKE-Phase 2)</span><span class="sxs-lookup"><span data-stu-id="17e93-118">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e93-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="17e93-119">-IkeIntegrity</span></span>
<span data-ttu-id="17e93-120">Der vpnclient-IKE-Integritätsalgorithmus (IKE-Phase 2)</span><span class="sxs-lookup"><span data-stu-id="17e93-120">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e93-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="17e93-121">-IpsecEncryption</span></span>
<span data-ttu-id="17e93-122">Der vpnclient IPSec-Verschlüsselungsalgorithmus (IKE-Phase 1)</span><span class="sxs-lookup"><span data-stu-id="17e93-122">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e93-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="17e93-123">-IpsecIntegrity</span></span>
<span data-ttu-id="17e93-124">Der vpnclient-IPSec-Integritätsalgorithmus (IKE-Phase 1)</span><span class="sxs-lookup"><span data-stu-id="17e93-124">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e93-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="17e93-125">-PfsGroup</span></span>
<span data-ttu-id="17e93-126">Die vpnclient-PFS-Gruppen, die in IKE Phase 2 für neue untergeordnete SA verwendet werden</span><span class="sxs-lookup"><span data-stu-id="17e93-126">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e93-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="17e93-127">-SADataSize</span></span>
<span data-ttu-id="17e93-128">Die vpnclient IPSec-Sicherheitszuordnung (auch als Schnellmodus oder Phase 2 SA bezeichnet) Nutzlast-Größe in KB</span><span class="sxs-lookup"><span data-stu-id="17e93-128">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="17e93-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="17e93-129">-SALifeTime</span></span>
<span data-ttu-id="17e93-130">Die vpnclient IPSec-Sicherheitszuordnung (auch als Schnellmodus oder Phase 2 SA bezeichnet) Lebensdauer in Sekunden</span><span class="sxs-lookup"><span data-stu-id="17e93-130">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="17e93-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e93-131">CommonParameters</span></span>
<span data-ttu-id="17e93-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17e93-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e93-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17e93-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e93-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17e93-134">INPUTS</span></span>

### <span data-ttu-id="17e93-135">Keine</span><span class="sxs-lookup"><span data-stu-id="17e93-135">None</span></span>

## <span data-ttu-id="17e93-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17e93-136">OUTPUTS</span></span>

### <span data-ttu-id="17e93-137">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="17e93-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="17e93-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="17e93-138">NOTES</span></span>

## <span data-ttu-id="17e93-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17e93-139">RELATED LINKS</span></span>
