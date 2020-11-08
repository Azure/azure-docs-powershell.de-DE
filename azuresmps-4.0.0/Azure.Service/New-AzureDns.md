---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006130"
---
# <span data-ttu-id="4e35c-101">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4e35c-101">New-AzureDns</span></span>

## <span data-ttu-id="4e35c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e35c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e35c-103">Erstellt ein Azure DNS Settings-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4e35c-103">Creates an Azure DNS settings object.</span></span>

## <span data-ttu-id="4e35c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e35c-104">SYNTAX</span></span>

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4e35c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e35c-105">DESCRIPTION</span></span>
<span data-ttu-id="4e35c-106">Mit dem Cmdlet **New-AzureDns** wird ein Azure DNS Settings-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e35c-106">The **New-AzureDns** cmdlet creates an Azure DNS settings object.</span></span>
<span data-ttu-id="4e35c-107">Sie können ein DNS-Einstellungsobjekt verwenden, wenn Sie einen virtuellen Computer mithilfe des Cmdlets **New-AzureVM** erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e35c-107">You can use a DNS settings object when you create a virtual machine by using the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="4e35c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e35c-108">EXAMPLES</span></span>

### <span data-ttu-id="4e35c-109">Beispiel 1: Erstellen eines DNS-Einstellungs Objekts</span><span class="sxs-lookup"><span data-stu-id="4e35c-109">Example 1: Create a DNS settings object</span></span>
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

<span data-ttu-id="4e35c-110">Mit diesem Befehl wird ein Azure DNS Settings-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e35c-110">This command creates an Azure DNS settings object.</span></span>
<span data-ttu-id="4e35c-111">Der DNS-Server hat die angegebene Adresse und den Anzeigenamen Dns01.</span><span class="sxs-lookup"><span data-stu-id="4e35c-111">The DNS server has the specified address and the friendly name Dns01.</span></span>
<span data-ttu-id="4e35c-112">Der Befehl speichert das Objekt in der $DNS-Variablen für die Verwendung durch das Cmdlet **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="4e35c-112">The command stores the object in the $Dns variable for use by the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="4e35c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e35c-113">PARAMETERS</span></span>

### <span data-ttu-id="4e35c-114">-Information</span><span class="sxs-lookup"><span data-stu-id="4e35c-114">-InformationAction</span></span>
<span data-ttu-id="4e35c-115">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="4e35c-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4e35c-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4e35c-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4e35c-117">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="4e35c-117">Continue</span></span>
- <span data-ttu-id="4e35c-118">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="4e35c-118">Ignore</span></span>
- <span data-ttu-id="4e35c-119">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="4e35c-119">Inquire</span></span>
- <span data-ttu-id="4e35c-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4e35c-120">SilentlyContinue</span></span>
- <span data-ttu-id="4e35c-121">Beenden</span><span class="sxs-lookup"><span data-stu-id="4e35c-121">Stop</span></span>
- <span data-ttu-id="4e35c-122">Anhalten</span><span class="sxs-lookup"><span data-stu-id="4e35c-122">Suspend</span></span>

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

### <span data-ttu-id="4e35c-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4e35c-123">-InformationVariable</span></span>
<span data-ttu-id="4e35c-124">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="4e35c-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4e35c-125">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="4e35c-125">-IPAddress</span></span>
<span data-ttu-id="4e35c-126">Gibt die IP-Adresse des DNS-Servers an.</span><span class="sxs-lookup"><span data-stu-id="4e35c-126">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="4e35c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4e35c-127">-Name</span></span>
<span data-ttu-id="4e35c-128">Gibt einen Anzeigenamen für den DNS-Server an.</span><span class="sxs-lookup"><span data-stu-id="4e35c-128">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="4e35c-129">Dieser Name ist nicht unbedingt ein vollständig qualifizierter Domänenname.</span><span class="sxs-lookup"><span data-stu-id="4e35c-129">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="4e35c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e35c-130">CommonParameters</span></span>
<span data-ttu-id="4e35c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e35c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e35c-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e35c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e35c-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e35c-133">INPUTS</span></span>

## <span data-ttu-id="4e35c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e35c-134">OUTPUTS</span></span>

## <span data-ttu-id="4e35c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e35c-135">NOTES</span></span>

## <span data-ttu-id="4e35c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e35c-136">RELATED LINKS</span></span>

[<span data-ttu-id="4e35c-137">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4e35c-137">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="4e35c-138">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4e35c-138">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="4e35c-139">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="4e35c-139">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="4e35c-140">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4e35c-140">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="4e35c-141">Satz-AzureDns</span><span class="sxs-lookup"><span data-stu-id="4e35c-141">Set-AzureDns</span></span>](./Set-AzureDns.md)


