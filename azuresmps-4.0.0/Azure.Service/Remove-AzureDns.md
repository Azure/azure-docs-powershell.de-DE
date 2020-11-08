---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1B1C1459-A602-423D-8CAA-B4901CFC2C82
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f684908e8119da007f8b1f844ebbac40713d51
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006685"
---
# <span data-ttu-id="8daac-101">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="8daac-101">Remove-AzureDns</span></span>

## <span data-ttu-id="8daac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8daac-102">SYNOPSIS</span></span>
<span data-ttu-id="8daac-103">Entfernt einen DNS-Server aus einem Azure-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8daac-103">Removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="8daac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8daac-104">SYNTAX</span></span>

```
Remove-AzureDns [-Name] <String> [-ServiceName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8daac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8daac-105">DESCRIPTION</span></span>
<span data-ttu-id="8daac-106">Das Cmdlet **Remove-AzureDns** entfernt einen DNS-Server aus einem Azure-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8daac-106">The **Remove-AzureDns** cmdlet removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="8daac-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8daac-107">EXAMPLES</span></span>

### <span data-ttu-id="8daac-108">Beispiel 1: Entfernen eines DNS-Servers aus einem Dienst</span><span class="sxs-lookup"><span data-stu-id="8daac-108">Example 1: Remove a DNS server from a service</span></span>
```
PS C:\> Remove-AzureDns -ServiceName "ContosoService" -Name "Dns07"
```

<span data-ttu-id="8daac-109">Mit diesem Befehl wird der DNS-Server namens Dns07 aus ContosoService entfernt.</span><span class="sxs-lookup"><span data-stu-id="8daac-109">This command removes the DNS server named Dns07 from ContosoService.</span></span>

## <span data-ttu-id="8daac-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8daac-110">PARAMETERS</span></span>

### <span data-ttu-id="8daac-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8daac-111">-Force</span></span>
<span data-ttu-id="8daac-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8daac-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8daac-113">-Information</span><span class="sxs-lookup"><span data-stu-id="8daac-113">-InformationAction</span></span>
<span data-ttu-id="8daac-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="8daac-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8daac-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8daac-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8daac-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="8daac-116">Continue</span></span>
- <span data-ttu-id="8daac-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="8daac-117">Ignore</span></span>
- <span data-ttu-id="8daac-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="8daac-118">Inquire</span></span>
- <span data-ttu-id="8daac-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8daac-119">SilentlyContinue</span></span>
- <span data-ttu-id="8daac-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="8daac-120">Stop</span></span>
- <span data-ttu-id="8daac-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="8daac-121">Suspend</span></span>

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

### <span data-ttu-id="8daac-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8daac-122">-InformationVariable</span></span>
<span data-ttu-id="8daac-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="8daac-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8daac-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8daac-124">-Name</span></span>
<span data-ttu-id="8daac-125">Gibt den Namen des DNS-Servers an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="8daac-125">Specifies the name of the DNS server that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8daac-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="8daac-126">-Profile</span></span>
<span data-ttu-id="8daac-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8daac-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8daac-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8daac-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8daac-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8daac-129">-ServiceName</span></span>
<span data-ttu-id="8daac-130">Gibt den Namen des Diensts an, von dem dieses Cmdlet einen DNS-Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="8daac-130">Specifies the name of the service from which this cmdlet removes a DNS server.</span></span>

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

### <span data-ttu-id="8daac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8daac-131">CommonParameters</span></span>
<span data-ttu-id="8daac-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8daac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8daac-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8daac-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8daac-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8daac-134">INPUTS</span></span>

## <span data-ttu-id="8daac-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8daac-135">OUTPUTS</span></span>

### <span data-ttu-id="8daac-136">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="8daac-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="8daac-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="8daac-137">NOTES</span></span>

## <span data-ttu-id="8daac-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8daac-138">RELATED LINKS</span></span>

[<span data-ttu-id="8daac-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="8daac-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="8daac-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="8daac-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="8daac-141">Neu – AzureDns</span><span class="sxs-lookup"><span data-stu-id="8daac-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="8daac-142">Satz-AzureDns</span><span class="sxs-lookup"><span data-stu-id="8daac-142">Set-AzureDns</span></span>](./Set-AzureDns.md)


