---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 895F9A5F-D48F-403D-BD8F-72D72D420690
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97bb3e07f5c6df25e7c03c167cc4cb49c25f9414
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005993"
---
# <span data-ttu-id="cb5fa-101">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="cb5fa-101">Set-AzureVNetConfig</span></span>

## <span data-ttu-id="cb5fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5fa-103">Aktualisiert die Einstellungen für das virtuelle Netzwerk für einen Azure Cloud-Dienst.</span><span class="sxs-lookup"><span data-stu-id="cb5fa-103">Updates the virtual network settings for an Azure cloud service.</span></span>

## <span data-ttu-id="cb5fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb5fa-104">SYNTAX</span></span>

```
Set-AzureVNetConfig [-ConfigurationPath] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cb5fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb5fa-105">DESCRIPTION</span></span>
<span data-ttu-id="cb5fa-106">Das Cmdlet " **Satz-AzureVNetConfig** " aktualisiert die Netzwerkkonfiguration für das aktuelle Azure-Abonnement, indem Sie einen Pfad zu einer Netzwerk Konfigurationsdatei (. netcfg) angeben.</span><span class="sxs-lookup"><span data-stu-id="cb5fa-106">The **Set-AzureVNetConfig** cmdlet updates the network configuration for the current Azure subscription by specifying a path to a network configuration file (.netcfg).</span></span>
<span data-ttu-id="cb5fa-107">Die Netzwerk Konfigurationsdatei definiert DNS-Server und-Subnetze für Cloud-Dienste in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb5fa-107">The network configuration file defines DNS servers and subnets for cloud services within a subscription.</span></span>

## <span data-ttu-id="cb5fa-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb5fa-108">EXAMPLES</span></span>

### <span data-ttu-id="cb5fa-109">Beispiel 1: Aktualisieren der Netzwerkkonfiguration des Azure-Abonnements auf eine lokale Datei</span><span class="sxs-lookup"><span data-stu-id="cb5fa-109">Example 1: Update the network configuration of the Azure subscription to a local file</span></span>
```
PS C:\> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="cb5fa-110">Mit diesem Befehl wird die Netzwerkkonfiguration des aktuellen Microsoft Azure-Abonnements in der lokalen Datei "c:\temp\MyAzNets.netcfg" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cb5fa-110">This command updates the network configuration of the current Microsoft Azure subscription to that in the local file "c:\temp\MyAzNets.netcfg".</span></span>

### <span data-ttu-id="cb5fa-111">Beispiel 2: Einrichten des Azure-Abonnements und anschließendes Aktualisieren der Netzwerkkonfiguration</span><span class="sxs-lookup"><span data-stu-id="cb5fa-111">Example 2: Set the Azure subscription and then update the network configuration</span></span>
```
PS C:\> $SubsId = "5bea2bc2-88a5-44b8-abe1-3e76733b6783"
C:\PS> $Cert = Get-Item cert:\LocalMachine\MY\82F105B2DA81149204A6257A9A91EC452B8C52C3
C:\PS> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="cb5fa-112">In diesem Beispiel wird das Microsoft Azure-Abonnement festgelegt, und dann wird die Netzwerkkonfiguration dieses Abonnements unter Verwendung der Konfiguration aktualisiert, die in der lokalen Datei "c:\temp\MyAzNets.netcfg" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cb5fa-112">This example sets the Microsoft Azure subscription, and then updates the network configuration of that subscription using the configuration defined in the local file "c:\temp\MyAzNets.netcfg".</span></span>

## <span data-ttu-id="cb5fa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb5fa-113">PARAMETERS</span></span>

### <span data-ttu-id="cb5fa-114">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="cb5fa-114">-ConfigurationPath</span></span>
<span data-ttu-id="cb5fa-115">Gibt den Pfad und den Dateinamen einer Netzwerk Konfigurationsdatei an (netcfg).</span><span class="sxs-lookup"><span data-stu-id="cb5fa-115">Specifies the path and file name of a network configuration file (.netcfg).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5fa-116">-Information</span><span class="sxs-lookup"><span data-stu-id="cb5fa-116">-InformationAction</span></span>
<span data-ttu-id="cb5fa-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="cb5fa-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cb5fa-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cb5fa-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cb5fa-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="cb5fa-119">Continue</span></span>
- <span data-ttu-id="cb5fa-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="cb5fa-120">Ignore</span></span>
- <span data-ttu-id="cb5fa-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="cb5fa-121">Inquire</span></span>
- <span data-ttu-id="cb5fa-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cb5fa-122">SilentlyContinue</span></span>
- <span data-ttu-id="cb5fa-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="cb5fa-123">Stop</span></span>
- <span data-ttu-id="cb5fa-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="cb5fa-124">Suspend</span></span>

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

### <span data-ttu-id="cb5fa-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cb5fa-125">-InformationVariable</span></span>
<span data-ttu-id="cb5fa-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="cb5fa-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cb5fa-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="cb5fa-127">-Profile</span></span>
<span data-ttu-id="cb5fa-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="cb5fa-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cb5fa-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="cb5fa-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cb5fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5fa-130">CommonParameters</span></span>
<span data-ttu-id="cb5fa-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb5fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5fa-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb5fa-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5fa-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb5fa-133">INPUTS</span></span>

## <span data-ttu-id="cb5fa-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb5fa-134">OUTPUTS</span></span>

## <span data-ttu-id="cb5fa-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb5fa-135">NOTES</span></span>

## <span data-ttu-id="cb5fa-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb5fa-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb5fa-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="cb5fa-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="cb5fa-138">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="cb5fa-138">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="cb5fa-139">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="cb5fa-139">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)


