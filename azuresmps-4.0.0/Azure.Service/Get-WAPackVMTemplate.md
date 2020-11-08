---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007597"
---
# <span data-ttu-id="c6e2d-101">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="c6e2d-101">Get-WAPackVMTemplate</span></span>

## <span data-ttu-id="c6e2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e2d-103">Ruft Vorlagen für virtuelle Computer ab.</span><span class="sxs-lookup"><span data-stu-id="c6e2d-103">Gets virtual machine templates.</span></span>

## <span data-ttu-id="c6e2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6e2d-104">SYNTAX</span></span>

### <span data-ttu-id="c6e2d-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6e2d-105">Empty (Default)</span></span>
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c6e2d-106">FromId</span><span class="sxs-lookup"><span data-stu-id="c6e2d-106">FromId</span></span>
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c6e2d-107">FromName</span><span class="sxs-lookup"><span data-stu-id="c6e2d-107">FromName</span></span>
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c6e2d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6e2d-108">DESCRIPTION</span></span>
<span data-ttu-id="c6e2d-109">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="c6e2d-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="c6e2d-110">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c6e2d-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c6e2d-111">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c6e2d-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c6e2d-112">Das Cmdlet " **Get-WAPackVMTemplate** " ruft Vorlagen für virtuelle Computer ab.</span><span class="sxs-lookup"><span data-stu-id="c6e2d-112">The **Get-WAPackVMTemplate** cmdlet gets virtual machine templates.</span></span>

## <span data-ttu-id="c6e2d-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6e2d-113">EXAMPLES</span></span>

### <span data-ttu-id="c6e2d-114">Beispiel 1: Abrufen einer Vorlage für einen virtuellen Computer mit einem Namen</span><span class="sxs-lookup"><span data-stu-id="c6e2d-114">Example 1: Get a virtual machine template by using a name</span></span>
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

<span data-ttu-id="c6e2d-115">Mit diesem Befehl wird die Vorlage für den virtuellen Computer mit dem Namen ContosoTemplate04 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c6e2d-115">This command gets the virtual machine template named ContosoTemplate04.</span></span>

### <span data-ttu-id="c6e2d-116">Beispiel 2: Abrufen einer Vorlage für einen virtuellen Computer mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="c6e2d-116">Example 2: Get a virtual machine template by using an ID</span></span>
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="c6e2d-117">Dieser Befehl ruft die Vorlage für den virtuellen Computer ab, die die angegebene ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="c6e2d-117">This command gets the virtual machine template that has the specified ID.</span></span>

### <span data-ttu-id="c6e2d-118">Beispiel 3: Abrufen aller Vorlagen für virtuelle Computer</span><span class="sxs-lookup"><span data-stu-id="c6e2d-118">Example 3: Get all virtual machine templates</span></span>
```
PS C:\> Get-WAPackVMTemplate
```

<span data-ttu-id="c6e2d-119">Dieser Befehl ruft alle Vorlagen für virtuelle Computer ab.</span><span class="sxs-lookup"><span data-stu-id="c6e2d-119">This command gets all the virtual machine templates.</span></span>

## <span data-ttu-id="c6e2d-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6e2d-120">PARAMETERS</span></span>

### <span data-ttu-id="c6e2d-121">-ID</span><span class="sxs-lookup"><span data-stu-id="c6e2d-121">-ID</span></span>
<span data-ttu-id="c6e2d-122">Gibt die eindeutige ID einer Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="c6e2d-122">Specifies the unique ID of a template.</span></span>

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

### <span data-ttu-id="c6e2d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c6e2d-123">-Name</span></span>
<span data-ttu-id="c6e2d-124">Gibt den Namen einer Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="c6e2d-124">Specifies the name of a template.</span></span>

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

### <span data-ttu-id="c6e2d-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="c6e2d-125">-Profile</span></span>
<span data-ttu-id="c6e2d-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c6e2d-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c6e2d-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c6e2d-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6e2d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e2d-128">CommonParameters</span></span>
<span data-ttu-id="c6e2d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e2d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e2d-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e2d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e2d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6e2d-131">INPUTS</span></span>

## <span data-ttu-id="c6e2d-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6e2d-132">OUTPUTS</span></span>

## <span data-ttu-id="c6e2d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6e2d-133">NOTES</span></span>

## <span data-ttu-id="c6e2d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6e2d-134">RELATED LINKS</span></span>

[<span data-ttu-id="c6e2d-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="c6e2d-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


