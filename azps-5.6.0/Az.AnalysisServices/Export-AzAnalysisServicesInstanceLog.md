---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 3e4e3b2c2f90420f198d2900d5de0d519ffde81a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950387"
---
# <span data-ttu-id="c07e0-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="c07e0-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="c07e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c07e0-102">SYNOPSIS</span></span>
<span data-ttu-id="c07e0-103">Exportiert ein Protokoll von einer Instanz des Analysis Services-Servers in der aktuell angemeldeten Umgebung, wie im Befehl Add-AzAnalysisServicesAccount angegeben</span><span class="sxs-lookup"><span data-stu-id="c07e0-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="c07e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c07e0-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c07e0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c07e0-105">DESCRIPTION</span></span>
<span data-ttu-id="c07e0-106">Das Export-AzAnalysisServicesInstance-Cmdlet exportiert das Protokoll von einer Instanz des Azure Analysis Services-Servers in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="c07e0-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="c07e0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c07e0-107">EXAMPLES</span></span>

### <span data-ttu-id="c07e0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c07e0-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="c07e0-109">Mit diesem Befehl wird das Protokoll vom Servertestserver in der im Befehl Add-AzAnalysisServicesAccount angegebenen Umgebung exportiert und in der datei gespeichert, die in OutputPath "C:\path\to\log\testserver.log" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c07e0-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="c07e0-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c07e0-110">PARAMETERS</span></span>

### <span data-ttu-id="c07e0-111">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="c07e0-111">-Force</span></span>
<span data-ttu-id="c07e0-112">Datei überschreiben, wenn vorhanden, ohne zu fragen</span><span class="sxs-lookup"><span data-stu-id="c07e0-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="c07e0-113">-Instanz</span><span class="sxs-lookup"><span data-stu-id="c07e0-113">-Instance</span></span>
<span data-ttu-id="c07e0-114">Name der Analysis Services-Serverinstanz</span><span class="sxs-lookup"><span data-stu-id="c07e0-114">Name of the Analysis Services server instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c07e0-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="c07e0-115">-OutputPath</span></span>
<span data-ttu-id="c07e0-116">Ausgabepfad zu Datei zum Exportieren des Protokolls</span><span class="sxs-lookup"><span data-stu-id="c07e0-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="c07e0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c07e0-117">-PassThru</span></span>
<span data-ttu-id="c07e0-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c07e0-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c07e0-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c07e0-119">-Confirm</span></span>
<span data-ttu-id="c07e0-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c07e0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c07e0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c07e0-121">-WhatIf</span></span>
<span data-ttu-id="c07e0-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c07e0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c07e0-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c07e0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c07e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07e0-124">CommonParameters</span></span>
<span data-ttu-id="c07e0-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c07e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07e0-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c07e0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07e0-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c07e0-127">INPUTS</span></span>

### <span data-ttu-id="c07e0-128">Keine</span><span class="sxs-lookup"><span data-stu-id="c07e0-128">None</span></span>

## <span data-ttu-id="c07e0-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c07e0-129">OUTPUTS</span></span>

### <span data-ttu-id="c07e0-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="c07e0-130">System.Void</span></span>

## <span data-ttu-id="c07e0-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c07e0-131">NOTES</span></span>
<span data-ttu-id="c07e0-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="c07e0-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="c07e0-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c07e0-133">RELATED LINKS</span></span>
