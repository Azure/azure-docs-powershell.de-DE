---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372573"
---
# <span data-ttu-id="af618-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="af618-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="af618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af618-102">SYNOPSIS</span></span>
<span data-ttu-id="af618-103">Generiert und lädt ein VirtualWan-VpnServerConfiguration A0 für die Einrichtung des Point-to-Site-Clients herunter.</span><span class="sxs-lookup"><span data-stu-id="af618-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="af618-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af618-104">SYNTAX</span></span>

### <span data-ttu-id="af618-105">ByVirtualWanNameByVpnServerConfigurationObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="af618-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af618-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="af618-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af618-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="af618-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af618-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="af618-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af618-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="af618-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af618-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="af618-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af618-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af618-111">DESCRIPTION</span></span>
<span data-ttu-id="af618-112">Mit **dem Cmdlet "Get-AzVirtualWanVpnServerConfigurationVpnProfile"** können Sie das VirtualWan-VpnServerConfiguration-Profil für das Einrichten des Point-to-Site-Clients generieren und herunterladen.</span><span class="sxs-lookup"><span data-stu-id="af618-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="af618-113">Dies ist für die Point-to-Site-Konnektivität vom Point-to-Site-Client zu Azure P2SVpnGateway erforderlich.</span><span class="sxs-lookup"><span data-stu-id="af618-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="af618-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af618-114">EXAMPLES</span></span>

### <span data-ttu-id="af618-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="af618-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="af618-116">Der oben aufgeführte Befehl generiert und gibt SAS-URL für Kunden zurück, um das VirtualWan-VpnServerConfiguration-Profil für die Einrichtung des Websiteclients auf "Verweisen auf" herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="af618-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="af618-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af618-117">PARAMETERS</span></span>

### <span data-ttu-id="af618-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="af618-118">-AuthenticationMethod</span></span>
<span data-ttu-id="af618-119">Authentifizierungsmethode</span><span class="sxs-lookup"><span data-stu-id="af618-119">Authentication Method</span></span>

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

### <span data-ttu-id="af618-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af618-120">-DefaultProfile</span></span>
<span data-ttu-id="af618-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af618-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af618-122">-Name</span><span class="sxs-lookup"><span data-stu-id="af618-122">-Name</span></span>
<span data-ttu-id="af618-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="af618-123">The resource name.</span></span>

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

### <span data-ttu-id="af618-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af618-124">-ResourceGroupName</span></span>
<span data-ttu-id="af618-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="af618-125">The resource group name.</span></span>

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

### <span data-ttu-id="af618-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af618-126">-ResourceId</span></span>
<span data-ttu-id="af618-127">Die Azure-Ressourcen-ID für das virtuelle Wan.</span><span class="sxs-lookup"><span data-stu-id="af618-127">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="af618-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="af618-128">-VirtualWanObject</span></span>
<span data-ttu-id="af618-129">Das virtuelle WAN-Objekt.</span><span class="sxs-lookup"><span data-stu-id="af618-129">The virtual wan object.</span></span>

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

### <span data-ttu-id="af618-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="af618-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="af618-131">Die VpnServerConfiguration, der dieser VirtualWan zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="af618-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

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

### <span data-ttu-id="af618-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="af618-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="af618-133">Die ID des Vpn-Server-Configuraiton-Objekts, dem dieses virtuelle Wan zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="af618-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

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

### <span data-ttu-id="af618-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af618-134">CommonParameters</span></span>
<span data-ttu-id="af618-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af618-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af618-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af618-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af618-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af618-137">INPUTS</span></span>

### <span data-ttu-id="af618-138">System.String</span><span class="sxs-lookup"><span data-stu-id="af618-138">System.String</span></span>
<span data-ttu-id="af618-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="af618-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="af618-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af618-140">OUTPUTS</span></span>

### <span data-ttu-id="af618-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="af618-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="af618-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="af618-142">NOTES</span></span>

## <span data-ttu-id="af618-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="af618-143">RELATED LINKS</span></span>
