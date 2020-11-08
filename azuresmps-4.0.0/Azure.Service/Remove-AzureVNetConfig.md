---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D903741F-1D22-48FC-BFA5-6876E557EFE5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4284d34ef5151dbcd16d9ed882dcf112abbb8ea5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005698"
---
# <span data-ttu-id="15f57-101">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="15f57-101">Remove-AzureVNetConfig</span></span>

## <span data-ttu-id="15f57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15f57-102">SYNOPSIS</span></span>
<span data-ttu-id="15f57-103">Löscht die Netzwerkkonfiguration aus dem aktuellen Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15f57-103">Deletes the network configuration from the current Azure subscription.</span></span>

## <span data-ttu-id="15f57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15f57-104">SYNTAX</span></span>

```
Remove-AzureVNetConfig [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="15f57-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15f57-105">DESCRIPTION</span></span>
<span data-ttu-id="15f57-106">Das Cmdlet **Remove-AzureVNetConfig** entfernt alle virtuellen Netzwerkeinstellungen aus dem aktuellen Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15f57-106">The **Remove-AzureVNetConfig** cmdlet removes all virtual network settings from the current Azure subscription.</span></span>

## <span data-ttu-id="15f57-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15f57-107">EXAMPLES</span></span>

### <span data-ttu-id="15f57-108">Beispiel 1: Entfernen einer virtuellen Netzwerkkonfiguration aus dem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="15f57-108">Example 1: Remove a virtual network configuration from the current subscription</span></span>
```
PS C:\> Remove-AzureVNetConfig
```

<span data-ttu-id="15f57-109">Mit diesem Befehl wird die Konfiguration des virtuellen Netzwerks aus dem aktuellen Abonnement entfernt.</span><span class="sxs-lookup"><span data-stu-id="15f57-109">This command removes the virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="15f57-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="15f57-110">PARAMETERS</span></span>

### <span data-ttu-id="15f57-111">-Information</span><span class="sxs-lookup"><span data-stu-id="15f57-111">-InformationAction</span></span>
<span data-ttu-id="15f57-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="15f57-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="15f57-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="15f57-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15f57-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="15f57-114">Continue</span></span>
- <span data-ttu-id="15f57-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="15f57-115">Ignore</span></span>
- <span data-ttu-id="15f57-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="15f57-116">Inquire</span></span>
- <span data-ttu-id="15f57-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="15f57-117">SilentlyContinue</span></span>
- <span data-ttu-id="15f57-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="15f57-118">Stop</span></span>
- <span data-ttu-id="15f57-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="15f57-119">Suspend</span></span>

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

### <span data-ttu-id="15f57-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="15f57-120">-InformationVariable</span></span>
<span data-ttu-id="15f57-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="15f57-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="15f57-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="15f57-122">-Profile</span></span>
<span data-ttu-id="15f57-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="15f57-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="15f57-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="15f57-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="15f57-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f57-125">CommonParameters</span></span>
<span data-ttu-id="15f57-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15f57-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f57-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15f57-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f57-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15f57-128">INPUTS</span></span>

## <span data-ttu-id="15f57-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15f57-129">OUTPUTS</span></span>

## <span data-ttu-id="15f57-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="15f57-130">NOTES</span></span>

## <span data-ttu-id="15f57-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15f57-131">RELATED LINKS</span></span>

[<span data-ttu-id="15f57-132">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="15f57-132">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="15f57-133">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="15f57-133">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="15f57-134">Satz-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="15f57-134">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


