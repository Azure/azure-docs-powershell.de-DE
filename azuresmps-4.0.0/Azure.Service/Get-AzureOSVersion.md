---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005843"
---
# <span data-ttu-id="88dae-101">Get-AzureOSVersion</span><span class="sxs-lookup"><span data-stu-id="88dae-101">Get-AzureOSVersion</span></span>

## <span data-ttu-id="88dae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88dae-102">SYNOPSIS</span></span>
<span data-ttu-id="88dae-103">Listet alle Azure Guest-Betriebssysteme auf.</span><span class="sxs-lookup"><span data-stu-id="88dae-103">Lists all Azure guest operating systems.</span></span>

## <span data-ttu-id="88dae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88dae-104">SYNTAX</span></span>

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="88dae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88dae-105">DESCRIPTION</span></span>
<span data-ttu-id="88dae-106">Das Cmdlet " **Get-AzureOSVersion** " listet alle verfügbaren Azure Guest-Betriebssysteme auf.</span><span class="sxs-lookup"><span data-stu-id="88dae-106">The **Get-AzureOSVersion** cmdlet lists all the available Azure guest operating systems.</span></span>

## <span data-ttu-id="88dae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88dae-107">EXAMPLES</span></span>

### <span data-ttu-id="88dae-108">Beispiel 1: Abrufen aller verfügbaren Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="88dae-108">Example 1: Get all available operating systems</span></span>
```
PS C:\> Get-AzureOSVersion
```

<span data-ttu-id="88dae-109">Dieser Befehl ruft ein Objekt ab, das eine Liste aller Versionen von Gastbetriebssystemen enthält, die im aktuellen Abonnement zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="88dae-109">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>

### <span data-ttu-id="88dae-110">Beispiel 2: Anzeigen von Betriebssysteminformationen in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="88dae-110">Example 2: Display operating system information in a table</span></span>
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

<span data-ttu-id="88dae-111">Dieser Befehl ruft ein Objekt ab, das eine Liste aller Versionen von Gastbetriebssystemen enthält, die im aktuellen Abonnement zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="88dae-111">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>
<span data-ttu-id="88dae-112">Der Befehl übergibt Sie mithilfe des Pipelineoperators an das Cmdlet **Format-Table** .</span><span class="sxs-lookup"><span data-stu-id="88dae-112">The command passes them to the **Format-Table** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="88dae-113">Dieses Cmdlet formatiert sie als Tabelle, in der die Betriebssystemfamilie, das Betriebssystemfamilien Etikett und die Version angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="88dae-113">That cmdlet formats them as a table that shows the operating system family, operating system family label, and version.</span></span>

## <span data-ttu-id="88dae-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="88dae-114">PARAMETERS</span></span>

### <span data-ttu-id="88dae-115">-Information</span><span class="sxs-lookup"><span data-stu-id="88dae-115">-InformationAction</span></span>
<span data-ttu-id="88dae-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="88dae-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="88dae-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="88dae-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88dae-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="88dae-118">Continue</span></span>
- <span data-ttu-id="88dae-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="88dae-119">Ignore</span></span>
- <span data-ttu-id="88dae-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="88dae-120">Inquire</span></span>
- <span data-ttu-id="88dae-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="88dae-121">SilentlyContinue</span></span>
- <span data-ttu-id="88dae-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="88dae-122">Stop</span></span>
- <span data-ttu-id="88dae-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="88dae-123">Suspend</span></span>

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

### <span data-ttu-id="88dae-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="88dae-124">-InformationVariable</span></span>
<span data-ttu-id="88dae-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="88dae-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="88dae-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="88dae-126">-Profile</span></span>
<span data-ttu-id="88dae-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="88dae-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="88dae-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="88dae-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="88dae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88dae-129">CommonParameters</span></span>
<span data-ttu-id="88dae-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88dae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88dae-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88dae-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88dae-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88dae-132">INPUTS</span></span>

## <span data-ttu-id="88dae-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88dae-133">OUTPUTS</span></span>

## <span data-ttu-id="88dae-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="88dae-134">NOTES</span></span>

## <span data-ttu-id="88dae-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88dae-135">RELATED LINKS</span></span>

[<span data-ttu-id="88dae-136">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="88dae-136">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)


