---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 62c73fe60e147ca34083851db50c3830198dd60e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841716"
---
# <span data-ttu-id="45601-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="45601-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="45601-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45601-102">SYNOPSIS</span></span>
<span data-ttu-id="45601-103">Ruft ein SSL-Zertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="45601-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="45601-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45601-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45601-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45601-105">DESCRIPTION</span></span>
<span data-ttu-id="45601-106">Das Cmdlet " **Get-AzApplicationGatewaySslCertificate** " Ruft ein SSL-Zertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="45601-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="45601-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45601-107">EXAMPLES</span></span>

### <span data-ttu-id="45601-108">Beispiel 1: Abrufen eines bestimmten SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="45601-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="45601-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="45601-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="45601-110">Der zweite Befehl ruft das SSL-Zertifikat mit dem Namen Cert01 aus dem Anwendungsgateway ab, das in der Variablen mit dem Namen $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="45601-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="45601-111">Der Befehl speichert das Zertifikat in der Variablen mit dem Namen $cert.</span><span class="sxs-lookup"><span data-stu-id="45601-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="45601-112">Beispiel 2: Abrufen einer Liste mit SSL-Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="45601-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="45601-113">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="45601-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="45601-114">Dieser zweite Befehl ruft eine Liste mit SSL-Zertifikaten aus dem Anwendungsgateway ab, die in der Variablen mit dem Namen $AppGW gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="45601-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="45601-115">Der Befehl speichert die Ergebnisse dann in der Variablen mit dem Namen $certs.</span><span class="sxs-lookup"><span data-stu-id="45601-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="45601-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="45601-116">PARAMETERS</span></span>

### <span data-ttu-id="45601-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="45601-117">-ApplicationGateway</span></span>
<span data-ttu-id="45601-118">Gibt das Application Gateway-Objekt an, das das SSL-Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="45601-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45601-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45601-119">-DefaultProfile</span></span>
<span data-ttu-id="45601-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="45601-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45601-121">-Name</span><span class="sxs-lookup"><span data-stu-id="45601-121">-Name</span></span>
<span data-ttu-id="45601-122">Gibt den Namen des SSL-Zertifikat Pools an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="45601-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45601-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45601-123">CommonParameters</span></span>
<span data-ttu-id="45601-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45601-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45601-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45601-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45601-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45601-126">INPUTS</span></span>

### <span data-ttu-id="45601-127">System. String</span><span class="sxs-lookup"><span data-stu-id="45601-127">System.String</span></span>

## <span data-ttu-id="45601-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45601-128">OUTPUTS</span></span>

### <span data-ttu-id="45601-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="45601-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="45601-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="45601-130">NOTES</span></span>

## <span data-ttu-id="45601-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45601-131">RELATED LINKS</span></span>

[<span data-ttu-id="45601-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="45601-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="45601-133">Neu – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="45601-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="45601-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="45601-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="45601-135">Satz-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="45601-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


