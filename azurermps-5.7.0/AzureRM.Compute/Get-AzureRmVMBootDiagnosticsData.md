---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: 5ae237c21c78f206188f23153bdf35c6bea10b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662592"
---
# <span data-ttu-id="ad521-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ad521-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="ad521-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad521-102">SYNOPSIS</span></span>
<span data-ttu-id="ad521-103">Ruft Start Diagnosedaten für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="ad521-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad521-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad521-104">SYNTAX</span></span>

### <span data-ttu-id="ad521-105">WindowsParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad521-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [<CommonParameters>]
```

### <span data-ttu-id="ad521-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="ad521-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [<CommonParameters>]
```

## <span data-ttu-id="ad521-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad521-107">DESCRIPTION</span></span>
<span data-ttu-id="ad521-108">Das Cmdlet " **Get-AzureRmVMBootDiagnosticsData** " ruft Start Diagnosedaten für einen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="ad521-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="ad521-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad521-109">EXAMPLES</span></span>

### <span data-ttu-id="ad521-110">Beispiel 1: Abrufen von Start Diagnosedaten</span><span class="sxs-lookup"><span data-stu-id="ad521-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="ad521-111">Dieser Befehl ruft Start Diagnosedaten für den virtuellen Computer mit dem Namen ContosoVM07 ab.</span><span class="sxs-lookup"><span data-stu-id="ad521-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="ad521-112">Auf diesem virtuellen Computer wird das Betriebssystem Windows ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad521-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="ad521-113">Der Befehl speichert die Daten im angegebenen lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="ad521-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="ad521-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad521-114">PARAMETERS</span></span>

### <span data-ttu-id="ad521-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="ad521-115">-Linux</span></span>
<span data-ttu-id="ad521-116">Gibt an, dass auf dem virtuellen Computer das Linux-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad521-116">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="ad521-117">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="ad521-117">-LocalPath</span></span>
<span data-ttu-id="ad521-118">Gibt den lokalen Pfad für die Start Diagnosedaten an.</span><span class="sxs-lookup"><span data-stu-id="ad521-118">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="ad521-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ad521-119">-Name</span></span>
<span data-ttu-id="ad521-120">Gibt den Namen des virtuellen Computers an, für den dieses Cmdlet Diagnosedaten erhält.</span><span class="sxs-lookup"><span data-stu-id="ad521-120">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="ad521-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad521-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad521-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="ad521-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ad521-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="ad521-123">-Windows</span></span>
<span data-ttu-id="ad521-124">Gibt an, dass auf dem virtuellen Computer das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad521-124">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="ad521-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad521-125">CommonParameters</span></span>
<span data-ttu-id="ad521-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad521-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad521-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad521-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad521-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad521-128">INPUTS</span></span>

### <span data-ttu-id="ad521-129">Keine</span><span class="sxs-lookup"><span data-stu-id="ad521-129">None</span></span>
<span data-ttu-id="ad521-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ad521-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad521-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad521-131">OUTPUTS</span></span>

## <span data-ttu-id="ad521-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad521-132">NOTES</span></span>

## <span data-ttu-id="ad521-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad521-133">RELATED LINKS</span></span>

[<span data-ttu-id="ad521-134">Satz-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ad521-134">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


