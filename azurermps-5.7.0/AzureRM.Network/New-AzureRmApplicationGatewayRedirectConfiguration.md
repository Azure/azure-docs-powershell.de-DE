---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 0d2d9d9390f60c7d7eb74061a52b9b437acdf772
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479702"
---
# <span data-ttu-id="8f7d6-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f7d6-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="8f7d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f7d6-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7d6-103">Erstellt eine Umleitungs Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8f7d6-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f7d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f7d6-104">SYNTAX</span></span>

### <span data-ttu-id="8f7d6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f7d6-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f7d6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8f7d6-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f7d6-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="8f7d6-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f7d6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f7d6-108">DESCRIPTION</span></span>
<span data-ttu-id="8f7d6-109">**Das Cmdlet New-AzureRmApplicationGatewayRedirectConfiguration** erstellt eine Umleitungs Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8f7d6-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="8f7d6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f7d6-110">EXAMPLES</span></span>

### <span data-ttu-id="8f7d6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f7d6-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="8f7d6-112">Dieser Befehl erstellt eine Umleitungs Konfiguration mit dem Namen Redirect01 und speichert das Ergebnis in der Variablen mit dem Namen $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="8f7d6-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="8f7d6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f7d6-113">PARAMETERS</span></span>

### <span data-ttu-id="8f7d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7d6-114">-DefaultProfile</span></span>
<span data-ttu-id="8f7d6-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f7d6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f7d6-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="8f7d6-116">-IncludePath</span></span>
<span data-ttu-id="8f7d6-117">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="8f7d6-117">Include path in the redirected url.</span></span>
<span data-ttu-id="8f7d6-118">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="8f7d6-118">Default is true.</span></span>

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

### <span data-ttu-id="8f7d6-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="8f7d6-119">-IncludeQueryString</span></span>
<span data-ttu-id="8f7d6-120">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="8f7d6-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="8f7d6-121">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="8f7d6-121">Default is true.</span></span>

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

### <span data-ttu-id="8f7d6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8f7d6-122">-Name</span></span>
<span data-ttu-id="8f7d6-123">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="8f7d6-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="8f7d6-124">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="8f7d6-124">-RedirectType</span></span>
<span data-ttu-id="8f7d6-125">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="8f7d6-125">The type of redirect</span></span>

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

### <span data-ttu-id="8f7d6-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="8f7d6-126">-TargetListener</span></span>
<span data-ttu-id="8f7d6-127">HTTPListener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="8f7d6-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="8f7d6-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="8f7d6-128">-TargetListenerID</span></span>
<span data-ttu-id="8f7d6-129">Die ID des Listener, an den die Anforderung umgeleitet werden soll</span><span class="sxs-lookup"><span data-stu-id="8f7d6-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="8f7d6-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="8f7d6-130">-TargetUrl</span></span>
<span data-ttu-id="8f7d6-131">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="8f7d6-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="8f7d6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7d6-132">CommonParameters</span></span>
<span data-ttu-id="8f7d6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7d6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7d6-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f7d6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7d6-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f7d6-135">INPUTS</span></span>

### <span data-ttu-id="8f7d6-136">Keine</span><span class="sxs-lookup"><span data-stu-id="8f7d6-136">None</span></span>

## <span data-ttu-id="8f7d6-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f7d6-137">OUTPUTS</span></span>

### <span data-ttu-id="8f7d6-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f7d6-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="8f7d6-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f7d6-139">NOTES</span></span>

## <span data-ttu-id="8f7d6-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f7d6-140">RELATED LINKS</span></span>

