---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: B96A64DD-9005-4B04-A720-6FCF33797E8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1fa73aa4e38c8d222da6e73508e9a18a15c1e3f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006297"
---
# <span data-ttu-id="466e6-101">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="466e6-101">Remove-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="466e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="466e6-102">SYNOPSIS</span></span>
<span data-ttu-id="466e6-103">Entfernt ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="466e6-103">Removes a Traffic Manager profile.</span></span>

## <span data-ttu-id="466e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="466e6-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerProfile -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="466e6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="466e6-105">DESCRIPTION</span></span>
<span data-ttu-id="466e6-106">Das Cmdlet **Remove-AzureTrafficManagerProfile** entfernt ein Microsoft Azure Traffic Manager-Profil aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="466e6-106">The **Remove-AzureTrafficManagerProfile** cmdlet removes a Microsoft Azure Traffic Manager profile from the current subscription.</span></span>

## <span data-ttu-id="466e6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="466e6-107">EXAMPLES</span></span>

### <span data-ttu-id="466e6-108">Beispiel 1: Entfernen eines Traffic Manager-Profils</span><span class="sxs-lookup"><span data-stu-id="466e6-108">Example 1: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="466e6-109">Mit diesem Befehl wird das Traffic Manager-Profil mit dem Namen myprofil entfernt.</span><span class="sxs-lookup"><span data-stu-id="466e6-109">This command removes the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="466e6-110">Beispiel 2: Entfernen eines Traffic Manager-Profils</span><span class="sxs-lookup"><span data-stu-id="466e6-110">Example 2: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile" -Force -PassThru
```

<span data-ttu-id="466e6-111">Mit diesem Befehl wird das Traffic Manager-Profil mit dem Namen myprofil entfernt, ohne dass Sie zur Bestätigung aufgefordert werden, und die Ergebnisse werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="466e6-111">This command removes the Traffic Manager profile named MyProfile without prompting you for confirmation, and returns the results.</span></span>

## <span data-ttu-id="466e6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="466e6-112">PARAMETERS</span></span>

### <span data-ttu-id="466e6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="466e6-113">-Force</span></span>
<span data-ttu-id="466e6-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="466e6-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="466e6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="466e6-115">-Name</span></span>
<span data-ttu-id="466e6-116">Gibt den Namen des zu löschenden Traffic Manager-Profils an.</span><span class="sxs-lookup"><span data-stu-id="466e6-116">Specifies the name of the Traffic Manager profile to delete.</span></span>

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

### <span data-ttu-id="466e6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="466e6-117">-PassThru</span></span>
<span data-ttu-id="466e6-118">Gibt $true zurück, wenn der Vorgang erfolgreich war; andernfalls $false.</span><span class="sxs-lookup"><span data-stu-id="466e6-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="466e6-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="466e6-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="466e6-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="466e6-120">-Profile</span></span>
<span data-ttu-id="466e6-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="466e6-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="466e6-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="466e6-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="466e6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="466e6-123">CommonParameters</span></span>
<span data-ttu-id="466e6-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="466e6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="466e6-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="466e6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="466e6-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="466e6-126">INPUTS</span></span>

## <span data-ttu-id="466e6-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="466e6-127">OUTPUTS</span></span>

### <span data-ttu-id="466e6-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="466e6-128">System.Boolean</span></span>
<span data-ttu-id="466e6-129">Dieses Cmdlet generiert $true oder $false.</span><span class="sxs-lookup"><span data-stu-id="466e6-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="466e6-130">Wenn der Vorgang erfolgreich ist und Sie den *passthru* -Parameter angeben, gibt dieses Cmdlet den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="466e6-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="466e6-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="466e6-131">NOTES</span></span>

## <span data-ttu-id="466e6-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="466e6-132">RELATED LINKS</span></span>

[<span data-ttu-id="466e6-133">Deaktivieren-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="466e6-133">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="466e6-134">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="466e6-134">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="466e6-135">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="466e6-135">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="466e6-136">Neu – AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="466e6-136">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="466e6-137">Satz-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="466e6-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


