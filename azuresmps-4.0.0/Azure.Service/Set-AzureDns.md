---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BC16303-CCB4-40D8-ABCB-59CF0D85ED63
online version: ''
schema: 2.0.0
ms.openlocfilehash: f24f5d8f7f72c59847cfa5dde51a1937bc304735
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006275"
---
# <span data-ttu-id="56afe-101">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="56afe-101">Set-AzureDns</span></span>

## <span data-ttu-id="56afe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56afe-102">SYNOPSIS</span></span>
<span data-ttu-id="56afe-103">Ändert die IP-Adresse eines DNS-Servers.</span><span class="sxs-lookup"><span data-stu-id="56afe-103">Modifies the IP address of a DNS server.</span></span>

## <span data-ttu-id="56afe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56afe-104">SYNTAX</span></span>

```
Set-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="56afe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56afe-105">DESCRIPTION</span></span>
<span data-ttu-id="56afe-106">Das Cmdlet " **Satz-AzureDns** " ändert die IP-Adresse eines DNS-Servers für einen Azure-Dienst.</span><span class="sxs-lookup"><span data-stu-id="56afe-106">The **Set-AzureDns** cmdlet modifies the IP address of a DNS server for an Azure service.</span></span>

## <span data-ttu-id="56afe-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56afe-107">EXAMPLES</span></span>

### <span data-ttu-id="56afe-108">Beispiel 1: Ändern der IP-Adresse eines DNS-Servers</span><span class="sxs-lookup"><span data-stu-id="56afe-108">Example 1: Modify the IP address of a DNS server</span></span>
```
PS C:\> Set-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.5 -Name "Dns07"
```

<span data-ttu-id="56afe-109">Dieser Befehl ändert die IP-Adresse des DNS-Servers mit dem Namen Dns07 für den Dienst mit dem Namen ContosoService.</span><span class="sxs-lookup"><span data-stu-id="56afe-109">This command modifies the IP address of the DNS server named Dns07 for the service named ContosoService.</span></span>

## <span data-ttu-id="56afe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="56afe-110">PARAMETERS</span></span>

### <span data-ttu-id="56afe-111">-Information</span><span class="sxs-lookup"><span data-stu-id="56afe-111">-InformationAction</span></span>
<span data-ttu-id="56afe-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="56afe-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="56afe-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="56afe-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56afe-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="56afe-114">Continue</span></span>
- <span data-ttu-id="56afe-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="56afe-115">Ignore</span></span>
- <span data-ttu-id="56afe-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="56afe-116">Inquire</span></span>
- <span data-ttu-id="56afe-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="56afe-117">SilentlyContinue</span></span>
- <span data-ttu-id="56afe-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="56afe-118">Stop</span></span>
- <span data-ttu-id="56afe-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="56afe-119">Suspend</span></span>

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

### <span data-ttu-id="56afe-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="56afe-120">-InformationVariable</span></span>
<span data-ttu-id="56afe-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="56afe-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="56afe-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="56afe-122">-IPAddress</span></span>
<span data-ttu-id="56afe-123">Gibt die neue IP-Adresse des DNS-Servers an.</span><span class="sxs-lookup"><span data-stu-id="56afe-123">Specifies the new IP address of the DNS server.</span></span>

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

### <span data-ttu-id="56afe-124">-Name</span><span class="sxs-lookup"><span data-stu-id="56afe-124">-Name</span></span>
<span data-ttu-id="56afe-125">Gibt den Namen des DNS-Servers an, der von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="56afe-125">Specifies the name of the DNS server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="56afe-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="56afe-126">-Profile</span></span>
<span data-ttu-id="56afe-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="56afe-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56afe-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="56afe-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56afe-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="56afe-129">-ServiceName</span></span>
<span data-ttu-id="56afe-130">Gibt den Namen des Diensts an, für den dieses Cmdlet die Adresse des DNS-Servers ändert.</span><span class="sxs-lookup"><span data-stu-id="56afe-130">Specifies the name of the service for which this cmdlet modifies the address of the DNS server.</span></span>

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

### <span data-ttu-id="56afe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56afe-131">CommonParameters</span></span>
<span data-ttu-id="56afe-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56afe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56afe-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56afe-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56afe-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56afe-134">INPUTS</span></span>

## <span data-ttu-id="56afe-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56afe-135">OUTPUTS</span></span>

### <span data-ttu-id="56afe-136">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="56afe-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="56afe-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="56afe-137">NOTES</span></span>

## <span data-ttu-id="56afe-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56afe-138">RELATED LINKS</span></span>

[<span data-ttu-id="56afe-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="56afe-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="56afe-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="56afe-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="56afe-141">Neu – AzureDns</span><span class="sxs-lookup"><span data-stu-id="56afe-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="56afe-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="56afe-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)


