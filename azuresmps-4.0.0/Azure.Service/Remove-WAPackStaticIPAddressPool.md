---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CE618AD2-7E28-4012-BF3C-B932B95FFDD5
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07358c37bf30e8d5fc3040cdfd174b800df96e4
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007618"
---
# <span data-ttu-id="83411-101">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="83411-101">Remove-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="83411-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83411-102">SYNOPSIS</span></span>
<span data-ttu-id="83411-103">Entfernt statische IP-Adresspool Objekte.</span><span class="sxs-lookup"><span data-stu-id="83411-103">Removes static IP address pool objects.</span></span>

## <span data-ttu-id="83411-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83411-104">SYNTAX</span></span>

```
Remove-WAPackStaticIPAddressPool -StaticIPAddressPool <StaticIPAddressPool> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="83411-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83411-105">DESCRIPTION</span></span>
<span data-ttu-id="83411-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="83411-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="83411-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="83411-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="83411-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="83411-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="83411-109">Das Cmdlet **Remove-WAPackStaticIPAddressPool** entfernt statische IP-Adresspool Objekte.</span><span class="sxs-lookup"><span data-stu-id="83411-109">The **Remove-WAPackStaticIPAddressPool** cmdlet removes static IP address pool objects.</span></span>

## <span data-ttu-id="83411-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83411-110">EXAMPLES</span></span>

### <span data-ttu-id="83411-111">Beispiel 1: Entfernen eines statischen IP-Adresspools</span><span class="sxs-lookup"><span data-stu-id="83411-111">Example 1: Remove a static IP address pool</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool01"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool
```

<span data-ttu-id="83411-112">Der erste Befehl ruft den statischen IP-Adresspool mit dem Namen ContosoStaticIPAddressPool01 mit dem Cmdlet **Get-WAPackStaticIPAddressPool** ab und speichert dieses Objekt dann in der $StaticIPAddressPool Variablen.</span><span class="sxs-lookup"><span data-stu-id="83411-112">The first command gets the static IP address pool named ContosoStaticIPAddressPool01 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $StaticIPAddressPool variable.</span></span>

<span data-ttu-id="83411-113">Der zweite Befehl entfernt den statischen IP-Adresspool, der in $StaticIPAddressPool gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="83411-113">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="83411-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="83411-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="83411-115">Beispiel 2: Entfernen eines statischen IP-Adresspools ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="83411-115">Example 2: Remove a static IP address pool without confirmation</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool02"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool -Force
```

<span data-ttu-id="83411-116">Der erste Befehl ruft den statischen IP-Adresspool mit dem Namen ContosoStaticIPAddressPool02 mit dem Cmdlet **Get-WAPackStaticIPAddressPool** ab und speichert dieses Objekt dann in der Variablen $ StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="83411-116">The first command gets the static IP address pool named ContosoStaticIPAddressPool02 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $ StaticIPAddressPool variable.</span></span>

<span data-ttu-id="83411-117">Der zweite Befehl entfernt den statischen IP-Adresspool, der in $StaticIPAddressPool gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="83411-117">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="83411-118">Dieser Befehl enthält den Parameter *Force* .</span><span class="sxs-lookup"><span data-stu-id="83411-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="83411-119">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="83411-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="83411-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="83411-120">PARAMETERS</span></span>

### <span data-ttu-id="83411-121">-Force</span><span class="sxs-lookup"><span data-stu-id="83411-121">-Force</span></span>
<span data-ttu-id="83411-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="83411-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="83411-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83411-123">-PassThru</span></span>
<span data-ttu-id="83411-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="83411-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="83411-125">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="83411-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83411-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="83411-126">-Profile</span></span>
<span data-ttu-id="83411-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="83411-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="83411-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="83411-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="83411-129">-StaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="83411-129">-StaticIPAddressPool</span></span>
<span data-ttu-id="83411-130">Gibt einen StaticIPAddressPool an.</span><span class="sxs-lookup"><span data-stu-id="83411-130">Specifies a StaticIPAddressPool.</span></span>
<span data-ttu-id="83411-131">Zum Abrufen eines statischen IP-Adresspools verwenden Sie das Cmdlet **Get-WAPackStaticIPAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="83411-131">To obtain a static IP address pool, use the **Get-WAPackStaticIPAddressPool** cmdlet.</span></span>

```yaml
Type: StaticIPAddressPool
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83411-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83411-132">CommonParameters</span></span>
<span data-ttu-id="83411-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83411-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83411-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83411-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83411-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83411-135">INPUTS</span></span>

## <span data-ttu-id="83411-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83411-136">OUTPUTS</span></span>

## <span data-ttu-id="83411-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="83411-137">NOTES</span></span>

## <span data-ttu-id="83411-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83411-138">RELATED LINKS</span></span>

[<span data-ttu-id="83411-139">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="83411-139">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="83411-140">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="83411-140">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


