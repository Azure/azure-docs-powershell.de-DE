---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 040e7e557934fc90e5609a42c2e553ccf34d2f8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948003"
---
# <span data-ttu-id="be17c-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="be17c-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="be17c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be17c-102">SYNOPSIS</span></span>
<span data-ttu-id="be17c-103">Überprüft die Konfiguration der Erweiterung AEM.</span><span class="sxs-lookup"><span data-stu-id="be17c-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="be17c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be17c-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be17c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be17c-105">DESCRIPTION</span></span>
<span data-ttu-id="be17c-106">Das **Cmdlet Test-AzVMAEMExtension** überprüft die Konfiguration der Azure Enhanced Monitoring (AEM)-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="be17c-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="be17c-107">Die Erweiterung AEM sammelt die Leistungsdaten.</span><span class="sxs-lookup"><span data-stu-id="be17c-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="be17c-108">Dieses Cmdlet überprüft, ob Leistungsdaten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="be17c-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="be17c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be17c-109">EXAMPLES</span></span>

### <span data-ttu-id="be17c-110">Beispiel 1: Überprüfen der Konfiguration der Erweiterung AEM</span><span class="sxs-lookup"><span data-stu-id="be17c-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="be17c-111">Dieser Befehl überprüft die Konfiguration der AEM-Erweiterung für den virtuellen Computer namens contoso-server.</span><span class="sxs-lookup"><span data-stu-id="be17c-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="be17c-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="be17c-112">PARAMETERS</span></span>

### <span data-ttu-id="be17c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be17c-113">-DefaultProfile</span></span>
<span data-ttu-id="be17c-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be17c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be17c-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="be17c-115">-OSType</span></span>
<span data-ttu-id="be17c-116">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="be17c-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="be17c-117">Wenn der Betriebssystemdatenträger keinen Typ hat, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="be17c-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="be17c-118">Die zulässigen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="be17c-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be17c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be17c-119">-ResourceGroupName</span></span>
<span data-ttu-id="be17c-120">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, den dieses Cmdlet überprüft.</span><span class="sxs-lookup"><span data-stu-id="be17c-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be17c-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="be17c-121">-SkipStorageCheck</span></span>
<span data-ttu-id="be17c-122">Gibt an, dass dieses Cmdlet die Überprüfung der Speicherkonfiguration überspringt.</span><span class="sxs-lookup"><span data-stu-id="be17c-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be17c-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="be17c-123">-VMName</span></span>
<span data-ttu-id="be17c-124">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="be17c-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="be17c-125">Dieses Cmdlet testet die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="be17c-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be17c-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="be17c-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="be17c-127">Gibt einen Zeitraum in Minuten für die Speicherkonfigurationsprüfung an.</span><span class="sxs-lookup"><span data-stu-id="be17c-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be17c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be17c-128">CommonParameters</span></span>
<span data-ttu-id="be17c-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be17c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be17c-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be17c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be17c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be17c-131">INPUTS</span></span>

### <span data-ttu-id="be17c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="be17c-132">System.String</span></span>

## <span data-ttu-id="be17c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be17c-133">OUTPUTS</span></span>

### <span data-ttu-id="be17c-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="be17c-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="be17c-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="be17c-135">NOTES</span></span>

## <span data-ttu-id="be17c-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="be17c-136">RELATED LINKS</span></span>

[<span data-ttu-id="be17c-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="be17c-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="be17c-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="be17c-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="be17c-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="be17c-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


