---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 539e8b0a91c72d275f0997f2ebc69e86f4a9c901
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949547"
---
# <span data-ttu-id="66af1-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="66af1-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="66af1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66af1-102">SYNOPSIS</span></span>
<span data-ttu-id="66af1-103">Ruft Startdiagnosedaten für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="66af1-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="66af1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66af1-104">SYNTAX</span></span>

### <span data-ttu-id="66af1-105">WindowsParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="66af1-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66af1-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="66af1-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66af1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66af1-107">DESCRIPTION</span></span>
<span data-ttu-id="66af1-108">Das **Get-AzVMBootDiagnosticsData-Cmdlet** ruft Startdiagnosedaten für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="66af1-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="66af1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66af1-109">EXAMPLES</span></span>

### <span data-ttu-id="66af1-110">Beispiel 1: Starten von Diagnosedaten</span><span class="sxs-lookup"><span data-stu-id="66af1-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="66af1-111">Dieser Befehl ruft Startdiagnosedaten für den virtuellen Computer namens ContosoVM07 ab.</span><span class="sxs-lookup"><span data-stu-id="66af1-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="66af1-112">Auf diesem virtuellen Computer wird das Windows-Betriebssystem ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66af1-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="66af1-113">Der Befehl speichert die Daten im angegebenen lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="66af1-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="66af1-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="66af1-114">PARAMETERS</span></span>

### <span data-ttu-id="66af1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66af1-115">-DefaultProfile</span></span>
<span data-ttu-id="66af1-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66af1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66af1-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="66af1-117">-Linux</span></span>
<span data-ttu-id="66af1-118">Gibt an, dass auf dem virtuellen Computer das Linux-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66af1-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="66af1-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="66af1-119">-LocalPath</span></span>
<span data-ttu-id="66af1-120">Gibt den lokalen Pfad für die Startdiagnosedaten an.</span><span class="sxs-lookup"><span data-stu-id="66af1-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="66af1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="66af1-121">-Name</span></span>
<span data-ttu-id="66af1-122">Gibt den Namen des virtuellen Computers an, für den dieses Cmdlet Diagnosedaten erhält.</span><span class="sxs-lookup"><span data-stu-id="66af1-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="66af1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66af1-123">-ResourceGroupName</span></span>
<span data-ttu-id="66af1-124">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="66af1-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="66af1-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="66af1-125">-Windows</span></span>
<span data-ttu-id="66af1-126">Gibt an, dass auf dem virtuellen Computer das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66af1-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="66af1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66af1-127">CommonParameters</span></span>
<span data-ttu-id="66af1-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66af1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66af1-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66af1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66af1-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66af1-130">INPUTS</span></span>

### <span data-ttu-id="66af1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="66af1-131">System.String</span></span>

## <span data-ttu-id="66af1-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66af1-132">OUTPUTS</span></span>

### <span data-ttu-id="66af1-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="66af1-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="66af1-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="66af1-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="66af1-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="66af1-135">NOTES</span></span>

## <span data-ttu-id="66af1-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="66af1-136">RELATED LINKS</span></span>

[<span data-ttu-id="66af1-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="66af1-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


