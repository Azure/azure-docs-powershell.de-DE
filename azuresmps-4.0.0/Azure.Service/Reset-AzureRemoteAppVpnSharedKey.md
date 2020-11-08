---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005677"
---
# <span data-ttu-id="3eb28-101">Reset-AzureRemoteAppVpnSharedKey</span><span class="sxs-lookup"><span data-stu-id="3eb28-101">Reset-AzureRemoteAppVpnSharedKey</span></span>

## <span data-ttu-id="3eb28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3eb28-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb28-103">Der freigegebene Azure RemoteApp-VPN-Schlüssel wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3eb28-103">Resets the Azure RemoteApp VPN shared key.</span></span>

## <span data-ttu-id="3eb28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3eb28-104">SYNTAX</span></span>

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3eb28-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3eb28-105">DESCRIPTION</span></span>
<span data-ttu-id="3eb28-106">Mit dem Cmdlet **Reset-AzureRemoteAppVpnSharedKey** wird der freigegebene Schlüssel Azure RemoteApp-VPN (virtuelles privates Netzwerk) zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3eb28-106">The **Reset-AzureRemoteAppVpnSharedKey** cmdlet resets the Azure RemoteApp virtual private network (VPN) shared key.</span></span>

## <span data-ttu-id="3eb28-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3eb28-107">EXAMPLES</span></span>

### <span data-ttu-id="3eb28-108">Beispiel 1: Zurücksetzen des freigegebenen Schlüssels in einem virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="3eb28-108">Example 1: Reset the shared key on a virtual network</span></span>
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

<span data-ttu-id="3eb28-109">Mit diesem Befehl wird der freigegebene Schlüssel im virtuellen Netzwerk mit dem Namen ContosoVNet zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3eb28-109">This command resets the shared key on the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="3eb28-110">Die VPN-Verbindung mit dem lokalen Netzwerk bleibt offline, bis der neue freigegebene Schlüssel auf dem VPN-Gerät konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="3eb28-110">The VPN connection to the on-premises network remains offline until the new shared key is configured on the VPN device.</span></span>
<span data-ttu-id="3eb28-111">Verwenden Sie zum Konfigurieren des VPN-Geräts das Cmdlet " **Get-AzureRemoteAppVpnDeviceConfigScript** ", um das richtige Skript oder die richtige Konfigurationsdatei für Ihr VPN-Gerät abzurufen, und laden Sie dann das Skript oder die Konfigurationsdatei auf das VPN-Gerät.</span><span class="sxs-lookup"><span data-stu-id="3eb28-111">To configure the VPN device, use the **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet to retrieve the correct script or configuration file for your VPN device, then load that script or configuration file onto the VPN device.</span></span>

## <span data-ttu-id="3eb28-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3eb28-112">PARAMETERS</span></span>

### <span data-ttu-id="3eb28-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="3eb28-113">-Profile</span></span>
<span data-ttu-id="3eb28-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3eb28-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3eb28-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3eb28-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3eb28-116">-VNetName</span><span class="sxs-lookup"><span data-stu-id="3eb28-116">-VNetName</span></span>
<span data-ttu-id="3eb28-117">Gibt den Namen des virtuellen Azure RemoteApp-Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="3eb28-117">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="3eb28-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3eb28-118">-Confirm</span></span>
<span data-ttu-id="3eb28-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3eb28-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb28-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb28-120">-WhatIf</span></span>
<span data-ttu-id="3eb28-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eb28-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eb28-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3eb28-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb28-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb28-123">CommonParameters</span></span>
<span data-ttu-id="3eb28-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb28-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb28-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb28-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb28-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3eb28-126">INPUTS</span></span>

## <span data-ttu-id="3eb28-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3eb28-127">OUTPUTS</span></span>

### <span data-ttu-id="3eb28-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3eb28-128">System.String</span></span>

## <span data-ttu-id="3eb28-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="3eb28-129">NOTES</span></span>

## <span data-ttu-id="3eb28-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3eb28-130">RELATED LINKS</span></span>

[<span data-ttu-id="3eb28-131">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="3eb28-131">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="3eb28-132">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="3eb28-132">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


