---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 7f3834e13ce6fb6c3e9a661fead09ffcfab78933
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502665"
---
# <span data-ttu-id="3fc92-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fc92-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="3fc92-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3fc92-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc92-103">Erstellt eine Umleitungs Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="3fc92-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fc92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fc92-104">SYNTAX</span></span>

### <span data-ttu-id="3fc92-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3fc92-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fc92-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3fc92-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fc92-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="3fc92-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3fc92-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fc92-108">DESCRIPTION</span></span>
<span data-ttu-id="3fc92-109">**Das Cmdlet New-AzureRmApplicationGatewayRedirectConfiguration** erstellt eine Umleitungs Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="3fc92-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="3fc92-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3fc92-110">EXAMPLES</span></span>

### <span data-ttu-id="3fc92-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3fc92-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="3fc92-112">Dieser Befehl erstellt eine Umleitungs Konfiguration mit dem Namen Redirect01 und speichert das Ergebnis in der Variablen mit dem Namen $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="3fc92-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="3fc92-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fc92-113">PARAMETERS</span></span>

### <span data-ttu-id="3fc92-114">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="3fc92-114">-IncludePath</span></span>
<span data-ttu-id="3fc92-115">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="3fc92-115">Include path in the redirected url.</span></span>
<span data-ttu-id="3fc92-116">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="3fc92-116">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc92-117">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="3fc92-117">-IncludeQueryString</span></span>
<span data-ttu-id="3fc92-118">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="3fc92-118">Include query string in the redirected url.</span></span>
<span data-ttu-id="3fc92-119">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="3fc92-119">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc92-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3fc92-120">-Name</span></span>
<span data-ttu-id="3fc92-121">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="3fc92-121">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="3fc92-122">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="3fc92-122">-RedirectType</span></span>
<span data-ttu-id="3fc92-123">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="3fc92-123">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc92-124">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="3fc92-124">-TargetListener</span></span>
<span data-ttu-id="3fc92-125">HTTPListener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="3fc92-125">HTTPListener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc92-126">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="3fc92-126">-TargetListenerID</span></span>
<span data-ttu-id="3fc92-127">Die ID des Listener, an den die Anforderung umgeleitet werden soll</span><span class="sxs-lookup"><span data-stu-id="3fc92-127">ID of  listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc92-128">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="3fc92-128">-TargetUrl</span></span>
<span data-ttu-id="3fc92-129">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="3fc92-129">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc92-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc92-130">-DefaultProfile</span></span>
<span data-ttu-id="3fc92-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3fc92-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fc92-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc92-132">CommonParameters</span></span>
<span data-ttu-id="3fc92-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fc92-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc92-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fc92-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc92-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3fc92-135">INPUTS</span></span>

### <span data-ttu-id="3fc92-136">Keine</span><span class="sxs-lookup"><span data-stu-id="3fc92-136">None</span></span>

## <span data-ttu-id="3fc92-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3fc92-137">OUTPUTS</span></span>

### <span data-ttu-id="3fc92-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fc92-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="3fc92-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="3fc92-139">NOTES</span></span>

## <span data-ttu-id="3fc92-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3fc92-140">RELATED LINKS</span></span>

