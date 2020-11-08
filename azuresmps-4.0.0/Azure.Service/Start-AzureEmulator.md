---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006237"
---
# <span data-ttu-id="353b2-101">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="353b2-101">Start-AzureEmulator</span></span>

## <span data-ttu-id="353b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="353b2-102">SYNOPSIS</span></span>
<span data-ttu-id="353b2-103">Startet die COMPUTE-und Speicher Emulatoren.</span><span class="sxs-lookup"><span data-stu-id="353b2-103">Starts the compute and storage emulators.</span></span>

## <span data-ttu-id="353b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="353b2-104">SYNTAX</span></span>

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="353b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="353b2-105">DESCRIPTION</span></span>
<span data-ttu-id="353b2-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="353b2-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="353b2-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="353b2-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="353b2-108">Das Cmdlet **Start-AzureEmulator** startet sowohl den Compute-als auch den Speicheremulator und hostet den aktuellen Dienst im COMPUTE-Emulator.</span><span class="sxs-lookup"><span data-stu-id="353b2-108">The **Start-AzureEmulator** cmdlet starts both the compute and storage emulators and hosts the current service in the compute emulator.</span></span>

## <span data-ttu-id="353b2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="353b2-109">EXAMPLES</span></span>

### <span data-ttu-id="353b2-110">Beispiel 1: Starten des Emulators und Starten eines Browsers</span><span class="sxs-lookup"><span data-stu-id="353b2-110">Example 1: Start the emulator and launch a browser</span></span>
```
PS C:\> Start-AzureEmulator -L
```

<span data-ttu-id="353b2-111">In diesem Beispiel wird der Dienst im Azure-Emulator ausgeführt, und ein neues Browserfenster wird im emulierten Dienst gestartet.</span><span class="sxs-lookup"><span data-stu-id="353b2-111">This example runs the service in the Azure emulator and launches a new browser window on the emulated service.</span></span>

## <span data-ttu-id="353b2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="353b2-112">PARAMETERS</span></span>

### <span data-ttu-id="353b2-113">-Start</span><span class="sxs-lookup"><span data-stu-id="353b2-113">-Launch</span></span>
<span data-ttu-id="353b2-114">Öffnet ein neues Browserfenster im Dienst, nachdem es im Emulator gehostet wurde.</span><span class="sxs-lookup"><span data-stu-id="353b2-114">Opens a new browser window on the service after hosting it in the emulator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353b2-115">-Modus</span><span class="sxs-lookup"><span data-stu-id="353b2-115">-Mode</span></span>
<span data-ttu-id="353b2-116">Gibt den emulatormodus an.</span><span class="sxs-lookup"><span data-stu-id="353b2-116">Specifies the emulator mode.</span></span>
<span data-ttu-id="353b2-117">Gültige Werte sind: Full und Express.</span><span class="sxs-lookup"><span data-stu-id="353b2-117">Valid values are: Full and Express.</span></span>
<span data-ttu-id="353b2-118">Der Standardwert ist Express.</span><span class="sxs-lookup"><span data-stu-id="353b2-118">The default value is Express.</span></span>

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353b2-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="353b2-119">-Profile</span></span>
<span data-ttu-id="353b2-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="353b2-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="353b2-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="353b2-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="353b2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353b2-122">CommonParameters</span></span>
<span data-ttu-id="353b2-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="353b2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353b2-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="353b2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353b2-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="353b2-125">INPUTS</span></span>

## <span data-ttu-id="353b2-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="353b2-126">OUTPUTS</span></span>

## <span data-ttu-id="353b2-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="353b2-127">NOTES</span></span>

## <span data-ttu-id="353b2-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="353b2-128">RELATED LINKS</span></span>

[<span data-ttu-id="353b2-129">Neu – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="353b2-129">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="353b2-130">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="353b2-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="353b2-131">Stopp-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="353b2-131">Stop-AzureEmulator</span></span>](./Stop-AzureEmulator.md)


