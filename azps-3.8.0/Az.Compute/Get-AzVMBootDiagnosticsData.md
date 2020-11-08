---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: c56c9e586b0089311477fc12b6624c74321f9a0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005263"
---
# <span data-ttu-id="a689f-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="a689f-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="a689f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a689f-102">SYNOPSIS</span></span>
<span data-ttu-id="a689f-103">Ruft Start Diagnosedaten für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="a689f-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="a689f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a689f-104">SYNTAX</span></span>

### <span data-ttu-id="a689f-105">WindowsParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a689f-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a689f-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="a689f-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a689f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a689f-107">DESCRIPTION</span></span>
<span data-ttu-id="a689f-108">Das Cmdlet " **Get-AzVMBootDiagnosticsData** " ruft Start Diagnosedaten für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="a689f-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="a689f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a689f-109">EXAMPLES</span></span>

### <span data-ttu-id="a689f-110">Beispiel 1: Abrufen von Start Diagnosedaten</span><span class="sxs-lookup"><span data-stu-id="a689f-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="a689f-111">Dieser Befehl ruft Start Diagnosedaten für den virtuellen Computer mit dem Namen ContosoVM07 ab.</span><span class="sxs-lookup"><span data-stu-id="a689f-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="a689f-112">Auf diesem virtuellen Computer wird das Betriebssystem Windows ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a689f-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="a689f-113">Der Befehl speichert die Daten im angegebenen lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="a689f-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="a689f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a689f-114">PARAMETERS</span></span>

### <span data-ttu-id="a689f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a689f-115">-DefaultProfile</span></span>
<span data-ttu-id="a689f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a689f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a689f-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="a689f-117">-Linux</span></span>
<span data-ttu-id="a689f-118">Gibt an, dass auf dem virtuellen Computer das Linux-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a689f-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="a689f-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="a689f-119">-LocalPath</span></span>
<span data-ttu-id="a689f-120">Gibt den lokalen Pfad für die Start Diagnosedaten an.</span><span class="sxs-lookup"><span data-stu-id="a689f-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="a689f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a689f-121">-Name</span></span>
<span data-ttu-id="a689f-122">Gibt den Namen des virtuellen Computers an, für den dieses Cmdlet Diagnosedaten erhält.</span><span class="sxs-lookup"><span data-stu-id="a689f-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="a689f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a689f-123">-ResourceGroupName</span></span>
<span data-ttu-id="a689f-124">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="a689f-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a689f-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="a689f-125">-Windows</span></span>
<span data-ttu-id="a689f-126">Gibt an, dass auf dem virtuellen Computer das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a689f-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="a689f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a689f-127">CommonParameters</span></span>
<span data-ttu-id="a689f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a689f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a689f-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a689f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a689f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a689f-130">INPUTS</span></span>

### <span data-ttu-id="a689f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a689f-131">System.String</span></span>

## <span data-ttu-id="a689f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a689f-132">OUTPUTS</span></span>

### <span data-ttu-id="a689f-133">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a689f-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a689f-134">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="a689f-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="a689f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a689f-135">NOTES</span></span>

## <span data-ttu-id="a689f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a689f-136">RELATED LINKS</span></span>

[<span data-ttu-id="a689f-137">Satz-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a689f-137">Set-AzVMBootDiagnostics</span></span>](./Set-AzVMBootDiagnostics.md)


