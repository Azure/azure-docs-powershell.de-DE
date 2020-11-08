---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007612"
---
# <span data-ttu-id="89383-101">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="89383-101">Remove-WAPackVNet</span></span>

## <span data-ttu-id="89383-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89383-102">SYNOPSIS</span></span>
<span data-ttu-id="89383-103">Entfernt virtuelle Netzwerkobjekte.</span><span class="sxs-lookup"><span data-stu-id="89383-103">Removes virtual network objects.</span></span>

## <span data-ttu-id="89383-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89383-104">SYNTAX</span></span>

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="89383-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89383-105">DESCRIPTION</span></span>
<span data-ttu-id="89383-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="89383-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="89383-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="89383-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="89383-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="89383-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="89383-109">Das Cmdlet **Remove-WAPackVNet** entfernt virtuelle Netzwerkobjekte.</span><span class="sxs-lookup"><span data-stu-id="89383-109">The **Remove-WAPackVNet** cmdlet removes virtual network objects.</span></span>

## <span data-ttu-id="89383-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89383-110">EXAMPLES</span></span>

### <span data-ttu-id="89383-111">Beispiel 1: Entfernen eines virtualisierten Netzwerks</span><span class="sxs-lookup"><span data-stu-id="89383-111">Example 1: Remove a virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

<span data-ttu-id="89383-112">Der erste Befehl ruft das virtualisierte Netzwerk mit dem Namen ContosoVNet01 mit dem Cmdlet **Get-WAPackVNet** ab und speichert dieses Objekt dann in der $VNet Variablen.</span><span class="sxs-lookup"><span data-stu-id="89383-112">The first command gets the virtualized network named ContosoVNet01 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="89383-113">Der zweite Befehl entfernt das virtualisierte Netzwerk, das in $VNet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="89383-113">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="89383-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="89383-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="89383-115">Beispiel 2: Entfernen eines virtualisierten Netzwerks ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="89383-115">Example 2: Remove a virtualized network without confirmation</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

<span data-ttu-id="89383-116">Der erste Befehl ruft den clouddienst mit dem Namen ContosoVNet02 mit dem Cmdlet **Get-WAPackVNet** ab und speichert dieses Objekt dann in der $VNet Variablen.</span><span class="sxs-lookup"><span data-stu-id="89383-116">The first command gets the cloud service named ContosoVNet02 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="89383-117">Der zweite Befehl entfernt das virtualisierte Netzwerk, das in $VNet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="89383-117">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="89383-118">Dieser Befehl enthält den Parameter *Force* .</span><span class="sxs-lookup"><span data-stu-id="89383-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="89383-119">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="89383-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="89383-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="89383-120">PARAMETERS</span></span>

### <span data-ttu-id="89383-121">-Force</span><span class="sxs-lookup"><span data-stu-id="89383-121">-Force</span></span>
<span data-ttu-id="89383-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="89383-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89383-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89383-123">-PassThru</span></span>
<span data-ttu-id="89383-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="89383-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="89383-125">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="89383-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="89383-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="89383-126">-Profile</span></span>
<span data-ttu-id="89383-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="89383-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89383-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="89383-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89383-129">-VNet</span><span class="sxs-lookup"><span data-stu-id="89383-129">-VNet</span></span>
<span data-ttu-id="89383-130">Gibt ein virtualisiertes Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="89383-130">Specifies a virtualized network.</span></span>
<span data-ttu-id="89383-131">Verwenden Sie das Cmdlet " **Get-WAPackVNet** ", um ein virtualisiertes Netzwerk zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="89383-131">To obtain a virtualized network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89383-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89383-132">CommonParameters</span></span>
<span data-ttu-id="89383-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89383-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89383-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89383-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89383-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89383-135">INPUTS</span></span>

## <span data-ttu-id="89383-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89383-136">OUTPUTS</span></span>

## <span data-ttu-id="89383-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="89383-137">NOTES</span></span>

## <span data-ttu-id="89383-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89383-138">RELATED LINKS</span></span>

[<span data-ttu-id="89383-139">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="89383-139">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="89383-140">Neu – WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="89383-140">New-WAPackVNet</span></span>](./New-WAPackVNet.md)


