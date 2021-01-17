---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: ffc22a8937e56537de167046f661ee4b5d262fed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302568"
---
# <span data-ttu-id="93fbb-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="93fbb-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="93fbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="93fbb-103">Überprüft die Konfiguration der AEM-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="93fbb-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="93fbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93fbb-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93fbb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93fbb-105">DESCRIPTION</span></span>
<span data-ttu-id="93fbb-106">Das **Cmdlet "Test-AzVMAEMExtension"** überprüft die Konfiguration der Azure Enhanced Monitoring (AEM)-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="93fbb-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="93fbb-107">Die Erweiterung AEM sammelt die Leistungsdaten.</span><span class="sxs-lookup"><span data-stu-id="93fbb-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="93fbb-108">Dieses Cmdlet überprüft, ob Leistungsdaten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="93fbb-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="93fbb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="93fbb-109">EXAMPLES</span></span>

### <span data-ttu-id="93fbb-110">Beispiel 1: Überprüfen der Konfiguration der Erweiterung AEM</span><span class="sxs-lookup"><span data-stu-id="93fbb-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="93fbb-111">Mit diesem Befehl wird die Konfiguration der Erweiterung AEM für den virtuellen Computer "contoso-server" überprüft.</span><span class="sxs-lookup"><span data-stu-id="93fbb-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="93fbb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93fbb-112">PARAMETERS</span></span>

### <span data-ttu-id="93fbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93fbb-113">-DefaultProfile</span></span>
<span data-ttu-id="93fbb-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93fbb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93fbb-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="93fbb-115">-OSType</span></span>
<span data-ttu-id="93fbb-116">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="93fbb-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="93fbb-117">Wenn der Betriebssystemdatenträger keinen Typ hat, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="93fbb-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="93fbb-118">Die zulässigen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="93fbb-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="93fbb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93fbb-119">-ResourceGroupName</span></span>
<span data-ttu-id="93fbb-120">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, den dieses Cmdlet überprüft.</span><span class="sxs-lookup"><span data-stu-id="93fbb-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="93fbb-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="93fbb-121">-SkipStorageCheck</span></span>
<span data-ttu-id="93fbb-122">Gibt an, dass dieses Cmdlet die Überprüfung der Speicherkonfiguration überspringt.</span><span class="sxs-lookup"><span data-stu-id="93fbb-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="93fbb-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="93fbb-123">-VMName</span></span>
<span data-ttu-id="93fbb-124">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="93fbb-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="93fbb-125">Dieses Cmdlet testet die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="93fbb-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="93fbb-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="93fbb-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="93fbb-127">Gibt einen Zeitraum in Minuten für die Speicherkonfigurationsprüfung an.</span><span class="sxs-lookup"><span data-stu-id="93fbb-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="93fbb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93fbb-128">CommonParameters</span></span>
<span data-ttu-id="93fbb-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93fbb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93fbb-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93fbb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93fbb-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="93fbb-131">INPUTS</span></span>

### <span data-ttu-id="93fbb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="93fbb-132">System.String</span></span>

## <span data-ttu-id="93fbb-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="93fbb-133">OUTPUTS</span></span>

### <span data-ttu-id="93fbb-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="93fbb-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="93fbb-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="93fbb-135">NOTES</span></span>

## <span data-ttu-id="93fbb-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="93fbb-136">RELATED LINKS</span></span>

[<span data-ttu-id="93fbb-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="93fbb-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="93fbb-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="93fbb-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="93fbb-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="93fbb-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


