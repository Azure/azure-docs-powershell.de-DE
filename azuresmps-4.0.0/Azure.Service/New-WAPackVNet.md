---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CB2936E4-E403-44B3-9CB8-617308E54C50
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9059e5bad8441f25846cf98a12c5e8dada2e814a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007603"
---
# <span data-ttu-id="fc0b2-101">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="fc0b2-101">New-WAPackVNet</span></span>

## <span data-ttu-id="fc0b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0b2-103">Erstellt ein virtualisiertes Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-103">Creates a virtualized network.</span></span>

## <span data-ttu-id="fc0b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc0b2-104">SYNTAX</span></span>

```
New-WAPackVNet -LogicalNetwork <LogicalNetwork> -Name <String> [-Description <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fc0b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc0b2-105">DESCRIPTION</span></span>
<span data-ttu-id="fc0b2-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="fc0b2-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fc0b2-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="fc0b2-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fc0b2-109">Mit dem Cmdlet **New-WAPackVNet** wird ein virtualisiertes Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-109">The **New-WAPackVNet** cmdlet creates a virtualized network.</span></span>

## <span data-ttu-id="fc0b2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc0b2-110">EXAMPLES</span></span>

### <span data-ttu-id="fc0b2-111">Beispiel 1: Erstellen eines virtualisierten Netzwerks</span><span class="sxs-lookup"><span data-stu-id="fc0b2-111">Example 1: Create a virtualized network</span></span>
```
PS C:\> $LogicalNetwork = Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
PS C:\> New-WAPackVNet -LogicalNetwork $LogicalNetwork -Name "ContosoVNett01" -Description "A description"
```

<span data-ttu-id="fc0b2-112">Der erste Befehl ruft zuerst das logische Netzwerk ab, dem ein neues virtualisiertes Netzwerk hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-112">The first command first retrieves the logical network to which we want to add a new virtualized network.</span></span>
<span data-ttu-id="fc0b2-113">Dieses logische Netzwerk hat den Namen ContosoLogicalNetwork01.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-113">This logical network is named ContosoLogicalNetwork01.</span></span>

<span data-ttu-id="fc0b2-114">Mit dem zweiten und letzten Befehl wird ein virtualisiertes Netzwerk mit dem zuvor abgerufenen logischen Netzwerk, einem Namen (ContosoVNett01) und einer Beschreibung (Beschreibung) erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-114">The second and last command creates a virtualized network using the previously retrieved logical network, a name (ContosoVNett01) and a description (A description).</span></span>

## <span data-ttu-id="fc0b2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc0b2-115">PARAMETERS</span></span>

### <span data-ttu-id="fc0b2-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc0b2-116">-Description</span></span>
<span data-ttu-id="fc0b2-117">Gibt eine Beschreibung für das virtualisierte Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-117">Specifies a description for the virtualized network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0b2-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="fc0b2-118">-LogicalNetwork</span></span>
<span data-ttu-id="fc0b2-119">Gibt einen LogicalNetwork an, der dem virtualisierten Netzwerk zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-119">Specifies a LogicalNetwork associated with the virtualized network.</span></span>

```yaml
Type: LogicalNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0b2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fc0b2-120">-Name</span></span>
<span data-ttu-id="fc0b2-121">Gibt einen Namen für das virtualisierte Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-121">Specifies a name for the virtualized network.</span></span>

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

### <span data-ttu-id="fc0b2-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="fc0b2-122">-Profile</span></span>
<span data-ttu-id="fc0b2-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fc0b2-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fc0b2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0b2-125">CommonParameters</span></span>
<span data-ttu-id="fc0b2-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc0b2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0b2-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc0b2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0b2-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc0b2-128">INPUTS</span></span>

## <span data-ttu-id="fc0b2-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc0b2-129">OUTPUTS</span></span>

## <span data-ttu-id="fc0b2-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc0b2-130">NOTES</span></span>

## <span data-ttu-id="fc0b2-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc0b2-131">RELATED LINKS</span></span>

[<span data-ttu-id="fc0b2-132">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="fc0b2-132">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="fc0b2-133">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="fc0b2-133">Remove-WAPackVNet</span></span>](./Remove-WAPackVNet.md)


