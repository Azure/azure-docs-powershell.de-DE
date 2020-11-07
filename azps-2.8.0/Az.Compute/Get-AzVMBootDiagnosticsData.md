---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 94e5a1087f870f8dbbe099962e69d83b64f52ed3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652155"
---
# <span data-ttu-id="0894b-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="0894b-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="0894b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0894b-102">SYNOPSIS</span></span>
<span data-ttu-id="0894b-103">Ruft Start Diagnosedaten für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="0894b-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="0894b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0894b-104">SYNTAX</span></span>

### <span data-ttu-id="0894b-105">WindowsParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0894b-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0894b-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="0894b-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0894b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0894b-107">DESCRIPTION</span></span>
<span data-ttu-id="0894b-108">Das Cmdlet " **Get-AzVMBootDiagnosticsData** " ruft Start Diagnosedaten für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="0894b-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="0894b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0894b-109">EXAMPLES</span></span>

### <span data-ttu-id="0894b-110">Beispiel 1: Abrufen von Start Diagnosedaten</span><span class="sxs-lookup"><span data-stu-id="0894b-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="0894b-111">Dieser Befehl ruft Start Diagnosedaten für den virtuellen Computer mit dem Namen ContosoVM07 ab.</span><span class="sxs-lookup"><span data-stu-id="0894b-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="0894b-112">Auf diesem virtuellen Computer wird das Betriebssystem Windows ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0894b-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="0894b-113">Der Befehl speichert die Daten im angegebenen lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="0894b-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="0894b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0894b-114">PARAMETERS</span></span>

### <span data-ttu-id="0894b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0894b-115">-DefaultProfile</span></span>
<span data-ttu-id="0894b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0894b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0894b-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="0894b-117">-Linux</span></span>
<span data-ttu-id="0894b-118">Gibt an, dass auf dem virtuellen Computer das Linux-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0894b-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="0894b-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="0894b-119">-LocalPath</span></span>
<span data-ttu-id="0894b-120">Gibt den lokalen Pfad für die Start Diagnosedaten an.</span><span class="sxs-lookup"><span data-stu-id="0894b-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="0894b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0894b-121">-Name</span></span>
<span data-ttu-id="0894b-122">Gibt den Namen des virtuellen Computers an, für den dieses Cmdlet Diagnosedaten erhält.</span><span class="sxs-lookup"><span data-stu-id="0894b-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="0894b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0894b-123">-ResourceGroupName</span></span>
<span data-ttu-id="0894b-124">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="0894b-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0894b-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="0894b-125">-Windows</span></span>
<span data-ttu-id="0894b-126">Gibt an, dass auf dem virtuellen Computer das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0894b-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="0894b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0894b-127">CommonParameters</span></span>
<span data-ttu-id="0894b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0894b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0894b-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0894b-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0894b-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0894b-130">INPUTS</span></span>

### <span data-ttu-id="0894b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0894b-131">System.String</span></span>

## <span data-ttu-id="0894b-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0894b-132">OUTPUTS</span></span>

### <span data-ttu-id="0894b-133">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0894b-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="0894b-134">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="0894b-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="0894b-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="0894b-135">NOTES</span></span>

## <span data-ttu-id="0894b-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0894b-136">RELATED LINKS</span></span>

[<span data-ttu-id="0894b-137">Satz-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0894b-137">Set-AzVMBootDiagnostics</span></span>](./Set-AzVMBootDiagnostics.md)


