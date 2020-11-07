---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b68f0bf3b0112587256fddc3dbb6c31605f811b7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843664"
---
# <span data-ttu-id="095f5-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="095f5-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="095f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="095f5-102">SYNOPSIS</span></span>
<span data-ttu-id="095f5-103">Legt den Zielstatus eines SSL-Zertifikats fest.</span><span class="sxs-lookup"><span data-stu-id="095f5-103">Sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="095f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="095f5-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="095f5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="095f5-105">DESCRIPTION</span></span>
<span data-ttu-id="095f5-106">Das Cmdlet " **Set-AzApplicationGatewaySslCertificate** " legt den Zielstatus eines SSL-Zertifikats fest.</span><span class="sxs-lookup"><span data-stu-id="095f5-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="095f5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="095f5-107">EXAMPLES</span></span>

### <span data-ttu-id="095f5-108">Beispiel 1: Festlegung des Zielstatus eines SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="095f5-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="095f5-109">Mit diesem Befehl wird der Zielstatus für ein SSL-Zertifikat vom Anwendungsgateway mit dem Namen ApplicationGateway01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="095f5-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="095f5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="095f5-110">PARAMETERS</span></span>

### <span data-ttu-id="095f5-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="095f5-111">-ApplicationGateway</span></span>
<span data-ttu-id="095f5-112">Gibt das Anwendungsgateway an, dem das Secure Socket Layer (SSL)-Zertifikat zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="095f5-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="095f5-113">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="095f5-113">-CertificateFile</span></span>
<span data-ttu-id="095f5-114">Gibt den Pfad des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="095f5-114">Specifies the path of the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095f5-115">-DefaultProfile</span></span>
<span data-ttu-id="095f5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="095f5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="095f5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="095f5-117">-Name</span></span>
<span data-ttu-id="095f5-118">Gibt den Namen des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="095f5-118">Specifies the name of the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095f5-119">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="095f5-119">-Password</span></span>
<span data-ttu-id="095f5-120">Gibt das Kennwort des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="095f5-120">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095f5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095f5-121">CommonParameters</span></span>
<span data-ttu-id="095f5-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095f5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095f5-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="095f5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095f5-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="095f5-124">INPUTS</span></span>

### <span data-ttu-id="095f5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="095f5-125">System.String</span></span>

## <span data-ttu-id="095f5-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="095f5-126">OUTPUTS</span></span>

### <span data-ttu-id="095f5-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="095f5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="095f5-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="095f5-128">NOTES</span></span>

## <span data-ttu-id="095f5-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="095f5-129">RELATED LINKS</span></span>

[<span data-ttu-id="095f5-130">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="095f5-130">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="095f5-131">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="095f5-131">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="095f5-132">Neu – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="095f5-132">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="095f5-133">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="095f5-133">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


