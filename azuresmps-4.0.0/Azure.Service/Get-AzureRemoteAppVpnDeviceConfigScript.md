---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005831"
---
# <span data-ttu-id="42d63-101">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="42d63-101">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>

## <span data-ttu-id="42d63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42d63-102">SYNOPSIS</span></span>
<span data-ttu-id="42d63-103">Ruft das Konfigurationsskript für ein Azure RemoteApp-VPN-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="42d63-103">Retrieves the configuration script for an Azure RemoteApp VPN device.</span></span>

## <span data-ttu-id="42d63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42d63-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="42d63-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d63-105">DESCRIPTION</span></span>
<span data-ttu-id="42d63-106">Das Cmdlet " **Get-AzureRemoteAppVpnDeviceConfigScript** " Ruft das Konfigurationsskript für ein Azure RemoteApp-VPN-Gerät (virtuelles privates Netzwerk) ab.</span><span class="sxs-lookup"><span data-stu-id="42d63-106">The **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet retrieves the configuration script for an Azure RemoteApp virtual private network (VPN) device.</span></span>

## <span data-ttu-id="42d63-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42d63-107">EXAMPLES</span></span>

### <span data-ttu-id="42d63-108">Beispiel 1: Abrufen eines Konfigurationsskripts für ein VPN-Gerät</span><span class="sxs-lookup"><span data-stu-id="42d63-108">Example 1: Get a configuration script for a VPN device</span></span>
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

<span data-ttu-id="42d63-109">Dieser Befehl gibt das Skript oder die Konfigurationsdatei zurück, das zum Konfigurieren des VPN-Geräts für das virtuelle Netzwerk mit dem Namen ContosoVNet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42d63-109">This command returns the script or configuration file used to configure the VPN device for the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="42d63-110">Diese Skript-oder Konfigurationsdatei sollte auf das VPN-Gerät auf die übliche Weise für dieses Gerät ausgeführt oder geladen werden.</span><span class="sxs-lookup"><span data-stu-id="42d63-110">This script or configuration file should be run or loaded onto the VPN device in the typical manner for that device.</span></span>
<span data-ttu-id="42d63-111">Erkundigen Sie sich beim Hersteller des VPN-Geräts nach den eindeutigen Anforderungen für die einzelnen Geräte.</span><span class="sxs-lookup"><span data-stu-id="42d63-111">Consult the VPN device vendor for the unique requirements for each device.</span></span>

## <span data-ttu-id="42d63-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d63-112">PARAMETERS</span></span>

### <span data-ttu-id="42d63-113">-Einstellung osfamily</span><span class="sxs-lookup"><span data-stu-id="42d63-113">-OSFamily</span></span>
<span data-ttu-id="42d63-114">Gibt die Betriebssystemfamilie an, die auf der Geräteplattform ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42d63-114">Specifies the operating system (OS) family that runs on the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42d63-115">-Plattform</span><span class="sxs-lookup"><span data-stu-id="42d63-115">-Platform</span></span>
<span data-ttu-id="42d63-116">Gibt die Geräteplattform an.</span><span class="sxs-lookup"><span data-stu-id="42d63-116">Specifies the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42d63-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="42d63-117">-Profile</span></span>
<span data-ttu-id="42d63-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="42d63-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="42d63-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="42d63-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42d63-120">-Vendor</span><span class="sxs-lookup"><span data-stu-id="42d63-120">-Vendor</span></span>
<span data-ttu-id="42d63-121">Gibt den Anbieter des VPN-Geräts an.</span><span class="sxs-lookup"><span data-stu-id="42d63-121">Specifies the vendor of the VPN device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42d63-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="42d63-122">-VNetName</span></span>
<span data-ttu-id="42d63-123">Gibt den Namen eines virtuellen Azure RemoteApp-Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="42d63-123">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42d63-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d63-124">CommonParameters</span></span>
<span data-ttu-id="42d63-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d63-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d63-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d63-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d63-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42d63-127">INPUTS</span></span>

## <span data-ttu-id="42d63-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42d63-128">OUTPUTS</span></span>

## <span data-ttu-id="42d63-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="42d63-129">NOTES</span></span>

## <span data-ttu-id="42d63-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42d63-130">RELATED LINKS</span></span>

[<span data-ttu-id="42d63-131">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="42d63-131">Get-AzureRemoteAppVpnDevice</span></span>](./Get-AzureRemoteAppVpnDevice.md)


