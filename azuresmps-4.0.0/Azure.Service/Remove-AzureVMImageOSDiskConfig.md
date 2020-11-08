---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1E1F98E9-FC45-4BEF-90F6-A21D7DB7C82F
online version: ''
schema: 2.0.0
ms.openlocfilehash: eac6db4400e5c51f295e0bbf549117ffdbc97644
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006651"
---
# <span data-ttu-id="5fcf3-101">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="5fcf3-101">Remove-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="5fcf3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5fcf3-102">SYNOPSIS</span></span>
<span data-ttu-id="5fcf3-103">Entfernt die Konfiguration des Betriebssystemdatenträgers aus dem DiskConfigSet-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-103">Removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="5fcf3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fcf3-104">SYNTAX</span></span>

```
Remove-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5fcf3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fcf3-105">DESCRIPTION</span></span>
<span data-ttu-id="5fcf3-106">Das Cmdlet **Remove-AzureVMImageOSDiskConfig** entfernt die Festplattenkonfiguration des Betriebssystems aus dem DiskConfigSet-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-106">The **Remove-AzureVMImageOSDiskConfig** cmdlet removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="5fcf3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5fcf3-107">EXAMPLES</span></span>

### <span data-ttu-id="5fcf3-108">Beispiel 1: Entfernen der Festplattenkonfiguration des Betriebssystems von einem DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="5fcf3-108">Example 1: Remove the operating system disk configuration from a DiskConfigSet</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageOSDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="5fcf3-109">Mit diesem Befehl wird die Festplattenkonfiguration des Betriebssystems aus dem DiskConfigSet-Objekt entfernt</span><span class="sxs-lookup"><span data-stu-id="5fcf3-109">This command removes the operating system disk configuration from the DiskConfigSet object</span></span>

## <span data-ttu-id="5fcf3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fcf3-110">PARAMETERS</span></span>

### <span data-ttu-id="5fcf3-111">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="5fcf3-111">-DiskConfig</span></span>
<span data-ttu-id="5fcf3-112">Gibt das Datenträger Konfigurationsobjekt an, das die Datenträgerobjekte des Betriebssystems kapselt.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-112">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcf3-113">-Information</span><span class="sxs-lookup"><span data-stu-id="5fcf3-113">-InformationAction</span></span>
<span data-ttu-id="5fcf3-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5fcf3-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5fcf3-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5fcf3-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="5fcf3-116">Continue</span></span>
- <span data-ttu-id="5fcf3-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="5fcf3-117">Ignore</span></span>
- <span data-ttu-id="5fcf3-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="5fcf3-118">Inquire</span></span>
- <span data-ttu-id="5fcf3-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5fcf3-119">SilentlyContinue</span></span>
- <span data-ttu-id="5fcf3-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="5fcf3-120">Stop</span></span>
- <span data-ttu-id="5fcf3-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="5fcf3-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fcf3-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5fcf3-122">-InformationVariable</span></span>
<span data-ttu-id="5fcf3-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fcf3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fcf3-124">CommonParameters</span></span>
<span data-ttu-id="5fcf3-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fcf3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fcf3-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fcf3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fcf3-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5fcf3-127">INPUTS</span></span>

## <span data-ttu-id="5fcf3-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5fcf3-128">OUTPUTS</span></span>

### <span data-ttu-id="5fcf3-129">Microsoft. WindowsAzure. Commands. Servicemanagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="5fcf3-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="5fcf3-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="5fcf3-130">NOTES</span></span>

## <span data-ttu-id="5fcf3-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5fcf3-131">RELATED LINKS</span></span>

[<span data-ttu-id="5fcf3-132">Satz-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="5fcf3-132">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)


