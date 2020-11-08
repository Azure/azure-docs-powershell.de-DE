---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AF4DF7EC-95BA-44E2-AB9B-5C8FE45CCE4C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83c0858d813c157301098f680fa9d2a90ef6950a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005940"
---
# <span data-ttu-id="e25a7-101">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e25a7-101">Add-AzureDns</span></span>

## <span data-ttu-id="e25a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e25a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e25a7-103">Fügt einen DNS-Server zu einem Azure-Dienst hinzu.</span><span class="sxs-lookup"><span data-stu-id="e25a7-103">Adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="e25a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e25a7-104">SYNTAX</span></span>

```
Add-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e25a7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e25a7-105">DESCRIPTION</span></span>
<span data-ttu-id="e25a7-106">Mit dem Cmdlet **Add-AzureDns** wird ein DNS-Server zu einem Azure-Dienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e25a7-106">The **Add-AzureDns** cmdlet adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="e25a7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e25a7-107">EXAMPLES</span></span>

### <span data-ttu-id="e25a7-108">Beispiel 1: Hinzufügen eines DNS-Servers</span><span class="sxs-lookup"><span data-stu-id="e25a7-108">Example 1: Add a DNS server</span></span>
```
PS C:\> Add-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.4 -Name "Dns07"
```

<span data-ttu-id="e25a7-109">Mit diesem Befehl wird der DNS-Server mit der Adresse 10.1.2.4 zu ContosoService hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e25a7-109">This command adds the DNS server that has the address 10.1.2.4 to ContosoService.</span></span>

## <span data-ttu-id="e25a7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e25a7-110">PARAMETERS</span></span>

### <span data-ttu-id="e25a7-111">-Information</span><span class="sxs-lookup"><span data-stu-id="e25a7-111">-InformationAction</span></span>
<span data-ttu-id="e25a7-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="e25a7-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e25a7-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e25a7-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e25a7-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="e25a7-114">Continue</span></span>
- <span data-ttu-id="e25a7-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="e25a7-115">Ignore</span></span>
- <span data-ttu-id="e25a7-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="e25a7-116">Inquire</span></span>
- <span data-ttu-id="e25a7-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e25a7-117">SilentlyContinue</span></span>
- <span data-ttu-id="e25a7-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="e25a7-118">Stop</span></span>
- <span data-ttu-id="e25a7-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="e25a7-119">Suspend</span></span>

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

### <span data-ttu-id="e25a7-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e25a7-120">-InformationVariable</span></span>
<span data-ttu-id="e25a7-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="e25a7-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e25a7-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="e25a7-122">-IPAddress</span></span>
<span data-ttu-id="e25a7-123">Gibt die IP-Adresse des DNS-Servers an.</span><span class="sxs-lookup"><span data-stu-id="e25a7-123">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="e25a7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e25a7-124">-Name</span></span>
<span data-ttu-id="e25a7-125">Gibt einen Anzeigenamen für den DNS-Server an.</span><span class="sxs-lookup"><span data-stu-id="e25a7-125">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="e25a7-126">Dieser Name ist nicht unbedingt ein vollständig qualifizierter Domänenname.</span><span class="sxs-lookup"><span data-stu-id="e25a7-126">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="e25a7-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="e25a7-127">-Profile</span></span>
<span data-ttu-id="e25a7-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e25a7-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e25a7-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e25a7-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e25a7-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e25a7-130">-ServiceName</span></span>
<span data-ttu-id="e25a7-131">Gibt den Namen des Diensts an, dem dieses Cmdlet den DNS-Server hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="e25a7-131">Specifies the name of the service to which this cmdlet adds the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25a7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25a7-132">CommonParameters</span></span>
<span data-ttu-id="e25a7-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e25a7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25a7-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e25a7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25a7-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e25a7-135">INPUTS</span></span>

## <span data-ttu-id="e25a7-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e25a7-136">OUTPUTS</span></span>

### <span data-ttu-id="e25a7-137">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="e25a7-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="e25a7-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="e25a7-138">NOTES</span></span>

## <span data-ttu-id="e25a7-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e25a7-139">RELATED LINKS</span></span>

[<span data-ttu-id="e25a7-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e25a7-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="e25a7-141">Neu – AzureDns</span><span class="sxs-lookup"><span data-stu-id="e25a7-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="e25a7-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e25a7-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="e25a7-143">Satz-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e25a7-143">Set-AzureDns</span></span>](./Set-AzureDns.md)


