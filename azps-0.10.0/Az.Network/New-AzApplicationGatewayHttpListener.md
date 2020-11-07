---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 104a5e022d89421ac960d699c7391db660c0dd6b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841411"
---
# <span data-ttu-id="5707d-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5707d-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5707d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5707d-102">SYNOPSIS</span></span>
<span data-ttu-id="5707d-103">Erstellt einen HTTP-Listener für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5707d-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="5707d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5707d-104">SYNTAX</span></span>

### <span data-ttu-id="5707d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5707d-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5707d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5707d-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5707d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5707d-107">DESCRIPTION</span></span>
<span data-ttu-id="5707d-108">Das Cmdlet **New-AzApplicationGatewayHttpListener** erstellt einen HTTP-Listener für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5707d-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="5707d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5707d-109">EXAMPLES</span></span>

### <span data-ttu-id="5707d-110">Beispiel 1: Erstellen eines HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="5707d-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="5707d-111">Dieser Befehl erstellt einen HTTP-Listener mit dem Namen Listener01 und speichert das Ergebnis in der Variablen mit dem Namen $Listener.</span><span class="sxs-lookup"><span data-stu-id="5707d-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="5707d-112">Beispiel 2: Erstellen eines HTTP-Listener mit SSL</span><span class="sxs-lookup"><span data-stu-id="5707d-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="5707d-113">Dieser Befehl erstellt einen HTTP-Listener, der SSL-Entlastung verwendet und das SSL-Zertifikat in der $SSLCert 01-Variable bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5707d-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="5707d-114">Der Befehl speichert das Ergebnis in der Variablen mit dem Namen $Listener.</span><span class="sxs-lookup"><span data-stu-id="5707d-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="5707d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5707d-115">PARAMETERS</span></span>

### <span data-ttu-id="5707d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5707d-116">-DefaultProfile</span></span>
<span data-ttu-id="5707d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5707d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5707d-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5707d-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="5707d-119">Gibt das Front-End-IP-Konfigurationsobjekt für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="5707d-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5707d-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5707d-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="5707d-121">Gibt die ID der Front-End-IP-Konfiguration für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="5707d-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5707d-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="5707d-122">-FrontendPort</span></span>
<span data-ttu-id="5707d-123">Gibt den Front-End-Port für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="5707d-123">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5707d-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="5707d-124">-FrontendPortId</span></span>
<span data-ttu-id="5707d-125">Gibt die ID des Front-End-Port Objekts für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="5707d-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5707d-126">-Hostname</span><span class="sxs-lookup"><span data-stu-id="5707d-126">-HostName</span></span>
<span data-ttu-id="5707d-127">Gibt den Hostnamen des Application Gateway HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="5707d-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="5707d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="5707d-128">-Name</span></span>
<span data-ttu-id="5707d-129">Gibt den Namen des vom Cmdlet erstellten HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="5707d-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5707d-130">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="5707d-130">-Protocol</span></span>
<span data-ttu-id="5707d-131">Gibt das Protokoll an, das der HTTP-Listener verwendet.</span><span class="sxs-lookup"><span data-stu-id="5707d-131">Specifies the protocol that the HTTP listener uses.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5707d-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="5707d-132">-RequireServerNameIndication</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5707d-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="5707d-133">-SslCertificate</span></span>
<span data-ttu-id="5707d-134">Gibt das SSL-Zertifikatobjekt für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="5707d-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5707d-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="5707d-135">-SslCertificateId</span></span>
<span data-ttu-id="5707d-136">Gibt die ID des SSL-Zertifikats für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="5707d-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5707d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5707d-137">CommonParameters</span></span>
<span data-ttu-id="5707d-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5707d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5707d-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5707d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5707d-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5707d-140">INPUTS</span></span>

### <span data-ttu-id="5707d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5707d-141">System.String</span></span>

## <span data-ttu-id="5707d-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5707d-142">OUTPUTS</span></span>

### <span data-ttu-id="5707d-143">Microsoft. Azure. Commands. Network. Models. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="5707d-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="5707d-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="5707d-144">NOTES</span></span>

## <span data-ttu-id="5707d-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5707d-145">RELATED LINKS</span></span>

[<span data-ttu-id="5707d-146">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5707d-146">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5707d-147">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5707d-147">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5707d-148">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5707d-148">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5707d-149">Satz-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5707d-149">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


