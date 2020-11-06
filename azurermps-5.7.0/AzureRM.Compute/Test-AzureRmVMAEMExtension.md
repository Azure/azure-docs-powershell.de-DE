---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: d766102b0e87968e59bdd9bf63157dd62e977a25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476914"
---
# <span data-ttu-id="8fae1-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8fae1-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="8fae1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fae1-102">SYNOPSIS</span></span>
<span data-ttu-id="8fae1-103">Überprüft die Konfiguration der AEM-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="8fae1-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fae1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fae1-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [<CommonParameters>]
```

## <span data-ttu-id="8fae1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fae1-105">DESCRIPTION</span></span>
<span data-ttu-id="8fae1-106">Das Cmdlet **Test-AzureRmVMAEMExtension** überprüft die Konfiguration der Erweiterung Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="8fae1-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="8fae1-107">Die AEM-Erweiterung sammelt die Leistungsdaten.</span><span class="sxs-lookup"><span data-stu-id="8fae1-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="8fae1-108">Dieses Cmdlet überprüft, ob Leistungsdaten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8fae1-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="8fae1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fae1-109">EXAMPLES</span></span>

### <span data-ttu-id="8fae1-110">Beispiel 1: Überprüfen der Konfiguration der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="8fae1-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="8fae1-111">Dieser Befehl überprüft die Konfiguration der AEM-Erweiterung für den virtuellen Computer mit dem Namen Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="8fae1-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="8fae1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fae1-112">PARAMETERS</span></span>

### <span data-ttu-id="8fae1-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="8fae1-113">-OSType</span></span>
<span data-ttu-id="8fae1-114">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="8fae1-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="8fae1-115">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="8fae1-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="8fae1-116">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="8fae1-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fae1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fae1-117">-ResourceGroupName</span></span>
<span data-ttu-id="8fae1-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, die von diesem Cmdlet überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="8fae1-118">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fae1-119">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="8fae1-119">-SkipStorageCheck</span></span>
<span data-ttu-id="8fae1-120">Gibt an, dass dieses Cmdlet die Überprüfung der Speicherkonfiguration überspringt.</span><span class="sxs-lookup"><span data-stu-id="8fae1-120">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fae1-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="8fae1-121">-VMName</span></span>
<span data-ttu-id="8fae1-122">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="8fae1-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="8fae1-123">Dieses Cmdlet testet die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8fae1-123">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fae1-124">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="8fae1-124">-WaitTimeInMinutes</span></span>
<span data-ttu-id="8fae1-125">Gibt einen Timeoutzeitraum für die Überprüfung der Speicherkonfiguration in Minuten an.</span><span class="sxs-lookup"><span data-stu-id="8fae1-125">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fae1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fae1-126">CommonParameters</span></span>
<span data-ttu-id="8fae1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fae1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fae1-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fae1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fae1-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fae1-129">INPUTS</span></span>

### <span data-ttu-id="8fae1-130">Keine</span><span class="sxs-lookup"><span data-stu-id="8fae1-130">None</span></span>
<span data-ttu-id="8fae1-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8fae1-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8fae1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fae1-132">OUTPUTS</span></span>

## <span data-ttu-id="8fae1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fae1-133">NOTES</span></span>

## <span data-ttu-id="8fae1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fae1-134">RELATED LINKS</span></span>

[<span data-ttu-id="8fae1-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8fae1-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="8fae1-136">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8fae1-136">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="8fae1-137">Satz-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8fae1-137">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


