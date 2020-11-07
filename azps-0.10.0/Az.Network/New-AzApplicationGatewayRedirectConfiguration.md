---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 5cf1e01be8d0a76ba8dc319c5241f40613ad4304
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841399"
---
# <span data-ttu-id="e5810-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5810-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e5810-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5810-102">SYNOPSIS</span></span>
<span data-ttu-id="e5810-103">Erstellt eine Umleitungs Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e5810-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="e5810-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5810-104">SYNTAX</span></span>

### <span data-ttu-id="e5810-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5810-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5810-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e5810-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5810-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="e5810-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5810-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5810-108">DESCRIPTION</span></span>
<span data-ttu-id="e5810-109">**Das Cmdlet New-AzApplicationGatewayRedirectConfiguration** erstellt eine Umleitungs Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e5810-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="e5810-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5810-110">EXAMPLES</span></span>

### <span data-ttu-id="e5810-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5810-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="e5810-112">Dieser Befehl erstellt eine Umleitungs Konfiguration mit dem Namen Redirect01 und speichert das Ergebnis in der Variablen mit dem Namen $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="e5810-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="e5810-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5810-113">PARAMETERS</span></span>

### <span data-ttu-id="e5810-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5810-114">-DefaultProfile</span></span>
<span data-ttu-id="e5810-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5810-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5810-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="e5810-116">-IncludePath</span></span>
<span data-ttu-id="e5810-117">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="e5810-117">Include path in the redirected url.</span></span>
<span data-ttu-id="e5810-118">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="e5810-118">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5810-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="e5810-119">-IncludeQueryString</span></span>
<span data-ttu-id="e5810-120">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="e5810-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="e5810-121">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="e5810-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5810-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e5810-122">-Name</span></span>
<span data-ttu-id="e5810-123">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e5810-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="e5810-124">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="e5810-124">-RedirectType</span></span>
<span data-ttu-id="e5810-125">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="e5810-125">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5810-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="e5810-126">-TargetListener</span></span>
<span data-ttu-id="e5810-127">HTTPListener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="e5810-127">HTTPListener to redirect the request to</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5810-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="e5810-128">-TargetListenerID</span></span>
<span data-ttu-id="e5810-129">Die ID des Listener, an den die Anforderung umgeleitet werden soll</span><span class="sxs-lookup"><span data-stu-id="e5810-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="e5810-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="e5810-130">-TargetUrl</span></span>
<span data-ttu-id="e5810-131">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="e5810-131">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5810-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5810-132">CommonParameters</span></span>
<span data-ttu-id="e5810-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5810-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5810-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5810-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5810-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5810-135">INPUTS</span></span>

### <span data-ttu-id="e5810-136">Keine</span><span class="sxs-lookup"><span data-stu-id="e5810-136">None</span></span>

## <span data-ttu-id="e5810-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5810-137">OUTPUTS</span></span>

### <span data-ttu-id="e5810-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5810-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e5810-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5810-139">NOTES</span></span>

## <span data-ttu-id="e5810-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5810-140">RELATED LINKS</span></span>

