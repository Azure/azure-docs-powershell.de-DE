---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010135"
---
# <span data-ttu-id="a2db2-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="a2db2-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="a2db2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2db2-102">SYNOPSIS</span></span>
<span data-ttu-id="a2db2-103">Generiert und downloadet das VPN-Profil auf VirtualWan-VpnServerConfiguration Ebene, um auf den Standort Client Setup zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="a2db2-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="a2db2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2db2-104">SYNTAX</span></span>

### <span data-ttu-id="a2db2-105">ByVirtualWanNameByVpnServerConfigurationObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2db2-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2db2-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a2db2-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2db2-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="a2db2-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2db2-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a2db2-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2db2-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="a2db2-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2db2-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a2db2-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2db2-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2db2-111">DESCRIPTION</span></span>
<span data-ttu-id="a2db2-112">Das Cmdlet " **Get-AzVirtualWanVpnServerConfigurationVpnProfile** " ermöglicht es Ihnen, das VPN-Profil auf VirtualWan-VpnServerConfiguration Ebene zu generieren und herunterzuladen, um auf den Standort Client Setup zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="a2db2-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="a2db2-113">Dies ist für die Verbindung zwischen Point-to-Site-und Site-Client und Azure P2SVpnGateway erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a2db2-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="a2db2-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2db2-114">EXAMPLES</span></span>

### <span data-ttu-id="a2db2-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2db2-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="a2db2-116">Der obige Befehl generiert und gibt die SAS-URL für den Kunden zurück, um das VPN-Profil auf VirtualWan-VpnServerConfiguration Ebene herunterzuladen, um auf den Standort Client Setup zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="a2db2-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="a2db2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2db2-117">PARAMETERS</span></span>

### <span data-ttu-id="a2db2-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="a2db2-118">-AuthenticationMethod</span></span>
<span data-ttu-id="a2db2-119">Authentifizierungsmethode</span><span class="sxs-lookup"><span data-stu-id="a2db2-119">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2db2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2db2-120">-DefaultProfile</span></span>
<span data-ttu-id="a2db2-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2db2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2db2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a2db2-122">-Name</span></span>
<span data-ttu-id="a2db2-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a2db2-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2db2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2db2-124">-ResourceGroupName</span></span>
<span data-ttu-id="a2db2-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a2db2-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2db2-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a2db2-126">-ResourceId</span></span>
<span data-ttu-id="a2db2-127">Die Azure-Ressourcen-ID für das virtuelle WAN.</span><span class="sxs-lookup"><span data-stu-id="a2db2-127">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceIdByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2db2-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="a2db2-128">-VirtualWanObject</span></span>
<span data-ttu-id="a2db2-129">Das virtuelle WAN-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a2db2-129">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2db2-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2db2-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="a2db2-131">Das VpnServerConfiguration, dem dieses VirtualWan zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a2db2-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2db2-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a2db2-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="a2db2-133">Die ID des VPN-Server-Konfiguration-Objekts, dem dieses virtuelle WAN zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a2db2-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationResourceId, ByVirtualWanObjectByVpnServerConfigurationResourceId, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2db2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2db2-134">CommonParameters</span></span>
<span data-ttu-id="a2db2-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2db2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2db2-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2db2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2db2-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2db2-137">INPUTS</span></span>

### <span data-ttu-id="a2db2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a2db2-138">System.String</span></span>
<span data-ttu-id="a2db2-139">Microsoft. Azure. Commands. Network. Models. PSVirtualWan Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2db2-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="a2db2-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2db2-140">OUTPUTS</span></span>

### <span data-ttu-id="a2db2-141">Microsoft. Azure. Commands. Network. Models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="a2db2-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="a2db2-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2db2-142">NOTES</span></span>

## <span data-ttu-id="a2db2-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2db2-143">RELATED LINKS</span></span>
