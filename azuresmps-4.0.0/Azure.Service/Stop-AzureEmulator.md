---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 43E2C42E-16A3-426E-A7C4-33942F06F908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 501a164fc4470a3d4fd6163050fba495ce3d2705
ms.sourcegitcommit: 25eca7b5f5480758aa2cd830458900cf91cf673c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "95515090"
---
# <span data-ttu-id="33606-101">Stop-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="33606-101">Stop-AzureEmulator</span></span>

## <span data-ttu-id="33606-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33606-102">SYNOPSIS</span></span>
<span data-ttu-id="33606-103">Beendet den Compute-Emulator.</span><span class="sxs-lookup"><span data-stu-id="33606-103">Stops the compute emulator.</span></span>

## <span data-ttu-id="33606-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33606-104">SYNTAX</span></span>

```
Stop-AzureEmulator [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="33606-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33606-105">DESCRIPTION</span></span>
<span data-ttu-id="33606-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="33606-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="33606-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="33606-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="33606-108">Das Cmdlet **Stop-AzureEmulator** beendet den Azure Compute-Emulator.</span><span class="sxs-lookup"><span data-stu-id="33606-108">The **Stop-AzureEmulator** cmdlet stops the Azure Compute Emulator.</span></span>
<span data-ttu-id="33606-109">Alle Dienste, die derzeit im Emulator ausgeführt werden, werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="33606-109">Any services currently running in the emulator are removed.</span></span>

## <span data-ttu-id="33606-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33606-110">EXAMPLES</span></span>

## <span data-ttu-id="33606-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="33606-111">PARAMETERS</span></span>

### <span data-ttu-id="33606-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33606-112">-PassThru</span></span>
<span data-ttu-id="33606-113">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="33606-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="33606-114">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="33606-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="33606-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="33606-115">-Profile</span></span>
<span data-ttu-id="33606-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="33606-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="33606-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="33606-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="33606-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33606-118">CommonParameters</span></span>
<span data-ttu-id="33606-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33606-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33606-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33606-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33606-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33606-121">INPUTS</span></span>

## <span data-ttu-id="33606-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33606-122">OUTPUTS</span></span>

## <span data-ttu-id="33606-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="33606-123">NOTES</span></span>

## <span data-ttu-id="33606-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33606-124">RELATED LINKS</span></span>

[<span data-ttu-id="33606-125">Anfang-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="33606-125">Start-AzureEmulator</span></span>](./Start-AzureEmulator.md)


