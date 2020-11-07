---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: cec5a6aa0b61889e7923ebce67d1247f99d215e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664472"
---
# <span data-ttu-id="f2552-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f2552-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="f2552-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2552-102">SYNOPSIS</span></span>
<span data-ttu-id="f2552-103">Legt den Zielstatus eines SSL-Zertifikats fest.</span><span class="sxs-lookup"><span data-stu-id="f2552-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2552-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2552-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2552-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2552-105">DESCRIPTION</span></span>
<span data-ttu-id="f2552-106">Das Cmdlet " **Set-AzureRmApplicationGatewaySslCertificate** " legt den Zielstatus eines SSL-Zertifikats fest.</span><span class="sxs-lookup"><span data-stu-id="f2552-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="f2552-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2552-107">EXAMPLES</span></span>

### <span data-ttu-id="f2552-108">Beispiel 1: Festlegung des Zielstatus eines SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="f2552-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="f2552-109">Mit diesem Befehl wird der Zielstatus für ein SSL-Zertifikat vom Anwendungsgateway mit dem Namen ApplicationGateway01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f2552-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="f2552-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2552-110">PARAMETERS</span></span>

### <span data-ttu-id="f2552-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2552-111">-ApplicationGateway</span></span>
<span data-ttu-id="f2552-112">Gibt das Anwendungsgateway an, dem das Secure Socket Layer (SSL)-Zertifikat zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f2552-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2552-113">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="f2552-113">-CertificateFile</span></span>
<span data-ttu-id="f2552-114">Gibt den Pfad des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="f2552-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="f2552-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f2552-115">-Name</span></span>
<span data-ttu-id="f2552-116">Gibt den Namen des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="f2552-116">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="f2552-117">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="f2552-117">-Password</span></span>
<span data-ttu-id="f2552-118">Gibt das Kennwort des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="f2552-118">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="f2552-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2552-119">-DefaultProfile</span></span>
<span data-ttu-id="f2552-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2552-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2552-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2552-121">CommonParameters</span></span>
<span data-ttu-id="f2552-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2552-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2552-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2552-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2552-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2552-124">INPUTS</span></span>

### <span data-ttu-id="f2552-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f2552-125">System.String</span></span>

## <span data-ttu-id="f2552-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2552-126">OUTPUTS</span></span>

### <span data-ttu-id="f2552-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2552-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2552-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2552-128">NOTES</span></span>

## <span data-ttu-id="f2552-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2552-129">RELATED LINKS</span></span>

[<span data-ttu-id="f2552-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f2552-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f2552-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f2552-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f2552-132">Neu – AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f2552-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f2552-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f2552-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


