---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CCA6334F-A193-4506-B873-76F29980C68D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25749aca2d0fb2682404d6c4d006c8ad1b1f3c6b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006542"
---
# <span data-ttu-id="e0bf0-101">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="e0bf0-101">Get-AzureLocation</span></span>

## <span data-ttu-id="e0bf0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="e0bf0-103">Ruft die verfügbaren Speicherorte des Datencenters für das aktuelle Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e0bf0-103">Gets the available data center locations for the current Azure subscription.</span></span>

## <span data-ttu-id="e0bf0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0bf0-104">SYNTAX</span></span>

```
Get-AzureLocation [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e0bf0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0bf0-105">DESCRIPTION</span></span>
<span data-ttu-id="e0bf0-106">Das Cmdlet " **Get-AzureLocation** " Ruft eine Liste der verfügbaren Azure-Datencenter und deren Eigenschaften für das aktuelle Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e0bf0-106">The **Get-AzureLocation** cmdlet gets a list of the available Azure data centers and their properties for the current Azure subscription.</span></span>
<span data-ttu-id="e0bf0-107">Bevor Sie dieses Cmdlet ausführen, müssen Sie das aktuelle Abonnement mithilfe der Cmdlets Select-AzureSubscription und Set-AzureSubscription einrichten.</span><span class="sxs-lookup"><span data-stu-id="e0bf0-107">Before you run this cmdlet, you must set your current subscription by using the Select-AzureSubscription and Set-AzureSubscription cmdlets.</span></span>

## <span data-ttu-id="e0bf0-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0bf0-108">EXAMPLES</span></span>

### <span data-ttu-id="e0bf0-109">Beispiel 1: Abrufen von Speicherorten</span><span class="sxs-lookup"><span data-stu-id="e0bf0-109">Example 1: Get locations</span></span>
```
PS C:\> Get-AzureLocation
```

<span data-ttu-id="e0bf0-110">Mit diesem Befehl wird eine Liste der verfügbaren Rechenzentren und deren Eigenschaften für das aktuelle Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e0bf0-110">This command gets a list of available data centers, and their properties, for the current subscription.</span></span>

## <span data-ttu-id="e0bf0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0bf0-111">PARAMETERS</span></span>

### <span data-ttu-id="e0bf0-112">-Information</span><span class="sxs-lookup"><span data-stu-id="e0bf0-112">-InformationAction</span></span>
<span data-ttu-id="e0bf0-113">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="e0bf0-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e0bf0-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e0bf0-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e0bf0-115">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="e0bf0-115">Continue</span></span>
- <span data-ttu-id="e0bf0-116">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="e0bf0-116">Ignore</span></span>
- <span data-ttu-id="e0bf0-117">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="e0bf0-117">Inquire</span></span>
- <span data-ttu-id="e0bf0-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e0bf0-118">SilentlyContinue</span></span>
- <span data-ttu-id="e0bf0-119">Beenden</span><span class="sxs-lookup"><span data-stu-id="e0bf0-119">Stop</span></span>
- <span data-ttu-id="e0bf0-120">Anhalten</span><span class="sxs-lookup"><span data-stu-id="e0bf0-120">Suspend</span></span>

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

### <span data-ttu-id="e0bf0-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e0bf0-121">-InformationVariable</span></span>
<span data-ttu-id="e0bf0-122">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="e0bf0-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e0bf0-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="e0bf0-123">-Profile</span></span>
<span data-ttu-id="e0bf0-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e0bf0-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0bf0-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e0bf0-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0bf0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0bf0-126">CommonParameters</span></span>
<span data-ttu-id="e0bf0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0bf0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0bf0-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0bf0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0bf0-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0bf0-129">INPUTS</span></span>

## <span data-ttu-id="e0bf0-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0bf0-130">OUTPUTS</span></span>

## <span data-ttu-id="e0bf0-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0bf0-131">NOTES</span></span>

## <span data-ttu-id="e0bf0-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0bf0-132">RELATED LINKS</span></span>

