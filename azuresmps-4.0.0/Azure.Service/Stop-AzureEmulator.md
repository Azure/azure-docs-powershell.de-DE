---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 43E2C42E-16A3-426E-A7C4-33942F06F908
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd94462eb89cff6b4cec97f05911e27dbb05c920
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005972"
---
# <span data-ttu-id="a43ac-101">Stop-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="a43ac-101">Stop-AzureEmulator</span></span>

## <span data-ttu-id="a43ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a43ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a43ac-103">Beendet den Compute-Emulator.</span><span class="sxs-lookup"><span data-stu-id="a43ac-103">Stops the compute emulator.</span></span>

## <span data-ttu-id="a43ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a43ac-104">SYNTAX</span></span>

```
Stop-AzureEmulator [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a43ac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a43ac-105">DESCRIPTION</span></span>
<span data-ttu-id="a43ac-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a43ac-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a43ac-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a43ac-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a43ac-108">Das Cmdlet **Stop-AzureEmulator** beendet den Azure Compute-Emulator.</span><span class="sxs-lookup"><span data-stu-id="a43ac-108">The **Stop-AzureEmulator** cmdlet stops the Azure compute emulator.</span></span>
<span data-ttu-id="a43ac-109">Alle Dienste, die derzeit im Emulator ausgeführt werden, werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="a43ac-109">Any services currently running in the emulator are removed.</span></span>

## <span data-ttu-id="a43ac-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a43ac-110">EXAMPLES</span></span>

## <span data-ttu-id="a43ac-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a43ac-111">PARAMETERS</span></span>

### <span data-ttu-id="a43ac-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a43ac-112">-PassThru</span></span>
<span data-ttu-id="a43ac-113">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a43ac-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a43ac-114">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a43ac-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a43ac-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="a43ac-115">-Profile</span></span>
<span data-ttu-id="a43ac-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a43ac-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a43ac-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a43ac-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a43ac-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43ac-118">CommonParameters</span></span>
<span data-ttu-id="a43ac-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a43ac-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43ac-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a43ac-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43ac-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a43ac-121">INPUTS</span></span>

## <span data-ttu-id="a43ac-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a43ac-122">OUTPUTS</span></span>

## <span data-ttu-id="a43ac-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="a43ac-123">NOTES</span></span>

## <span data-ttu-id="a43ac-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a43ac-124">RELATED LINKS</span></span>

[<span data-ttu-id="a43ac-125">Anfang-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="a43ac-125">Start-AzureEmulator</span></span>](./Start-AzureEmulator.md)


