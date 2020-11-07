---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/test-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: ae4a6d72fcb44406773234b6de55cec7ccef8eb9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850887"
---
# <span data-ttu-id="aa37d-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="aa37d-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="aa37d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa37d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa37d-103">Überprüft die Konfiguration der AEM-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="aa37d-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa37d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa37d-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa37d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa37d-105">DESCRIPTION</span></span>
<span data-ttu-id="aa37d-106">Das Cmdlet **Test-AzureRmVMAEMExtension** überprüft die Konfiguration der Erweiterung Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="aa37d-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="aa37d-107">Die AEM-Erweiterung sammelt die Leistungsdaten.</span><span class="sxs-lookup"><span data-stu-id="aa37d-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="aa37d-108">Dieses Cmdlet überprüft, ob Leistungsdaten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="aa37d-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="aa37d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa37d-109">EXAMPLES</span></span>

### <span data-ttu-id="aa37d-110">Beispiel 1: Überprüfen der Konfiguration der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="aa37d-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="aa37d-111">Dieser Befehl überprüft die Konfiguration der AEM-Erweiterung für den virtuellen Computer mit dem Namen Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="aa37d-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="aa37d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa37d-112">PARAMETERS</span></span>

### <span data-ttu-id="aa37d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa37d-113">-DefaultProfile</span></span>
<span data-ttu-id="aa37d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa37d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa37d-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="aa37d-115">-OSType</span></span>
<span data-ttu-id="aa37d-116">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="aa37d-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="aa37d-117">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="aa37d-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="aa37d-118">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="aa37d-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="aa37d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa37d-119">-ResourceGroupName</span></span>
<span data-ttu-id="aa37d-120">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, die von diesem Cmdlet überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="aa37d-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="aa37d-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="aa37d-121">-SkipStorageCheck</span></span>
<span data-ttu-id="aa37d-122">Gibt an, dass dieses Cmdlet die Überprüfung der Speicherkonfiguration überspringt.</span><span class="sxs-lookup"><span data-stu-id="aa37d-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="aa37d-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="aa37d-123">-VMName</span></span>
<span data-ttu-id="aa37d-124">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="aa37d-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="aa37d-125">Dieses Cmdlet testet die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="aa37d-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="aa37d-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="aa37d-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="aa37d-127">Gibt einen Timeoutzeitraum für die Überprüfung der Speicherkonfiguration in Minuten an.</span><span class="sxs-lookup"><span data-stu-id="aa37d-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="aa37d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa37d-128">CommonParameters</span></span>
<span data-ttu-id="aa37d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa37d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa37d-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa37d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa37d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa37d-131">INPUTS</span></span>

### <span data-ttu-id="aa37d-132">Keine</span><span class="sxs-lookup"><span data-stu-id="aa37d-132">None</span></span>
<span data-ttu-id="aa37d-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="aa37d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa37d-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa37d-134">OUTPUTS</span></span>

### <span data-ttu-id="aa37d-135">Microsoft. Azure. Commands. Compute. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="aa37d-135">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="aa37d-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa37d-136">NOTES</span></span>

## <span data-ttu-id="aa37d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa37d-137">RELATED LINKS</span></span>

[<span data-ttu-id="aa37d-138">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="aa37d-138">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="aa37d-139">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="aa37d-139">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="aa37d-140">Satz-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="aa37d-140">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


