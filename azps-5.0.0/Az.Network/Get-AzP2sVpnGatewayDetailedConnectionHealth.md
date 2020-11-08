---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178334"
---
# <span data-ttu-id="3a1e1-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="3a1e1-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="3a1e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a1e1-102">SYNOPSIS</span></span>
<span data-ttu-id="3a1e1-103">Ruft die detaillierten Informationen zu aktuellen Point-to-Site-Verbindungen von P2SVpnGateway ab.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="3a1e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a1e1-104">SYNTAX</span></span>

### <span data-ttu-id="3a1e1-105">ByP2SVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a1e1-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a1e1-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="3a1e1-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1e1-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="3a1e1-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a1e1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a1e1-108">DESCRIPTION</span></span>
<span data-ttu-id="3a1e1-109">Mit dem Cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** können Sie die detaillierten Informationen zu aktuellen Point-to-Site-Verbindungen von P2SVpnGateway abrufen.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="3a1e1-110">Der Kunde muss die SAS-URL weiterleiten, wo wir diese detaillierten Gesundheitsinformationen einfügen können.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="3a1e1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a1e1-111">EXAMPLES</span></span>

### <span data-ttu-id="3a1e1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a1e1-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="3a1e1-113">Mit dem Cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** können Sie die detaillierten Informationen zu aktuellen Point-to-Site-Verbindungen von P2SVpnGateway abrufen.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="3a1e1-114">Der Kunde kann Integritätsinformationen vom übergebenen SAS-URL-Download herunterladen.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="3a1e1-115">Dadurch werden Informationen zu den einzelnen Punkt-zu-Standort-Verbindungen mit Benutzernamen, Bytes in, Bytes aus, zugewiesene IP-Adresse usw. angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="3a1e1-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a1e1-116">PARAMETERS</span></span>

### <span data-ttu-id="3a1e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a1e1-117">-DefaultProfile</span></span>
<span data-ttu-id="3a1e1-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a1e1-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3a1e1-119">-InputObject</span></span>
<span data-ttu-id="3a1e1-120">Das zu ändernde P2S-VPN-Gateway-Objekt</span><span class="sxs-lookup"><span data-stu-id="3a1e1-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="3a1e1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3a1e1-121">-Name</span></span>
<span data-ttu-id="3a1e1-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-122">The resource name.</span></span>

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

### <span data-ttu-id="3a1e1-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="3a1e1-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="3a1e1-124">OutputBlob-SAS-URL, auf die der P2S-VPN-Verbindungsstatus geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="3a1e1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a1e1-125">-ResourceGroupName</span></span>
<span data-ttu-id="3a1e1-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-126">The resource group name.</span></span>

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

### <span data-ttu-id="3a1e1-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3a1e1-127">-ResourceId</span></span>
<span data-ttu-id="3a1e1-128">Die Azure-Ressourcen-ID des zu ändernden P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="3a1e1-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="3a1e1-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="3a1e1-130">Die Liste der zu filternden P2S-VPN-Benutzernamen.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-130">The list of P2S vpn user names to filter.</span></span>

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

### <span data-ttu-id="3a1e1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a1e1-131">CommonParameters</span></span>
<span data-ttu-id="3a1e1-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a1e1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a1e1-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a1e1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a1e1-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a1e1-134">INPUTS</span></span>

### <span data-ttu-id="3a1e1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3a1e1-135">System.String</span></span>
<span data-ttu-id="3a1e1-136">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="3a1e1-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="3a1e1-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a1e1-137">OUTPUTS</span></span>

### <span data-ttu-id="3a1e1-138">Microsoft. Azure. Commands. Network. Models. PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="3a1e1-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="3a1e1-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a1e1-139">NOTES</span></span>

## <span data-ttu-id="3a1e1-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a1e1-140">RELATED LINKS</span></span>
