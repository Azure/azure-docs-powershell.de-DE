---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4BAD0DDE-80D4-4A89-AFFB-78C933D2C0D5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76771d8c0e8d06cbe134e920a06be5fc1b109fe2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007559"
---
# <span data-ttu-id="d9693-101">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="d9693-101">Get-WAPackCloudService</span></span>

## <span data-ttu-id="d9693-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9693-102">SYNOPSIS</span></span>
<span data-ttu-id="d9693-103">Ruft Cloud-Dienstobjekte ab.</span><span class="sxs-lookup"><span data-stu-id="d9693-103">Gets cloud service objects.</span></span>

## <span data-ttu-id="d9693-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9693-104">SYNTAX</span></span>

### <span data-ttu-id="d9693-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9693-105">Empty (Default)</span></span>
```
Get-WAPackCloudService [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d9693-106">FromName</span><span class="sxs-lookup"><span data-stu-id="d9693-106">FromName</span></span>
```
Get-WAPackCloudService [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d9693-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9693-107">DESCRIPTION</span></span>
<span data-ttu-id="d9693-108">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="d9693-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="d9693-109">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d9693-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d9693-110">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d9693-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d9693-111">Das Cmdlet " **Get-WAPackCloudService** " ruft Cloud-Dienstobjekte ab.</span><span class="sxs-lookup"><span data-stu-id="d9693-111">The **Get-WAPackCloudService** cmdlet gets cloud service objects.</span></span>

## <span data-ttu-id="d9693-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9693-112">EXAMPLES</span></span>

## <span data-ttu-id="d9693-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9693-113">PARAMETERS</span></span>

### <span data-ttu-id="d9693-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d9693-114">-Name</span></span>
<span data-ttu-id="d9693-115">Gibt den Namen eines Cloud-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="d9693-115">Specifies the name of a cloud service.</span></span>

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

### <span data-ttu-id="d9693-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="d9693-116">-Profile</span></span>
<span data-ttu-id="d9693-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d9693-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9693-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d9693-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d9693-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9693-119">CommonParameters</span></span>
<span data-ttu-id="d9693-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9693-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9693-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9693-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9693-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9693-122">INPUTS</span></span>

## <span data-ttu-id="d9693-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9693-123">OUTPUTS</span></span>

## <span data-ttu-id="d9693-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9693-124">NOTES</span></span>

## <span data-ttu-id="d9693-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9693-125">RELATED LINKS</span></span>

[<span data-ttu-id="d9693-126">Neu – WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="d9693-126">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)

[<span data-ttu-id="d9693-127">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="d9693-127">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


