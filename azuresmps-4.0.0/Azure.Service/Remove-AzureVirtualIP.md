---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B107D789-8F66-4D7D-B126-08ACB0364826
online version: ''
schema: 2.0.0
ms.openlocfilehash: e59df078539e9ea94073defd4c8ea13a69cc2e5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005693"
---
# <span data-ttu-id="f7306-101">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="f7306-101">Remove-AzureVirtualIP</span></span>

## <span data-ttu-id="f7306-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7306-102">SYNOPSIS</span></span>
<span data-ttu-id="f7306-103">Löscht eine virtuelle IP-Adresse aus Ihrem clouddienst.</span><span class="sxs-lookup"><span data-stu-id="f7306-103">Deletes a virtual IP address from your Cloud Service.</span></span>

## <span data-ttu-id="f7306-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7306-104">SYNTAX</span></span>

```
Remove-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f7306-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7306-105">DESCRIPTION</span></span>
<span data-ttu-id="f7306-106">Das Cmdlet **Remove-AzureVirtualIP** löscht eine virtuelle IP (VIP) aus einem Azure-Dienst.</span><span class="sxs-lookup"><span data-stu-id="f7306-106">The **Remove-AzureVirtualIP** cmdlet deletes a virtual IP (VIP) from an Azure service.</span></span>
<span data-ttu-id="f7306-107">Der Vorgang ist nur erfolgreich, wenn der virtuellen IP keine Endpunkte zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f7306-107">The operation succeeds only if the virtual IP has no endpoints associated with it.</span></span>

## <span data-ttu-id="f7306-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7306-108">EXAMPLES</span></span>

### <span data-ttu-id="f7306-109">Beispiel 1: Entfernen einer virtuellen IP-Adresse aus einem Dienst</span><span class="sxs-lookup"><span data-stu-id="f7306-109">Example 1: Remove a virtual IP address from a service</span></span>
```
PS C:\> Remove-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
```

<span data-ttu-id="f7306-110">Dieser Befehl entfernt eine virtuelle IP-Adresse aus einem Dienst.</span><span class="sxs-lookup"><span data-stu-id="f7306-110">This command removes a virtual IP address from a service.</span></span>

## <span data-ttu-id="f7306-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7306-111">PARAMETERS</span></span>

### <span data-ttu-id="f7306-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f7306-112">-Force</span></span>
<span data-ttu-id="f7306-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f7306-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7306-114">-Information</span><span class="sxs-lookup"><span data-stu-id="f7306-114">-InformationAction</span></span>
<span data-ttu-id="f7306-115">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="f7306-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f7306-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f7306-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7306-117">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="f7306-117">Continue</span></span>
- <span data-ttu-id="f7306-118">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="f7306-118">Ignore</span></span>
- <span data-ttu-id="f7306-119">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="f7306-119">Inquire</span></span>
- <span data-ttu-id="f7306-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f7306-120">SilentlyContinue</span></span>
- <span data-ttu-id="f7306-121">Beenden</span><span class="sxs-lookup"><span data-stu-id="f7306-121">Stop</span></span>
- <span data-ttu-id="f7306-122">Anhalten</span><span class="sxs-lookup"><span data-stu-id="f7306-122">Suspend</span></span>

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

### <span data-ttu-id="f7306-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f7306-123">-InformationVariable</span></span>
<span data-ttu-id="f7306-124">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="f7306-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f7306-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="f7306-125">-Profile</span></span>
<span data-ttu-id="f7306-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f7306-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f7306-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f7306-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f7306-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f7306-128">-ServiceName</span></span>
<span data-ttu-id="f7306-129">Gibt den Namen des Diensts an, aus dem eine virtuelle IP-Adresse entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7306-129">Specifies the name of the service from which to remove a virtual IP address.</span></span>

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

### <span data-ttu-id="f7306-130">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="f7306-130">-VirtualIPName</span></span>
<span data-ttu-id="f7306-131">Gibt den Namen der zu entfernenden virtuellen IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="f7306-131">Specifies the name of the virtual IP address to remove.</span></span>

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

### <span data-ttu-id="f7306-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7306-132">CommonParameters</span></span>
<span data-ttu-id="f7306-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7306-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7306-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7306-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7306-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7306-135">INPUTS</span></span>

## <span data-ttu-id="f7306-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7306-136">OUTPUTS</span></span>

### <span data-ttu-id="f7306-137">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="f7306-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="f7306-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7306-138">NOTES</span></span>

## <span data-ttu-id="f7306-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7306-139">RELATED LINKS</span></span>

[<span data-ttu-id="f7306-140">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="f7306-140">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)


