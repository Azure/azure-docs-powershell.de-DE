---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5CAF2D29-F4AE-4322-AA4F-61267723B955
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2e19ad4b56e5141458f1fe9305a0c33691d024d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005703"
---
# <span data-ttu-id="1e461-101">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="1e461-101">Remove-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="1e461-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e461-102">SYNOPSIS</span></span>
<span data-ttu-id="1e461-103">Entfernt die Datenträgerkonfiguration aus dem DiskConfigSet-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1e461-103">Removes the data disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="1e461-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e461-104">SYNTAX</span></span>

### <span data-ttu-id="1e461-105">RemoveByDiskName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1e461-105">RemoveByDiskName (Default)</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1e461-106">RemoveByDiskLun</span><span class="sxs-lookup"><span data-stu-id="1e461-106">RemoveByDiskLun</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1e461-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e461-107">DESCRIPTION</span></span>
<span data-ttu-id="1e461-108">Das Cmdlet **Remove-AzureVMImageDataDiskConfig** entfernt die Daten Festplattenkonfiguration aus dem **DiskConfigSet** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1e461-108">The **Remove-AzureVMImageDataDiskConfig** cmdlet removes the data disk configuration from the **DiskConfigSet** object.</span></span>

## <span data-ttu-id="1e461-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e461-109">EXAMPLES</span></span>

### <span data-ttu-id="1e461-110">Beispiel 1: Entfernen der Datenträgerkonfiguration aus dem DiskConfigSet-Objekt</span><span class="sxs-lookup"><span data-stu-id="1e461-110">Example 1: Remove the data disk configuration from the DiskConfigSet object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="1e461-111">In diesem Beispiel wird ein **DiskConfigSet** erstellt, konfiguriert und dann der Daten Datenträger entfernt.</span><span class="sxs-lookup"><span data-stu-id="1e461-111">This example creates a **DiskConfigSet** , configures it, then removes the data disk.</span></span>

## <span data-ttu-id="1e461-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e461-112">PARAMETERS</span></span>

### <span data-ttu-id="1e461-113">-Datadiskname</span><span class="sxs-lookup"><span data-stu-id="1e461-113">-DataDiskName</span></span>
<span data-ttu-id="1e461-114">Gibt den Namen des Daten Datenträgers an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="1e461-114">Specifies the name of the data disk that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDiskName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e461-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="1e461-115">-DiskConfig</span></span>
<span data-ttu-id="1e461-116">Gibt das Datenträger Konfigurationsobjekt an, das die Datenträgerobjekte des Betriebssystems kapselt.</span><span class="sxs-lookup"><span data-stu-id="1e461-116">Specifies the disk configuration object that encapsulates the operating system disk and data disk objects.</span></span>

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

### <span data-ttu-id="1e461-117">-Information</span><span class="sxs-lookup"><span data-stu-id="1e461-117">-InformationAction</span></span>
<span data-ttu-id="1e461-118">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="1e461-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1e461-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1e461-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e461-120">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="1e461-120">Continue</span></span>
- <span data-ttu-id="1e461-121">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="1e461-121">Ignore</span></span>
- <span data-ttu-id="1e461-122">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="1e461-122">Inquire</span></span>
- <span data-ttu-id="1e461-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1e461-123">SilentlyContinue</span></span>
- <span data-ttu-id="1e461-124">Beenden</span><span class="sxs-lookup"><span data-stu-id="1e461-124">Stop</span></span>
- <span data-ttu-id="1e461-125">Anhalten</span><span class="sxs-lookup"><span data-stu-id="1e461-125">Suspend</span></span>

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

### <span data-ttu-id="1e461-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1e461-126">-InformationVariable</span></span>
<span data-ttu-id="1e461-127">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="1e461-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1e461-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="1e461-128">-Lun</span></span>
<span data-ttu-id="1e461-129">Gibt den Steckplatz an, in dem das Datenlaufwerk auf dem virtuellen Computer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1e461-129">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveByDiskLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e461-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e461-130">CommonParameters</span></span>
<span data-ttu-id="1e461-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e461-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e461-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e461-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e461-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e461-133">INPUTS</span></span>

## <span data-ttu-id="1e461-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e461-134">OUTPUTS</span></span>

### <span data-ttu-id="1e461-135">Microsoft. WindowsAzure. Commands. Servicemanagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="1e461-135">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="1e461-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e461-136">NOTES</span></span>

## <span data-ttu-id="1e461-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e461-137">RELATED LINKS</span></span>

[<span data-ttu-id="1e461-138">Satz-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="1e461-138">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


