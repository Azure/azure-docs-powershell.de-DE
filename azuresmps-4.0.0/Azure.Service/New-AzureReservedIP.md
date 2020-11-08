---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9C22F5D7-1FD0-4699-83D7-1D72C5234DEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d09173c43de9c01056055f714217db5eb4c58225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006199"
---
# <span data-ttu-id="6965f-101">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="6965f-101">New-AzureReservedIP</span></span>

## <span data-ttu-id="6965f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6965f-102">SYNOPSIS</span></span>
<span data-ttu-id="6965f-103">Erstellt eine reservierte IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6965f-103">Creates a reserved IP address.</span></span>

## <span data-ttu-id="6965f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6965f-104">SYNTAX</span></span>

### <span data-ttu-id="6965f-105">CreateNewReservedIP (Standard)</span><span class="sxs-lookup"><span data-stu-id="6965f-105">CreateNewReservedIP (Default)</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6965f-106">CreateInUseReservedIPUsingSlot</span><span class="sxs-lookup"><span data-stu-id="6965f-106">CreateInUseReservedIPUsingSlot</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6965f-107">CreateInUseReservedIP</span><span class="sxs-lookup"><span data-stu-id="6965f-107">CreateInUseReservedIP</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6965f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6965f-108">DESCRIPTION</span></span>
<span data-ttu-id="6965f-109">Das Cmdlet **New-AzureReservedIP** erstellt eine reservierte IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6965f-109">The **New-AzureReservedIP** cmdlet creates a reserved IP address.</span></span>

## <span data-ttu-id="6965f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6965f-110">EXAMPLES</span></span>

### <span data-ttu-id="6965f-111">Beispiel 1: Erstellen einer neuen reservierten IP</span><span class="sxs-lookup"><span data-stu-id="6965f-111">Example 1: Create a new reserved IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName $Name -Label $Label -Location $Location
```

<span data-ttu-id="6965f-112">Mit diesem Befehl wird eine neue reservierte IP-Adresse im Abonnement erstellt, die zum Erstellen von Cloud-Diensten verwendet werden kann, die Web-, Worker-und Virtual Machines umfassen.</span><span class="sxs-lookup"><span data-stu-id="6965f-112">This command creates a new reserved IP address in the subscription, which can be used for creating cloud services that include Web, Worker, and Virtual Machines.</span></span>

### <span data-ttu-id="6965f-113">Beispiel 2: Erstellen einer reservierten IP basierend auf einer vorhandenen IP</span><span class="sxs-lookup"><span data-stu-id="6965f-113">Example 2: Create a reserved IP based on an existing IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName resip14 -Location "West Europe" -ServiceName piptestwesteurope
```

<span data-ttu-id="6965f-114">Mit diesem Befehl wird eine vorhandene VIP-(virtuelle IP-Adresse) für den angegebenen Dienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="6965f-114">This command creates an existing VIP (Virtual IP) on the specified service.</span></span>

## <span data-ttu-id="6965f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6965f-115">PARAMETERS</span></span>

### <span data-ttu-id="6965f-116">-Information</span><span class="sxs-lookup"><span data-stu-id="6965f-116">-InformationAction</span></span>
<span data-ttu-id="6965f-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="6965f-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6965f-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6965f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6965f-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="6965f-119">Continue</span></span>
- <span data-ttu-id="6965f-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="6965f-120">Ignore</span></span>
- <span data-ttu-id="6965f-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="6965f-121">Inquire</span></span>
- <span data-ttu-id="6965f-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6965f-122">SilentlyContinue</span></span>
- <span data-ttu-id="6965f-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="6965f-123">Stop</span></span>
- <span data-ttu-id="6965f-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="6965f-124">Suspend</span></span>

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

### <span data-ttu-id="6965f-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6965f-125">-InformationVariable</span></span>
<span data-ttu-id="6965f-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="6965f-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6965f-127">-Label</span><span class="sxs-lookup"><span data-stu-id="6965f-127">-Label</span></span>
<span data-ttu-id="6965f-128">Gibt eine Bezeichnung für die reservierte IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="6965f-128">Specifies a label for the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6965f-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="6965f-129">-Location</span></span>
<span data-ttu-id="6965f-130">Gibt einen Speicherort an, an dem die reservierte IP-Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6965f-130">Specifies a location at which to create the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6965f-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="6965f-131">-Profile</span></span>
<span data-ttu-id="6965f-132">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6965f-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6965f-133">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6965f-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6965f-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="6965f-134">-ReservedIPName</span></span>
<span data-ttu-id="6965f-135">Gibt den Namen der reservierten IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="6965f-135">Specifies the reserved IP address name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6965f-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6965f-136">-ServiceName</span></span>
<span data-ttu-id="6965f-137">Gibt einen Dienstnamen an.</span><span class="sxs-lookup"><span data-stu-id="6965f-137">Specifies a service name.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6965f-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="6965f-138">-Slot</span></span>
<span data-ttu-id="6965f-139">Gibt den Bereitstellungs Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="6965f-139">Specifies the deployment slot.</span></span>
<span data-ttu-id="6965f-140">Die akzeptablen Werte für diesen Parameter sind: Staging, Production.</span><span class="sxs-lookup"><span data-stu-id="6965f-140">The acceptable values for this parameter are: Staging, Production.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6965f-141">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="6965f-141">-VirtualIPName</span></span>
<span data-ttu-id="6965f-142">Gibt an, dass dieses Cmdlet den **VirtualIPName** -Parameter verwendet, um eine vorhandene virtuelle IP-Adresse (VIP) in Ihrer Bereitstellung zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="6965f-142">Specifies that this cmdlet uses the **VirtualIPName** parameter to reserve an existing virtual IP address (VIP) in your deployment.</span></span>
<span data-ttu-id="6965f-143">Wenn dieser Parameter nicht angegeben wird, reserviert dieses Cmdlet einen neuen VIP-Code.</span><span class="sxs-lookup"><span data-stu-id="6965f-143">If this parameter is not specified, this cmdlet reserves a new VIP.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6965f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6965f-144">CommonParameters</span></span>
<span data-ttu-id="6965f-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6965f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6965f-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6965f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6965f-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6965f-147">INPUTS</span></span>

## <span data-ttu-id="6965f-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6965f-148">OUTPUTS</span></span>

## <span data-ttu-id="6965f-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="6965f-149">NOTES</span></span>

## <span data-ttu-id="6965f-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6965f-150">RELATED LINKS</span></span>

[<span data-ttu-id="6965f-151">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="6965f-151">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="6965f-152">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="6965f-152">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


