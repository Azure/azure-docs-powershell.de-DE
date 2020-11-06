---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1af7ef3b60fa296a5fb8190675393a0726d0502b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479673"
---
# <span data-ttu-id="f5693-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5693-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="f5693-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5693-102">SYNOPSIS</span></span>
<span data-ttu-id="f5693-103">Legt den Zielstatus eines SSL-Zertifikats fest.</span><span class="sxs-lookup"><span data-stu-id="f5693-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5693-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5693-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5693-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5693-105">DESCRIPTION</span></span>
<span data-ttu-id="f5693-106">Das Cmdlet " **Set-AzureRmApplicationGatewaySslCertificate** " legt den Zielstatus eines SSL-Zertifikats fest.</span><span class="sxs-lookup"><span data-stu-id="f5693-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="f5693-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5693-107">EXAMPLES</span></span>

### <span data-ttu-id="f5693-108">Beispiel 1: Festlegung des Zielstatus eines SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="f5693-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="f5693-109">Mit diesem Befehl wird der Zielstatus für ein SSL-Zertifikat vom Anwendungsgateway mit dem Namen ApplicationGateway01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f5693-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="f5693-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5693-110">PARAMETERS</span></span>

### <span data-ttu-id="f5693-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5693-111">-ApplicationGateway</span></span>
<span data-ttu-id="f5693-112">Gibt das Anwendungsgateway an, dem das Secure Socket Layer (SSL)-Zertifikat zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f5693-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="f5693-113">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="f5693-113">-CertificateFile</span></span>
<span data-ttu-id="f5693-114">Gibt den Pfad des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="f5693-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="f5693-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5693-115">-DefaultProfile</span></span>
<span data-ttu-id="f5693-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5693-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5693-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f5693-117">-Name</span></span>
<span data-ttu-id="f5693-118">Gibt den Namen des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="f5693-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="f5693-119">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="f5693-119">-Password</span></span>
<span data-ttu-id="f5693-120">Gibt das Kennwort des SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="f5693-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="f5693-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5693-121">CommonParameters</span></span>
<span data-ttu-id="f5693-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5693-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5693-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5693-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5693-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5693-124">INPUTS</span></span>

### <span data-ttu-id="f5693-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f5693-125">System.String</span></span>

## <span data-ttu-id="f5693-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5693-126">OUTPUTS</span></span>

### <span data-ttu-id="f5693-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5693-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f5693-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5693-128">NOTES</span></span>

## <span data-ttu-id="f5693-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5693-129">RELATED LINKS</span></span>

[<span data-ttu-id="f5693-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5693-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f5693-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5693-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f5693-132">Neu – AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5693-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f5693-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5693-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


