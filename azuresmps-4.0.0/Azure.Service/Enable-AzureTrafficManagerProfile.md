---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006581"
---
# <span data-ttu-id="9778a-101">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9778a-101">Enable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="9778a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9778a-102">SYNOPSIS</span></span>
<span data-ttu-id="9778a-103">Aktiviert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="9778a-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="9778a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9778a-104">SYNTAX</span></span>

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9778a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9778a-105">DESCRIPTION</span></span>
<span data-ttu-id="9778a-106">Das Cmdlet **enable-AzureTrafficManagerProfile** aktiviert ein Microsoft Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="9778a-106">The **Enable-AzureTrafficManagerProfile** cmdlet enables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="9778a-107">Geben Sie den *passthru* -Parameter an, um anzuzeigen, ob der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="9778a-107">Specify the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="9778a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9778a-108">EXAMPLES</span></span>

### <span data-ttu-id="9778a-109">Beispiel 1: Aktivieren eines Traffic Manager-Profils</span><span class="sxs-lookup"><span data-stu-id="9778a-109">Example 1: Enable a Traffic Manager profile</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="9778a-110">Mit diesem Befehl wird das Traffic Manager-Profil mit dem Namen myprofil aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9778a-110">This command enables the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="9778a-111">Beispiel 2: Aktivieren eines Traffic Manager-Profils und Anzeigen der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="9778a-111">Example 2: Enable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="9778a-112">Dieser Befehl aktiviert das Traffic Manager-Profil mit dem Namen myProfile und zeigt an, ob der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="9778a-112">This command enables the Traffic Manager profile named MyProfile and displays whether the command succeeded.</span></span>

## <span data-ttu-id="9778a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9778a-113">PARAMETERS</span></span>

### <span data-ttu-id="9778a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="9778a-114">-Name</span></span>
<span data-ttu-id="9778a-115">Gibt den Namen des zu aktivierenden Traffic Manager-Profils an.</span><span class="sxs-lookup"><span data-stu-id="9778a-115">Specifies the name of the Traffic Manager profile to enable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9778a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9778a-116">-PassThru</span></span>
<span data-ttu-id="9778a-117">Gibt $true zurück, wenn der Vorgang erfolgreich war; andernfalls $false.</span><span class="sxs-lookup"><span data-stu-id="9778a-117">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="9778a-118">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="9778a-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9778a-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="9778a-119">-Profile</span></span>
<span data-ttu-id="9778a-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9778a-120">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9778a-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9778a-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9778a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9778a-122">CommonParameters</span></span>
<span data-ttu-id="9778a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9778a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9778a-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9778a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9778a-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9778a-125">INPUTS</span></span>

## <span data-ttu-id="9778a-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9778a-126">OUTPUTS</span></span>

### <span data-ttu-id="9778a-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9778a-127">System.Boolean</span></span>
<span data-ttu-id="9778a-128">Dieses Cmdlet generiert $true oder $false.</span><span class="sxs-lookup"><span data-stu-id="9778a-128">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="9778a-129">Wenn der Vorgang erfolgreich ist und Sie den *passthru* -Parameter angeben, gibt dieses Cmdlet den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="9778a-129">If the operation succeeds and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="9778a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="9778a-130">NOTES</span></span>

## <span data-ttu-id="9778a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9778a-131">RELATED LINKS</span></span>

[<span data-ttu-id="9778a-132">Deaktivieren-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9778a-132">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="9778a-133">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9778a-133">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="9778a-134">Neu – AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9778a-134">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="9778a-135">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9778a-135">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="9778a-136">Satz-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9778a-136">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


