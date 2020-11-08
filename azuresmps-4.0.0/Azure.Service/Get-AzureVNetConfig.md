---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F34910FA-B024-4C1C-B040-671C8962C49D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 558d714c432efd1dbd8f11feb09b0bbde035e2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006494"
---
# <span data-ttu-id="6652a-101">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="6652a-101">Get-AzureVNetConfig</span></span>

## <span data-ttu-id="6652a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6652a-102">SYNOPSIS</span></span>
<span data-ttu-id="6652a-103">Ruft die Azure Virtual Network-Konfiguration aus dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="6652a-103">Gets the Azure virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="6652a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6652a-104">SYNTAX</span></span>

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6652a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6652a-105">DESCRIPTION</span></span>
<span data-ttu-id="6652a-106">Das Cmdlet " **Get-AzureVNetConfig** " Ruft die virtuelle Netzwerkkonfiguration des aktuellen Azure-Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="6652a-106">The **Get-AzureVNetConfig** cmdlet retrieves the virtual network configuration of the current Azure subscription.</span></span>
<span data-ttu-id="6652a-107">Wenn der Parameter *ExportToFile* angegeben wird, wird eine Netzwerk Konfigurationsdatei erstellt.</span><span class="sxs-lookup"><span data-stu-id="6652a-107">If the *ExportToFile* parameter is specified, a network configuration file is created.</span></span>

## <span data-ttu-id="6652a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6652a-108">EXAMPLES</span></span>

### <span data-ttu-id="6652a-109">Beispiel 1: Abrufen der virtuellen Netzwerkkonfiguration eines aktuellen Azure-Abonnements</span><span class="sxs-lookup"><span data-stu-id="6652a-109">Example 1: Get the virtual network configuration of a current Azure subscription</span></span>
```
PS C:\> Get-AzureVNetConfig
```

<span data-ttu-id="6652a-110">Mit diesem Befehl wird die virtuelle Netzwerkkonfiguration des aktuellen Azure-Abonnements abgerufen und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6652a-110">This command gets the virtual network configuration of the current Azure subscription and displays it.</span></span>

### <span data-ttu-id="6652a-111">Beispiel 2: Abrufen der virtuellen Netzwerkkonfiguration des aktuellen Azure-Abonnements und speichern in einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="6652a-111">Example 2: Get the virtual network configuration of the current Azure subscription and save it to a local file</span></span>
```
PS C:\> Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="6652a-112">Mit diesem Befehl wird die virtuelle Netzwerkkonfiguration des aktuellen Azure-Abonnements abgerufen und dann in einer lokalen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6652a-112">This command gets the virtual network configuration of the current Azure subscription and then saves it to a local file.</span></span>

## <span data-ttu-id="6652a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6652a-113">PARAMETERS</span></span>

### <span data-ttu-id="6652a-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="6652a-114">-ExportToFile</span></span>
<span data-ttu-id="6652a-115">Gibt den Pfad und den Dateinamen einer Netzwerk Konfigurationsdatei an, die aus den Einstellungen erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6652a-115">Specifies the path and file name of a network configuration file to be created from the settings.</span></span>

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

### <span data-ttu-id="6652a-116">-Information</span><span class="sxs-lookup"><span data-stu-id="6652a-116">-InformationAction</span></span>
<span data-ttu-id="6652a-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="6652a-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6652a-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6652a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6652a-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="6652a-119">Continue</span></span>
- <span data-ttu-id="6652a-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="6652a-120">Ignore</span></span>
- <span data-ttu-id="6652a-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="6652a-121">Inquire</span></span>
- <span data-ttu-id="6652a-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6652a-122">SilentlyContinue</span></span>
- <span data-ttu-id="6652a-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="6652a-123">Stop</span></span>
- <span data-ttu-id="6652a-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="6652a-124">Suspend</span></span>

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

### <span data-ttu-id="6652a-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6652a-125">-InformationVariable</span></span>
<span data-ttu-id="6652a-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="6652a-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6652a-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="6652a-127">-Profile</span></span>
<span data-ttu-id="6652a-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6652a-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6652a-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6652a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6652a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6652a-130">CommonParameters</span></span>
<span data-ttu-id="6652a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6652a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6652a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6652a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6652a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6652a-133">INPUTS</span></span>

## <span data-ttu-id="6652a-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6652a-134">OUTPUTS</span></span>

## <span data-ttu-id="6652a-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="6652a-135">NOTES</span></span>

## <span data-ttu-id="6652a-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6652a-136">RELATED LINKS</span></span>

[<span data-ttu-id="6652a-137">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="6652a-137">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="6652a-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="6652a-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="6652a-139">Satz-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="6652a-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


