---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995887"
---
# <span data-ttu-id="c55e4-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="c55e4-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="c55e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c55e4-102">SYNOPSIS</span></span>
<span data-ttu-id="c55e4-103">Exportiert ein Protokoll aus einer Instanz des Analysis Services-Servers in der aktuell angemeldeten Umgebung, wie in Add-AzAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="c55e4-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="c55e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c55e4-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c55e4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c55e4-105">DESCRIPTION</span></span>
<span data-ttu-id="c55e4-106">Das Export-AzAnalysisServicesInstance-Cmdlet exportiert das Protokoll aus einer Instanz von Azure Analysis Services-Server in eine Datei</span><span class="sxs-lookup"><span data-stu-id="c55e4-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="c55e4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c55e4-107">EXAMPLES</span></span>

### <span data-ttu-id="c55e4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c55e4-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="c55e4-109">Mit diesem Befehl wird das Protokoll aus dem Server "Testserver" in der im Add-AzAnalysisServicesAccount-Befehl angegebenen Umgebung exportiert und in der in OutputPath "C:\path\to\log\testserver.log" angegebenen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c55e4-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="c55e4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c55e4-110">PARAMETERS</span></span>

### <span data-ttu-id="c55e4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c55e4-111">-Force</span></span>
<span data-ttu-id="c55e4-112">Datei überschreiben, falls vorhanden, ohne zu Fragen</span><span class="sxs-lookup"><span data-stu-id="c55e4-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="c55e4-113">-Instanz</span><span class="sxs-lookup"><span data-stu-id="c55e4-113">-Instance</span></span>
<span data-ttu-id="c55e4-114">Name der Analysis Services-Serverinstanz</span><span class="sxs-lookup"><span data-stu-id="c55e4-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="c55e4-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="c55e4-115">-OutputPath</span></span>
<span data-ttu-id="c55e4-116">Ausgabepfad zur Datei zum Exportprotokoll</span><span class="sxs-lookup"><span data-stu-id="c55e4-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="c55e4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c55e4-117">-PassThru</span></span>
<span data-ttu-id="c55e4-118">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="c55e4-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c55e4-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c55e4-119">-Confirm</span></span>
<span data-ttu-id="c55e4-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c55e4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c55e4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c55e4-121">-WhatIf</span></span>
<span data-ttu-id="c55e4-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c55e4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c55e4-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c55e4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c55e4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c55e4-124">CommonParameters</span></span>
<span data-ttu-id="c55e4-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c55e4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c55e4-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c55e4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c55e4-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c55e4-127">INPUTS</span></span>

### <span data-ttu-id="c55e4-128">Keine</span><span class="sxs-lookup"><span data-stu-id="c55e4-128">None</span></span>

## <span data-ttu-id="c55e4-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c55e4-129">OUTPUTS</span></span>

### <span data-ttu-id="c55e4-130">System. void</span><span class="sxs-lookup"><span data-stu-id="c55e4-130">System.Void</span></span>

## <span data-ttu-id="c55e4-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c55e4-131">NOTES</span></span>
<span data-ttu-id="c55e4-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="c55e4-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="c55e4-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c55e4-133">RELATED LINKS</span></span>
