---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 96248492feac9997d1afdba83fdda943c75fa363
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100397831"
---
# <span data-ttu-id="60a55-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="60a55-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="60a55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60a55-102">SYNOPSIS</span></span>
<span data-ttu-id="60a55-103">Ruft Startdiagnosedaten für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="60a55-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="60a55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60a55-104">SYNTAX</span></span>

### <span data-ttu-id="60a55-105">WindowsParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="60a55-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60a55-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="60a55-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60a55-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60a55-107">DESCRIPTION</span></span>
<span data-ttu-id="60a55-108">Das **Cmdlet "Get-AzVMBootDiagnosticsData"** ruft Startdiagnosedaten für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="60a55-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="60a55-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="60a55-109">EXAMPLES</span></span>

### <span data-ttu-id="60a55-110">Beispiel 1: Erhalten von Startdiagnosedaten</span><span class="sxs-lookup"><span data-stu-id="60a55-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="60a55-111">Dieser Befehl ruft Startdiagnosedaten für den virtuellen Computer "ContosoVM07" ab.</span><span class="sxs-lookup"><span data-stu-id="60a55-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="60a55-112">Dieser virtuelle Computer führt das Betriebssystem Windows aus.</span><span class="sxs-lookup"><span data-stu-id="60a55-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="60a55-113">Der Befehl speichert die Daten im angegebenen lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="60a55-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="60a55-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60a55-114">PARAMETERS</span></span>

### <span data-ttu-id="60a55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a55-115">-DefaultProfile</span></span>
<span data-ttu-id="60a55-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60a55-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60a55-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="60a55-117">-Linux</span></span>
<span data-ttu-id="60a55-118">Gibt an, dass der virtuelle Computer das Betriebssystem Linux ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="60a55-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a55-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="60a55-119">-LocalPath</span></span>
<span data-ttu-id="60a55-120">Gibt den lokalen Pfad für die Startdiagnosedaten an.</span><span class="sxs-lookup"><span data-stu-id="60a55-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a55-121">-Name</span><span class="sxs-lookup"><span data-stu-id="60a55-121">-Name</span></span>
<span data-ttu-id="60a55-122">Gibt den Namen des virtuellen Computers an, für den dieses Cmdlet Diagnosedaten erhält.</span><span class="sxs-lookup"><span data-stu-id="60a55-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a55-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a55-123">-ResourceGroupName</span></span>
<span data-ttu-id="60a55-124">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="60a55-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="60a55-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="60a55-125">-Windows</span></span>
<span data-ttu-id="60a55-126">Gibt an, dass der virtuelle Computer das Betriebssystem Windows ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="60a55-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a55-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a55-127">CommonParameters</span></span>
<span data-ttu-id="60a55-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a55-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a55-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60a55-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a55-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="60a55-130">INPUTS</span></span>

### <span data-ttu-id="60a55-131">System.String</span><span class="sxs-lookup"><span data-stu-id="60a55-131">System.String</span></span>

## <span data-ttu-id="60a55-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="60a55-132">OUTPUTS</span></span>

### <span data-ttu-id="60a55-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="60a55-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="60a55-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="60a55-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="60a55-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="60a55-135">NOTES</span></span>

## <span data-ttu-id="60a55-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="60a55-136">RELATED LINKS</span></span>

[<span data-ttu-id="60a55-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="60a55-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


