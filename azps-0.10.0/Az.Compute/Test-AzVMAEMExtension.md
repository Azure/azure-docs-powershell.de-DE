---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 36fd9813523a5977c1981e6de54384cf71de7dc5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842451"
---
# <span data-ttu-id="35077-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="35077-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="35077-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35077-102">SYNOPSIS</span></span>
<span data-ttu-id="35077-103">Überprüft die Konfiguration der AEM-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="35077-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="35077-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35077-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35077-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35077-105">DESCRIPTION</span></span>
<span data-ttu-id="35077-106">Das Cmdlet **Test-AzVMAEMExtension** überprüft die Konfiguration der Erweiterung Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="35077-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="35077-107">Die AEM-Erweiterung sammelt die Leistungsdaten.</span><span class="sxs-lookup"><span data-stu-id="35077-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="35077-108">Dieses Cmdlet überprüft, ob Leistungsdaten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="35077-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="35077-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35077-109">EXAMPLES</span></span>

### <span data-ttu-id="35077-110">Beispiel 1: Überprüfen der Konfiguration der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="35077-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="35077-111">Dieser Befehl überprüft die Konfiguration der AEM-Erweiterung für den virtuellen Computer mit dem Namen Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="35077-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="35077-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="35077-112">PARAMETERS</span></span>

### <span data-ttu-id="35077-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35077-113">-DefaultProfile</span></span>
<span data-ttu-id="35077-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35077-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35077-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="35077-115">-OSType</span></span>
<span data-ttu-id="35077-116">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="35077-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="35077-117">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="35077-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="35077-118">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="35077-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="35077-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35077-119">-ResourceGroupName</span></span>
<span data-ttu-id="35077-120">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, die von diesem Cmdlet überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="35077-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="35077-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="35077-121">-SkipStorageCheck</span></span>
<span data-ttu-id="35077-122">Gibt an, dass dieses Cmdlet die Überprüfung der Speicherkonfiguration überspringt.</span><span class="sxs-lookup"><span data-stu-id="35077-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="35077-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="35077-123">-VMName</span></span>
<span data-ttu-id="35077-124">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="35077-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="35077-125">Dieses Cmdlet testet die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="35077-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="35077-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="35077-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="35077-127">Gibt einen Timeoutzeitraum für die Überprüfung der Speicherkonfiguration in Minuten an.</span><span class="sxs-lookup"><span data-stu-id="35077-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="35077-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35077-128">CommonParameters</span></span>
<span data-ttu-id="35077-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35077-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35077-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35077-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35077-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35077-131">INPUTS</span></span>

### <span data-ttu-id="35077-132">Keine</span><span class="sxs-lookup"><span data-stu-id="35077-132">None</span></span>
<span data-ttu-id="35077-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="35077-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="35077-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35077-134">OUTPUTS</span></span>

### <span data-ttu-id="35077-135">Microsoft. Azure. Commands. Compute. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="35077-135">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="35077-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="35077-136">NOTES</span></span>

## <span data-ttu-id="35077-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35077-137">RELATED LINKS</span></span>

[<span data-ttu-id="35077-138">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="35077-138">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="35077-139">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="35077-139">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="35077-140">Satz-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="35077-140">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


