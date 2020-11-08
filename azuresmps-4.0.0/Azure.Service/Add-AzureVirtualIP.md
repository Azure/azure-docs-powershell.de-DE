---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FBED8515-4216-4AB6-B34E-D14A6063A3A7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2f145ec51bc6744d877661554e3d8e475d722fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005919"
---
# <span data-ttu-id="1a428-101">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="1a428-101">Add-AzureVirtualIP</span></span>

## <span data-ttu-id="1a428-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a428-102">SYNOPSIS</span></span>
<span data-ttu-id="1a428-103">Fügt einen virtuellen IP-Dienst zu einem clouddienst hinzu.</span><span class="sxs-lookup"><span data-stu-id="1a428-103">Adds a virtual IP to a cloud service.</span></span>

## <span data-ttu-id="1a428-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a428-104">SYNTAX</span></span>

```
Add-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1a428-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a428-105">DESCRIPTION</span></span>
<span data-ttu-id="1a428-106">Mit dem Cmdlet **Add-AzureVirtualIP** wird dem Azure-Dienst eine neue virtuelle IP (VIP) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1a428-106">The **Add-AzureVirtualIP** cmdlet adds a new virtual IP (VIP) to your Azure service.</span></span>
<span data-ttu-id="1a428-107">Die neue virtuelle IP-Adresse hat einen Namen, aber keine IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="1a428-107">The new virtual IP has a name but is not allocated an IP address.</span></span>

<span data-ttu-id="1a428-108">Die IP-Adresse wird nur zugewiesen, wenn Sie einen Endpunkt dem VIP zuordnen.</span><span class="sxs-lookup"><span data-stu-id="1a428-108">The IP address is allocated only when you associate an endpoint to the VIP.</span></span>
<span data-ttu-id="1a428-109">Weitere Informationen finden Sie unter Add-AzureEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1a428-109">See Add-AzureEndpoint for more details.</span></span>

<span data-ttu-id="1a428-110">Ihr Abonnement wird für zusätzliche VIPs nur dann berechnet, wenn Sie einem Endpunkt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1a428-110">Your subscription is charged for extra VIPs only once they are associated with an endpoint.</span></span>

## <span data-ttu-id="1a428-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a428-111">EXAMPLES</span></span>

### <span data-ttu-id="1a428-112">Beispiel 1: Hinzufügen einer virtuellen IP zu einem Dienst</span><span class="sxs-lookup"><span data-stu-id="1a428-112">Example 1: Add a virtual IP to a service</span></span>
```
PS C:\> Add-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
OperationDescription OperationId                          OperationStatus
-------------------- -----------                          ---------------
Add-AzureVirtualIP   4bd7b638-d2e7-216f-ba38-5221233d70ce Succeeded
```

<span data-ttu-id="1a428-113">Mit diesem Befehl wird einem Dienst eine virtuelle IP-Adresse hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1a428-113">This command adds a virtual IP address to a service.</span></span>

## <span data-ttu-id="1a428-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a428-114">PARAMETERS</span></span>

### <span data-ttu-id="1a428-115">-Information</span><span class="sxs-lookup"><span data-stu-id="1a428-115">-InformationAction</span></span>
<span data-ttu-id="1a428-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="1a428-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1a428-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1a428-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1a428-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="1a428-118">Continue</span></span>
- <span data-ttu-id="1a428-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="1a428-119">Ignore</span></span>
- <span data-ttu-id="1a428-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="1a428-120">Inquire</span></span>
- <span data-ttu-id="1a428-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1a428-121">SilentlyContinue</span></span>
- <span data-ttu-id="1a428-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="1a428-122">Stop</span></span>
- <span data-ttu-id="1a428-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="1a428-123">Suspend</span></span>

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

### <span data-ttu-id="1a428-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1a428-124">-InformationVariable</span></span>
<span data-ttu-id="1a428-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="1a428-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1a428-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="1a428-126">-Profile</span></span>
<span data-ttu-id="1a428-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1a428-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a428-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1a428-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a428-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1a428-129">-ServiceName</span></span>
<span data-ttu-id="1a428-130">Gibt den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="1a428-130">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="1a428-131">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="1a428-131">-VirtualIPName</span></span>
<span data-ttu-id="1a428-132">Gibt den Namen der virtuellen IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="1a428-132">Specifies the name of the virtual IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a428-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a428-133">CommonParameters</span></span>
<span data-ttu-id="1a428-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a428-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a428-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a428-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a428-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a428-136">INPUTS</span></span>

## <span data-ttu-id="1a428-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a428-137">OUTPUTS</span></span>

### <span data-ttu-id="1a428-138">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="1a428-138">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="1a428-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a428-139">NOTES</span></span>

## <span data-ttu-id="1a428-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a428-140">RELATED LINKS</span></span>

[<span data-ttu-id="1a428-141">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a428-141">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="1a428-142">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="1a428-142">Remove-AzureVirtualIP</span></span>](./Remove-AzureVirtualIP.md)


