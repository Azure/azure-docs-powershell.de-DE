---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA2E37AB-F137-4A62-9ABC-90565305A23B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6d1bbac3db6f69f5cdda14870de20eee7f8170b
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007563"
---
# <span data-ttu-id="e9d3b-101">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="e9d3b-101">New-WAPackCloudService</span></span>

## <span data-ttu-id="e9d3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d3b-103">Erstellt einen clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e9d3b-103">Creates a cloud service.</span></span>

## <span data-ttu-id="e9d3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9d3b-104">SYNTAX</span></span>

```
New-WAPackCloudService -Name <String> -Label <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e9d3b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9d3b-105">DESCRIPTION</span></span>
<span data-ttu-id="e9d3b-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="e9d3b-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="e9d3b-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e9d3b-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e9d3b-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e9d3b-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e9d3b-109">Das Cmdlet **New-WAPackCloudService** erstellt einen clouddienst.</span><span class="sxs-lookup"><span data-stu-id="e9d3b-109">The **New-WAPackCloudService** cmdlet creates a cloud service.</span></span>

## <span data-ttu-id="e9d3b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9d3b-110">EXAMPLES</span></span>

### <span data-ttu-id="e9d3b-111">Beispiel 1: Erstellen eines Cloud-Diensts</span><span class="sxs-lookup"><span data-stu-id="e9d3b-111">Example 1: Create a cloud service</span></span>
```
PS C:\> New-WAPackCloudService -Name "ContosoCloudService01" -Label "A label"
```

<span data-ttu-id="e9d3b-112">Der Befehl erstellt einen clouddienst mit dem Namen ContosoCloudService01 mit einer Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="e9d3b-112">The command creates a cloud service named ContosoCloudService01 with a label.</span></span>

## <span data-ttu-id="e9d3b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9d3b-113">PARAMETERS</span></span>

### <span data-ttu-id="e9d3b-114">-Label</span><span class="sxs-lookup"><span data-stu-id="e9d3b-114">-Label</span></span>
<span data-ttu-id="e9d3b-115">Gibt eine Bezeichnung für den cloudbasierten Dienst an.</span><span class="sxs-lookup"><span data-stu-id="e9d3b-115">Specifies a label for the cloud service.</span></span>

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

### <span data-ttu-id="e9d3b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e9d3b-116">-Name</span></span>
<span data-ttu-id="e9d3b-117">Gibt einen Namen für den cloudservice an.</span><span class="sxs-lookup"><span data-stu-id="e9d3b-117">Specifies a name for the cloudservice.</span></span>

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

### <span data-ttu-id="e9d3b-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="e9d3b-118">-Profile</span></span>
<span data-ttu-id="e9d3b-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e9d3b-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9d3b-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e9d3b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e9d3b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d3b-121">CommonParameters</span></span>
<span data-ttu-id="e9d3b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9d3b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d3b-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9d3b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d3b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9d3b-124">INPUTS</span></span>

## <span data-ttu-id="e9d3b-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9d3b-125">OUTPUTS</span></span>

## <span data-ttu-id="e9d3b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9d3b-126">NOTES</span></span>

## <span data-ttu-id="e9d3b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9d3b-127">RELATED LINKS</span></span>

[<span data-ttu-id="e9d3b-128">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="e9d3b-128">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="e9d3b-129">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="e9d3b-129">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


