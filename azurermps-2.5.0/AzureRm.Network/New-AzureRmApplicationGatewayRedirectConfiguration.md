---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 2cb7455d5a902882fdd98dd5fea47ae5a28e1dc9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848135"
---
# <span data-ttu-id="14813-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="14813-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="14813-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14813-102">SYNOPSIS</span></span>
<span data-ttu-id="14813-103">Erstellt eine Umleitungs Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="14813-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14813-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14813-104">SYNTAX</span></span>

### <span data-ttu-id="14813-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="14813-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14813-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="14813-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14813-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="14813-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14813-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14813-108">DESCRIPTION</span></span>
<span data-ttu-id="14813-109">**Das Cmdlet New-AzureRmApplicationGatewayRedirectConfiguration** erstellt eine Umleitungs Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="14813-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="14813-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14813-110">EXAMPLES</span></span>

### <span data-ttu-id="14813-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="14813-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="14813-112">Dieser Befehl erstellt eine Umleitungs Konfiguration mit dem Namen Redirect01 und speichert das Ergebnis in der Variablen mit dem Namen $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="14813-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="14813-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="14813-113">PARAMETERS</span></span>

### <span data-ttu-id="14813-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14813-114">-DefaultProfile</span></span>
<span data-ttu-id="14813-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="14813-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14813-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="14813-116">-IncludePath</span></span>
<span data-ttu-id="14813-117">Fügen Sie den Pfad in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="14813-117">Include path in the redirected url.</span></span>
<span data-ttu-id="14813-118">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="14813-118">Default is true.</span></span>

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

### <span data-ttu-id="14813-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="14813-119">-IncludeQueryString</span></span>
<span data-ttu-id="14813-120">Fügen Sie Abfragezeichenfolge in die umgeleitete URL ein.</span><span class="sxs-lookup"><span data-stu-id="14813-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="14813-121">Der Standardwert ist wahr.</span><span class="sxs-lookup"><span data-stu-id="14813-121">Default is true.</span></span>

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

### <span data-ttu-id="14813-122">-Name</span><span class="sxs-lookup"><span data-stu-id="14813-122">-Name</span></span>
<span data-ttu-id="14813-123">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="14813-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="14813-124">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="14813-124">-RedirectType</span></span>
<span data-ttu-id="14813-125">Der Typ der Umleitung</span><span class="sxs-lookup"><span data-stu-id="14813-125">The type of redirect</span></span>

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

### <span data-ttu-id="14813-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="14813-126">-TargetListener</span></span>
<span data-ttu-id="14813-127">HTTPListener zum Umleiten der Anforderung an</span><span class="sxs-lookup"><span data-stu-id="14813-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="14813-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="14813-128">-TargetListenerID</span></span>
<span data-ttu-id="14813-129">Die ID des Listener, an den die Anforderung umgeleitet werden soll</span><span class="sxs-lookup"><span data-stu-id="14813-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="14813-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="14813-130">-TargetUrl</span></span>
<span data-ttu-id="14813-131">Ziel-URL FO-Umleitung</span><span class="sxs-lookup"><span data-stu-id="14813-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="14813-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14813-132">CommonParameters</span></span>
<span data-ttu-id="14813-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14813-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14813-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14813-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14813-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14813-135">INPUTS</span></span>

### <span data-ttu-id="14813-136">Keine</span><span class="sxs-lookup"><span data-stu-id="14813-136">None</span></span>

## <span data-ttu-id="14813-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14813-137">OUTPUTS</span></span>

### <span data-ttu-id="14813-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="14813-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="14813-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="14813-139">NOTES</span></span>

## <span data-ttu-id="14813-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14813-140">RELATED LINKS</span></span>

