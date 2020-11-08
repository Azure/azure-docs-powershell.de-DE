---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006515"
---
# <span data-ttu-id="ad3b5-101">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="ad3b5-101">Get-AzureService</span></span>

## <span data-ttu-id="ad3b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad3b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3b5-103">Gibt ein Objekt mit Informationen zu den Cloud-Diensten für das aktuelle Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="ad3b5-103">Returns an object with information about the cloud services for the current subscription.</span></span>

## <span data-ttu-id="ad3b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad3b5-104">SYNTAX</span></span>

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ad3b5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad3b5-105">DESCRIPTION</span></span>
<span data-ttu-id="ad3b5-106">Das Cmdlet " **Get-AzureService** " gibt ein List-Objekt mit allen Azure-Cloud-Diensten zurück, die dem aktuellen Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ad3b5-106">The **Get-AzureService** cmdlet returns a list object with all of the Azure cloud services associated with the current subscription.</span></span>
<span data-ttu-id="ad3b5-107">Wenn Sie den Parameter *ServiceName* angeben, gibt **Get-AzureService** Informationen nur für den übereinstimmenden Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="ad3b5-107">If you specify the *ServiceName* parameter, **Get-AzureService** returns information on only the matching service.</span></span>

## <span data-ttu-id="ad3b5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad3b5-108">EXAMPLES</span></span>

### <span data-ttu-id="ad3b5-109">Beispiel 1: Abrufen von Informationen zu allen Diensten</span><span class="sxs-lookup"><span data-stu-id="ad3b5-109">Example 1: Get information about all services</span></span>
```
PS C:\> Get-AzureService
```

<span data-ttu-id="ad3b5-110">Dieser Befehl gibt ein Objekt zurück, das Informationen zu allen Azure-Diensten enthält, die dem aktuellen Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ad3b5-110">This command returns an object that contains information about all of the Azure services associated with the current subscription.</span></span>

### <span data-ttu-id="ad3b5-111">Beispiel 2: Abrufen von Informationen zu einem bestimmten Dienst</span><span class="sxs-lookup"><span data-stu-id="ad3b5-111">Example 2: Get information about a specified service</span></span>
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

<span data-ttu-id="ad3b5-112">Dieser Befehl gibt Informationen zum $MySvc Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="ad3b5-112">This command returns information about the $MySvc service.</span></span>

### <span data-ttu-id="ad3b5-113">Beispiel 3: Anzeigen verfügbarer Methoden und Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad3b5-113">Example 3: Display available methods and properties</span></span>
```
PS C:\> Get-AzureService | Get-Member
```

<span data-ttu-id="ad3b5-114">Mit diesem Befehl werden die Eigenschaften und Methoden angezeigt, die über das Cmdlet **Get-AzureService** zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ad3b5-114">This command displays the properties and methods that are available from the **Get-AzureService** cmdlet.</span></span>

## <span data-ttu-id="ad3b5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad3b5-115">PARAMETERS</span></span>

### <span data-ttu-id="ad3b5-116">-Information</span><span class="sxs-lookup"><span data-stu-id="ad3b5-116">-InformationAction</span></span>
<span data-ttu-id="ad3b5-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="ad3b5-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ad3b5-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ad3b5-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad3b5-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="ad3b5-119">Continue</span></span>
- <span data-ttu-id="ad3b5-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="ad3b5-120">Ignore</span></span>
- <span data-ttu-id="ad3b5-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="ad3b5-121">Inquire</span></span>
- <span data-ttu-id="ad3b5-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ad3b5-122">SilentlyContinue</span></span>
- <span data-ttu-id="ad3b5-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="ad3b5-123">Stop</span></span>
- <span data-ttu-id="ad3b5-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="ad3b5-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3b5-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ad3b5-125">-InformationVariable</span></span>
<span data-ttu-id="ad3b5-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="ad3b5-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3b5-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="ad3b5-127">-Profile</span></span>
<span data-ttu-id="ad3b5-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ad3b5-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ad3b5-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ad3b5-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3b5-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ad3b5-130">-ServiceName</span></span>
<span data-ttu-id="ad3b5-131">Gibt den Namen eines Diensts an, auf dem Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ad3b5-131">Specifies the name of a service on which to return information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad3b5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3b5-132">CommonParameters</span></span>
<span data-ttu-id="ad3b5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad3b5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3b5-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad3b5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3b5-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad3b5-135">INPUTS</span></span>

## <span data-ttu-id="ad3b5-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad3b5-136">OUTPUTS</span></span>

### <span data-ttu-id="ad3b5-137">HostedServiceContext</span><span class="sxs-lookup"><span data-stu-id="ad3b5-137">HostedServiceContext</span></span>

## <span data-ttu-id="ad3b5-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad3b5-138">NOTES</span></span>

## <span data-ttu-id="ad3b5-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad3b5-139">RELATED LINKS</span></span>

[<span data-ttu-id="ad3b5-140">Neu – AzureService</span><span class="sxs-lookup"><span data-stu-id="ad3b5-140">New-AzureService</span></span>](./New-AzureService.md)

[<span data-ttu-id="ad3b5-141">Satz-AzureService</span><span class="sxs-lookup"><span data-stu-id="ad3b5-141">Set-AzureService</span></span>](./Set-AzureService.md)


