---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007636"
---
# <span data-ttu-id="5126b-101">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="5126b-101">Get-WAPackVMSizeProfile</span></span>

## <span data-ttu-id="5126b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5126b-102">SYNOPSIS</span></span>
<span data-ttu-id="5126b-103">Ruft size-Profilobjekte ab.</span><span class="sxs-lookup"><span data-stu-id="5126b-103">Gets size profile objects.</span></span>

## <span data-ttu-id="5126b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5126b-104">SYNTAX</span></span>

### <span data-ttu-id="5126b-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="5126b-105">Empty (Default)</span></span>
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5126b-106">FromId</span><span class="sxs-lookup"><span data-stu-id="5126b-106">FromId</span></span>
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5126b-107">FromName</span><span class="sxs-lookup"><span data-stu-id="5126b-107">FromName</span></span>
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5126b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5126b-108">DESCRIPTION</span></span>
<span data-ttu-id="5126b-109">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="5126b-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="5126b-110">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5126b-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5126b-111">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5126b-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5126b-112">Das Cmdlet " **Get-WAPackVMSizeProfile** " ruft Größen Profilobjekte für virtuelle Computer ab.</span><span class="sxs-lookup"><span data-stu-id="5126b-112">The **Get-WAPackVMSizeProfile** cmdlet gets size profile objects for virtual machines.</span></span>

## <span data-ttu-id="5126b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5126b-113">EXAMPLES</span></span>

### <span data-ttu-id="5126b-114">Beispiel 1: Abrufen eines Größen Profils mithilfe eines Namens</span><span class="sxs-lookup"><span data-stu-id="5126b-114">Example 1: Get a size profile by using a name</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

<span data-ttu-id="5126b-115">Dieser Befehl ruft das Größen Profil mit dem Namen ContosoSizeProfile07 ab.</span><span class="sxs-lookup"><span data-stu-id="5126b-115">This command gets the size profile named ContosoSizeProfile07.</span></span>

### <span data-ttu-id="5126b-116">Beispiel 2: Abrufen eines Größen Profils mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="5126b-116">Example 2: Get a size profile by using an ID</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="5126b-117">Dieser Befehl ruft das Größen Profil ab, das die angegebene ID hat.</span><span class="sxs-lookup"><span data-stu-id="5126b-117">This command gets the size profile that has the specified ID.</span></span>

### <span data-ttu-id="5126b-118">Beispiel 3: Abrufen aller Größen profile</span><span class="sxs-lookup"><span data-stu-id="5126b-118">Example 3: Get all size profiles</span></span>
```
PS C:\> Get-WAPackVMSizeProfile
```

<span data-ttu-id="5126b-119">Dieser Befehl ruft alle Größen Profile ab.</span><span class="sxs-lookup"><span data-stu-id="5126b-119">This command gets all the size profiles.</span></span>

## <span data-ttu-id="5126b-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="5126b-120">PARAMETERS</span></span>

### <span data-ttu-id="5126b-121">-ID</span><span class="sxs-lookup"><span data-stu-id="5126b-121">-ID</span></span>
<span data-ttu-id="5126b-122">Gibt die eindeutige ID eines Größen Profils an.</span><span class="sxs-lookup"><span data-stu-id="5126b-122">Specifies the unique ID of a size profile.</span></span>

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

### <span data-ttu-id="5126b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5126b-123">-Name</span></span>
<span data-ttu-id="5126b-124">Gibt den Namen eines Größen Profils an.</span><span class="sxs-lookup"><span data-stu-id="5126b-124">Specifies the name of a size profile.</span></span>

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

### <span data-ttu-id="5126b-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="5126b-125">-Profile</span></span>
<span data-ttu-id="5126b-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5126b-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5126b-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5126b-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5126b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5126b-128">CommonParameters</span></span>
<span data-ttu-id="5126b-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5126b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5126b-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5126b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5126b-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5126b-131">INPUTS</span></span>

## <span data-ttu-id="5126b-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5126b-132">OUTPUTS</span></span>

## <span data-ttu-id="5126b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="5126b-133">NOTES</span></span>

## <span data-ttu-id="5126b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5126b-134">RELATED LINKS</span></span>

[<span data-ttu-id="5126b-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="5126b-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


