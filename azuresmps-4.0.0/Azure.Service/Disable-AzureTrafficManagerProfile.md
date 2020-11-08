---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005899"
---
# <span data-ttu-id="72807-101">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72807-101">Disable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="72807-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72807-102">SYNOPSIS</span></span>
<span data-ttu-id="72807-103">Deaktiviert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="72807-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="72807-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72807-104">SYNTAX</span></span>

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="72807-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72807-105">DESCRIPTION</span></span>
<span data-ttu-id="72807-106">Das Cmdlet **Disable-AzureTrafficManagerProfile** deaktiviert ein Microsoft Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="72807-106">The **Disable-AzureTrafficManagerProfile** cmdlet disables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="72807-107">Sie können den *passthru* -Parameter verwenden, um anzuzeigen, ob der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="72807-107">You can use the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="72807-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72807-108">EXAMPLES</span></span>

### <span data-ttu-id="72807-109">Beispiel 1: Deaktivieren eines Traffic Manager-Profils und Anzeigen der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="72807-109">Example 1: Disable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="72807-110">Mit diesem Befehl wird das Traffic Manager-Profil mit dem Namen myprofil deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="72807-110">This command disables the Traffic Manager profile named MyProfile.</span></span>
<span data-ttu-id="72807-111">Der Befehl gibt den *passthru* -Parameter an, um anzuzeigen, ob der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="72807-111">The command specifies the *PassThru* parameter to display whether the command succeeded.</span></span>

### <span data-ttu-id="72807-112">Beispiel 2: Deaktivieren eines Traffic Manager-Profils und Anzeigen von Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="72807-112">Example 2: Disable a Traffic Manager profile and display no results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="72807-113">Dieser Befehl deaktiviert das Traffic Manager-Profil mit dem Namen "Mein Profil", zeigt aber nicht an, ob der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="72807-113">This command disables the Traffic Manager profile named MyProfile but does not display whether the command succeeded.</span></span>

## <span data-ttu-id="72807-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="72807-114">PARAMETERS</span></span>

### <span data-ttu-id="72807-115">-Name</span><span class="sxs-lookup"><span data-stu-id="72807-115">-Name</span></span>
<span data-ttu-id="72807-116">Gibt den Namen des zu deaktivierenden Traffic Manager-Profils an.</span><span class="sxs-lookup"><span data-stu-id="72807-116">Specifies the name of the Traffic Manager profile to disable.</span></span>

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

### <span data-ttu-id="72807-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72807-117">-PassThru</span></span>
<span data-ttu-id="72807-118">Gibt $true zurück, wenn der Vorgang erfolgreich war; andernfalls $false.</span><span class="sxs-lookup"><span data-stu-id="72807-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="72807-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="72807-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="72807-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="72807-120">-Profile</span></span>
<span data-ttu-id="72807-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="72807-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="72807-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="72807-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="72807-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72807-123">CommonParameters</span></span>
<span data-ttu-id="72807-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72807-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72807-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72807-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72807-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72807-126">INPUTS</span></span>

## <span data-ttu-id="72807-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72807-127">OUTPUTS</span></span>

### <span data-ttu-id="72807-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72807-128">System.Boolean</span></span>
<span data-ttu-id="72807-129">Dieses Cmdlet generiert $true oder $false.</span><span class="sxs-lookup"><span data-stu-id="72807-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="72807-130">Wenn der Vorgang erfolgreich ist und Sie den *passthru* -Parameter angeben, gibt dieses Cmdlet den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="72807-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="72807-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="72807-131">NOTES</span></span>

## <span data-ttu-id="72807-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72807-132">RELATED LINKS</span></span>

[<span data-ttu-id="72807-133">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72807-133">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="72807-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72807-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="72807-135">Neu – AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72807-135">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="72807-136">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72807-136">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="72807-137">Satz-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="72807-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


