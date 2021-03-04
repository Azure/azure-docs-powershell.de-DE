---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 17092ab89ded950678e60b079cd30558f7ce2aac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919739"
---
# <span data-ttu-id="adb81-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="adb81-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="adb81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adb81-102">SYNOPSIS</span></span>
<span data-ttu-id="adb81-103">Ruft die detaillierten Informationen zu aktuellen Punkt-zu-Website-Verbindungen von P2SVpnGateway ab.</span><span class="sxs-lookup"><span data-stu-id="adb81-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="adb81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adb81-104">SYNTAX</span></span>

### <span data-ttu-id="adb81-105">ByP2SVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="adb81-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="adb81-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="adb81-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adb81-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="adb81-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adb81-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="adb81-108">DESCRIPTION</span></span>
<span data-ttu-id="adb81-109">Das **Cmdlet Get-AzP2sVpnGatewayDetailedConnectionHealth** ermöglicht es Ihnen, detaillierte Informationen zu aktuellen Punkt-zu-Website-Verbindungen von P2SVpnGateway zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="adb81-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="adb81-110">Der Kunde muss die SAS-URL übergeben, in der wir diese detaillierten Integritätsinformationen eingeben können.</span><span class="sxs-lookup"><span data-stu-id="adb81-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="adb81-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="adb81-111">EXAMPLES</span></span>

### <span data-ttu-id="adb81-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="adb81-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="adb81-113">Das **Cmdlet Get-AzP2sVpnGatewayDetailedConnectionHealth** ermöglicht es Ihnen, detaillierte Informationen zu aktuellen Punkt-zu-Website-Verbindungen von P2SVpnGateway zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="adb81-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="adb81-114">Der Kunde kann Integritätsdetails aus dem übergebenen SAS-URL-Download herunterladen.</span><span class="sxs-lookup"><span data-stu-id="adb81-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="adb81-115">Dies zeigt Informationen zu jedem Punkt auf die Websiteverbindung mit Benutzernamen, Bytes in, Bytes out, zugewiesene IP-Adresse usw. an.</span><span class="sxs-lookup"><span data-stu-id="adb81-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="adb81-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="adb81-116">PARAMETERS</span></span>

### <span data-ttu-id="adb81-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb81-117">-DefaultProfile</span></span>
<span data-ttu-id="adb81-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="adb81-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb81-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adb81-119">-InputObject</span></span>
<span data-ttu-id="adb81-120">Das zu ändernde p2s-Vpn-Gatewayobjekt</span><span class="sxs-lookup"><span data-stu-id="adb81-120">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adb81-121">-Name</span><span class="sxs-lookup"><span data-stu-id="adb81-121">-Name</span></span>
<span data-ttu-id="adb81-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="adb81-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adb81-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="adb81-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="adb81-124">OutputBlob Sas-URL, in die der p2s-Vpnverbindungszustand geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="adb81-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adb81-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb81-125">-ResourceGroupName</span></span>
<span data-ttu-id="adb81-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="adb81-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adb81-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adb81-127">-ResourceId</span></span>
<span data-ttu-id="adb81-128">Die Azure-Ressourcen-ID des zu ändernden P2SVpnGateways.</span><span class="sxs-lookup"><span data-stu-id="adb81-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adb81-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="adb81-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="adb81-130">Die Liste der zu filternden P2S-Vpn-Benutzernamen.</span><span class="sxs-lookup"><span data-stu-id="adb81-130">The list of P2S vpn user names to filter.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adb81-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb81-131">CommonParameters</span></span>
<span data-ttu-id="adb81-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb81-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb81-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adb81-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb81-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="adb81-134">INPUTS</span></span>

### <span data-ttu-id="adb81-135">System.String</span><span class="sxs-lookup"><span data-stu-id="adb81-135">System.String</span></span>
<span data-ttu-id="adb81-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="adb81-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="adb81-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="adb81-137">OUTPUTS</span></span>

### <span data-ttu-id="adb81-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="adb81-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="adb81-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="adb81-139">NOTES</span></span>

## <span data-ttu-id="adb81-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="adb81-140">RELATED LINKS</span></span>
