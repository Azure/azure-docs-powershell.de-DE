---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmbootdiagnosticsdata
schema: 2.0.0
ms.openlocfilehash: 867f2c14e90eddd9649e0720d41f56aa896c61ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848895"
---
# <span data-ttu-id="9ef23-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="9ef23-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="9ef23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ef23-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef23-103">Ruft Start Diagnosedaten für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="9ef23-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ef23-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ef23-104">SYNTAX</span></span>

### <span data-ttu-id="9ef23-105">WindowsParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ef23-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ef23-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="9ef23-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ef23-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ef23-107">DESCRIPTION</span></span>
<span data-ttu-id="9ef23-108">Das Cmdlet " **Get-AzureRmVMBootDiagnosticsData** " ruft Start Diagnosedaten für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="9ef23-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="9ef23-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ef23-109">EXAMPLES</span></span>

### <span data-ttu-id="9ef23-110">Beispiel 1: Abrufen von Start Diagnosedaten</span><span class="sxs-lookup"><span data-stu-id="9ef23-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="9ef23-111">Dieser Befehl ruft Start Diagnosedaten für den virtuellen Computer mit dem Namen ContosoVM07 ab.</span><span class="sxs-lookup"><span data-stu-id="9ef23-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="9ef23-112">Auf diesem virtuellen Computer wird das Betriebssystem Windows ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ef23-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="9ef23-113">Der Befehl speichert die Daten im angegebenen lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="9ef23-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="9ef23-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ef23-114">PARAMETERS</span></span>

### <span data-ttu-id="9ef23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef23-115">-DefaultProfile</span></span>
<span data-ttu-id="9ef23-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ef23-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ef23-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="9ef23-117">-Linux</span></span>
<span data-ttu-id="9ef23-118">Gibt an, dass auf dem virtuellen Computer das Linux-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ef23-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef23-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="9ef23-119">-LocalPath</span></span>
<span data-ttu-id="9ef23-120">Gibt den lokalen Pfad für die Start Diagnosedaten an.</span><span class="sxs-lookup"><span data-stu-id="9ef23-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef23-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9ef23-121">-Name</span></span>
<span data-ttu-id="9ef23-122">Gibt den Namen des virtuellen Computers an, für den dieses Cmdlet Diagnosedaten erhält.</span><span class="sxs-lookup"><span data-stu-id="9ef23-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef23-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef23-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ef23-124">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="9ef23-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9ef23-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="9ef23-125">-Windows</span></span>
<span data-ttu-id="9ef23-126">Gibt an, dass auf dem virtuellen Computer das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ef23-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef23-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef23-127">CommonParameters</span></span>
<span data-ttu-id="9ef23-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ef23-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef23-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ef23-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef23-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ef23-130">INPUTS</span></span>

### <span data-ttu-id="9ef23-131">Keine</span><span class="sxs-lookup"><span data-stu-id="9ef23-131">None</span></span>
<span data-ttu-id="9ef23-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9ef23-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ef23-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ef23-133">OUTPUTS</span></span>

### <span data-ttu-id="9ef23-134">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9ef23-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="9ef23-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="9ef23-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="9ef23-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ef23-136">NOTES</span></span>

## <span data-ttu-id="9ef23-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ef23-137">RELATED LINKS</span></span>

[<span data-ttu-id="9ef23-138">Satz-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9ef23-138">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


