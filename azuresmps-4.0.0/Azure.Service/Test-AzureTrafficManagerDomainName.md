---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006141"
---
# <span data-ttu-id="c2324-101">Test-AzureTrafficManagerDomainName</span><span class="sxs-lookup"><span data-stu-id="c2324-101">Test-AzureTrafficManagerDomainName</span></span>

## <span data-ttu-id="c2324-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2324-102">SYNOPSIS</span></span>
<span data-ttu-id="c2324-103">Überprüft, ob ein Domänenname als Datenverkehrs-Manager-Profil verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c2324-103">Checks whether a domain name is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="c2324-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2324-104">SYNTAX</span></span>

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c2324-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2324-105">DESCRIPTION</span></span>
<span data-ttu-id="c2324-106">Das Cmdlet **Test-AzureTrafficManagerDomainName** überprüft, ob ein Domänenname als Microsoft Azure Traffic Manager-Profil verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c2324-106">The **Test-AzureTrafficManagerDomainName** cmdlet checks whether a domain name is available as a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="c2324-107">Wenn der Domänenname verfügbar ist, gibt dieses Cmdlet den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="c2324-107">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="c2324-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2324-108">EXAMPLES</span></span>

### <span data-ttu-id="c2324-109">Beispiel 1: überprüfen, ob ein Domänenname verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="c2324-109">Example 1: Check whether a domain name is available</span></span>
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

<span data-ttu-id="c2324-110">Dieser Befehl überprüft, ob der Domänenname ContosoApp.Trafficmanager.net als Datenverkehrs-Manager-Profil verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c2324-110">This command checks whether the domain name ContosoApp.trafficmanager.net is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="c2324-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2324-111">PARAMETERS</span></span>

### <span data-ttu-id="c2324-112">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="c2324-112">-DomainName</span></span>
<span data-ttu-id="c2324-113">Gibt den zu überprüfenden Domänennamen an.</span><span class="sxs-lookup"><span data-stu-id="c2324-113">Specifies the domain name to test.</span></span>
<span data-ttu-id="c2324-114">Sie müssen die folgende Zeichenfolge einbeziehen:</span><span class="sxs-lookup"><span data-stu-id="c2324-114">You must include the following string:</span></span> 

<span data-ttu-id="c2324-115">. Trafficmanager.net</span><span class="sxs-lookup"><span data-stu-id="c2324-115">.trafficmanager.net</span></span>

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

### <span data-ttu-id="c2324-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="c2324-116">-Profile</span></span>
<span data-ttu-id="c2324-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c2324-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c2324-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c2324-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c2324-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2324-119">CommonParameters</span></span>
<span data-ttu-id="c2324-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2324-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2324-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2324-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2324-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2324-122">INPUTS</span></span>

## <span data-ttu-id="c2324-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2324-123">OUTPUTS</span></span>

### <span data-ttu-id="c2324-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2324-124">System.Boolean</span></span>
<span data-ttu-id="c2324-125">Dieses Cmdlet generiert $true oder $false.</span><span class="sxs-lookup"><span data-stu-id="c2324-125">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="c2324-126">Wenn der Domänenname verfügbar ist, gibt dieses Cmdlet den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="c2324-126">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="c2324-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2324-127">NOTES</span></span>

## <span data-ttu-id="c2324-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2324-128">RELATED LINKS</span></span>

