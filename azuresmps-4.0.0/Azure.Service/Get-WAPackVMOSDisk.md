---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007558"
---
# <span data-ttu-id="0c995-101">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="0c995-101">Get-WAPackVMOSDisk</span></span>

## <span data-ttu-id="0c995-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c995-102">SYNOPSIS</span></span>
<span data-ttu-id="0c995-103">Ruft Betriebssystem-Datenträgerobjekte für virtuelle Computer ab.</span><span class="sxs-lookup"><span data-stu-id="0c995-103">Gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="0c995-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c995-104">SYNTAX</span></span>

### <span data-ttu-id="0c995-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c995-105">Empty (Default)</span></span>
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0c995-106">FromId</span><span class="sxs-lookup"><span data-stu-id="0c995-106">FromId</span></span>
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0c995-107">FromName</span><span class="sxs-lookup"><span data-stu-id="0c995-107">FromName</span></span>
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0c995-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c995-108">DESCRIPTION</span></span>
<span data-ttu-id="0c995-109">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="0c995-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="0c995-110">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0c995-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0c995-111">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0c995-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0c995-112">Das Cmdlet " **Get-WAPackVMOSDisk** " ruft Betriebssystem-Datenträgerobjekte für virtuelle Computer ab.</span><span class="sxs-lookup"><span data-stu-id="0c995-112">The **Get-WAPackVMOSDisk** cmdlet gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="0c995-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c995-113">EXAMPLES</span></span>

### <span data-ttu-id="0c995-114">Beispiel 1: Abrufen eines Betriebssystemdatenträgers unter Verwendung eines Namens</span><span class="sxs-lookup"><span data-stu-id="0c995-114">Example 1: Get an operating system disk by using a name</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

<span data-ttu-id="0c995-115">Dieser Befehl ruft einen Betriebssystemdatenträger mit dem Namen ContosoOSDisk ab.</span><span class="sxs-lookup"><span data-stu-id="0c995-115">This command gets an operating system disk named ContosoOSDisk.</span></span>

### <span data-ttu-id="0c995-116">Beispiel 2: Abrufen eines Betriebssystemdatenträgers mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="0c995-116">Example 2: Get an operating system disk by using an ID</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="0c995-117">Mit diesem Befehl wird der Betriebssystemdatenträger mit der angegebenen ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0c995-117">This command gets the operating system disk that has the specified ID.</span></span>

### <span data-ttu-id="0c995-118">Beispiel 3: Abrufen aller Betriebssystemdatenträger</span><span class="sxs-lookup"><span data-stu-id="0c995-118">Example 3: Get all operating system disks</span></span>
```
PS C:\> Get-WAPackVMOSDisk
```

<span data-ttu-id="0c995-119">Dieser Befehl ruft alle Betriebssystemdatenträger ab.</span><span class="sxs-lookup"><span data-stu-id="0c995-119">This command gets all operating system disks.</span></span>

## <span data-ttu-id="0c995-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c995-120">PARAMETERS</span></span>

### <span data-ttu-id="0c995-121">-ID</span><span class="sxs-lookup"><span data-stu-id="0c995-121">-ID</span></span>
<span data-ttu-id="0c995-122">Gibt die eindeutige ID eines Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="0c995-122">Specifies the unique ID of an operating system disk.</span></span>

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

### <span data-ttu-id="0c995-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0c995-123">-Name</span></span>
<span data-ttu-id="0c995-124">Gibt den Namen eines Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="0c995-124">Specifies the name of an operating system disk.</span></span>

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

### <span data-ttu-id="0c995-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="0c995-125">-Profile</span></span>
<span data-ttu-id="0c995-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0c995-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0c995-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0c995-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0c995-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c995-128">CommonParameters</span></span>
<span data-ttu-id="0c995-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c995-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c995-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c995-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c995-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c995-131">INPUTS</span></span>

## <span data-ttu-id="0c995-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c995-132">OUTPUTS</span></span>

## <span data-ttu-id="0c995-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c995-133">NOTES</span></span>

## <span data-ttu-id="0c995-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c995-134">RELATED LINKS</span></span>

[<span data-ttu-id="0c995-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="0c995-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


