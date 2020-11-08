---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 047C5FBD-CB0D-47BF-AE03-4DF32B4FAD87
online version: ''
schema: 2.0.0
ms.openlocfilehash: a546c9fdb066aaf1203055fd62d8eb01258569c8
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007562"
---
# <span data-ttu-id="3b973-101">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3b973-101">Get-WAPackVM</span></span>

## <span data-ttu-id="3b973-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b973-102">SYNOPSIS</span></span>
<span data-ttu-id="3b973-103">Ruft Objekte für virtuelle Maschinen ab.</span><span class="sxs-lookup"><span data-stu-id="3b973-103">Gets virtual machine objects.</span></span>

## <span data-ttu-id="3b973-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b973-104">SYNTAX</span></span>

### <span data-ttu-id="3b973-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b973-105">Empty (Default)</span></span>
```
Get-WAPackVM [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3b973-106">FromName</span><span class="sxs-lookup"><span data-stu-id="3b973-106">FromName</span></span>
```
Get-WAPackVM [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3b973-107">FromId</span><span class="sxs-lookup"><span data-stu-id="3b973-107">FromId</span></span>
```
Get-WAPackVM [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3b973-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b973-108">DESCRIPTION</span></span>
<span data-ttu-id="3b973-109">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="3b973-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="3b973-110">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3b973-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3b973-111">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3b973-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3b973-112">Das Cmdlet " **Get-WAPackVM** " Ruft Objekte des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="3b973-112">The **Get-WAPackVM** cmdlet gets virtual machine objects.</span></span>

## <span data-ttu-id="3b973-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b973-113">EXAMPLES</span></span>

### <span data-ttu-id="3b973-114">Beispiel 1: Abrufen eines virtuellen Computers mithilfe eines Namens</span><span class="sxs-lookup"><span data-stu-id="3b973-114">Example 1: Get a virtual machine by using a name</span></span>
```
PS C:\> Get-WAPackVM -Name "ContosoV126"
```

<span data-ttu-id="3b973-115">Dieser Befehl ruft den virtuellen Computer mit dem Namen ContosoV126 ab.</span><span class="sxs-lookup"><span data-stu-id="3b973-115">This command gets the virtual machine named ContosoV126.</span></span>

### <span data-ttu-id="3b973-116">Beispiel 2: Abrufen eines virtuellen Computers mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="3b973-116">Example 2: Get a virtual machine by using an ID</span></span>
```
PS C:\> Get-WAPackVM -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="3b973-117">Dieser Befehl ruft den virtuellen Computer ab, der die angegebene ID hat.</span><span class="sxs-lookup"><span data-stu-id="3b973-117">This command gets the virtual machine that has the specified ID.</span></span>

### <span data-ttu-id="3b973-118">Beispiel 3: Abrufen aller virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="3b973-118">Example 3: Get all virtual machines</span></span>
```
PS C:\> Get-WAPackVM
```

<span data-ttu-id="3b973-119">Dieser Befehl ruft alle virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="3b973-119">This command gets all virtual machines.</span></span>

## <span data-ttu-id="3b973-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b973-120">PARAMETERS</span></span>

### <span data-ttu-id="3b973-121">-ID</span><span class="sxs-lookup"><span data-stu-id="3b973-121">-ID</span></span>
<span data-ttu-id="3b973-122">Gibt die eindeutige ID einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="3b973-122">Specifies the unique ID of a virtual machine.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b973-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3b973-123">-Name</span></span>
<span data-ttu-id="3b973-124">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="3b973-124">Specifies the name of a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b973-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="3b973-125">-Profile</span></span>
<span data-ttu-id="3b973-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3b973-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b973-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3b973-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3b973-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b973-128">CommonParameters</span></span>
<span data-ttu-id="3b973-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b973-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b973-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b973-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b973-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b973-131">INPUTS</span></span>

## <span data-ttu-id="3b973-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b973-132">OUTPUTS</span></span>

## <span data-ttu-id="3b973-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b973-133">NOTES</span></span>

## <span data-ttu-id="3b973-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b973-134">RELATED LINKS</span></span>

[<span data-ttu-id="3b973-135">Neu – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3b973-135">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="3b973-136">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3b973-136">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="3b973-137">Neustart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3b973-137">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="3b973-138">Lebenslauf-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3b973-138">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="3b973-139">Satz-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3b973-139">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="3b973-140">Anfang-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3b973-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="3b973-141">Stopp-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3b973-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="3b973-142">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3b973-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="3b973-143">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="3b973-143">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


