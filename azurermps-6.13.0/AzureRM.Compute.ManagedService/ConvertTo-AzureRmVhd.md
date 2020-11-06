---
external help file: AzureRM.Compute.ManagedService-help.xml
Module Name: AzureRM.Compute.ManagedService
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: 0fa0f2d5cb78fe96f05b818b5cbfdabca47cbdee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477910"
---
# <span data-ttu-id="f62e7-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="f62e7-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="f62e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f62e7-102">SYNOPSIS</span></span>
<span data-ttu-id="f62e7-103">Konvertieren von Hyper-V VM in Azure unterstützte virtuelle Festplatten-Dateien</span><span class="sxs-lookup"><span data-stu-id="f62e7-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f62e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f62e7-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f62e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f62e7-105">DESCRIPTION</span></span>
<span data-ttu-id="f62e7-106">Konvertieren von Hyper-V VM in Azure unterstützte virtuelle Festplatten-Dateien</span><span class="sxs-lookup"><span data-stu-id="f62e7-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="f62e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f62e7-107">EXAMPLES</span></span>

### <span data-ttu-id="f62e7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f62e7-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="f62e7-109">Konvertieren Sie die Hyper-V-VM mit dem Namen "Test" in Azure unterstützte virtuelle Festplatten-Dateien in den aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="f62e7-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="f62e7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f62e7-110">PARAMETERS</span></span>

### <span data-ttu-id="f62e7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f62e7-111">-AsJob</span></span>
<span data-ttu-id="f62e7-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="f62e7-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62e7-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="f62e7-113">-ExportPath</span></span>
<span data-ttu-id="f62e7-114">Der Exportordner Pfad, in dem die Datenträgerdateien enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f62e7-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62e7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f62e7-115">-Force</span></span>
<span data-ttu-id="f62e7-116">Erzwingen des Exports, auch wenn vorhandener Ordner gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="f62e7-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62e7-117">-Vserver</span><span class="sxs-lookup"><span data-stu-id="f62e7-117">-HyperVServer</span></span>
<span data-ttu-id="f62e7-118">Der Hyper-V-Server-DNS-Name mit "localhost" als Standardwert.</span><span class="sxs-lookup"><span data-stu-id="f62e7-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62e7-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="f62e7-119">-HyperVVMName</span></span>
<span data-ttu-id="f62e7-120">Der Name des Hyper-V-namens.</span><span class="sxs-lookup"><span data-stu-id="f62e7-120">The Hyper-V name name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62e7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f62e7-121">-Confirm</span></span>
<span data-ttu-id="f62e7-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f62e7-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62e7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f62e7-123">-WhatIf</span></span>
<span data-ttu-id="f62e7-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f62e7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f62e7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f62e7-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62e7-126">CommonParameters</span></span>
<span data-ttu-id="f62e7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f62e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62e7-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f62e7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62e7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f62e7-129">INPUTS</span></span>

### <span data-ttu-id="f62e7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f62e7-130">System.String</span></span>

## <span data-ttu-id="f62e7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f62e7-131">OUTPUTS</span></span>

### <span data-ttu-id="f62e7-132">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="f62e7-132">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="f62e7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f62e7-133">NOTES</span></span>

## <span data-ttu-id="f62e7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f62e7-134">RELATED LINKS</span></span>
