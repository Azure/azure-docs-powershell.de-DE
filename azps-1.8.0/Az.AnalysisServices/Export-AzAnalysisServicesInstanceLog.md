---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 04a1c63ac2ae1b0db692f2bef4b4803a8acb744f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650441"
---
# <span data-ttu-id="e7271-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="e7271-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="e7271-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7271-102">SYNOPSIS</span></span>
<span data-ttu-id="e7271-103">Exportiert ein Protokoll aus einer Instanz des Analysis Services-Servers in der aktuell angemeldeten Umgebung, wie in Add-AzAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="e7271-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="e7271-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7271-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7271-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7271-105">DESCRIPTION</span></span>
<span data-ttu-id="e7271-106">Das Export-AzAnalysisServicesInstance-Cmdlet exportiert das Protokoll aus einer Instanz von Azure Analysis Services-Server in eine Datei</span><span class="sxs-lookup"><span data-stu-id="e7271-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="e7271-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7271-107">EXAMPLES</span></span>

### <span data-ttu-id="e7271-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e7271-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="e7271-109">Mit diesem Befehl wird das Protokoll aus dem Server "Testserver" in der im Add-AzAnalysisServicesAccount-Befehl angegebenen Umgebung exportiert und in der in OutputPath "C:\path\to\log\testserver.log" angegebenen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e7271-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="e7271-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7271-110">PARAMETERS</span></span>

### <span data-ttu-id="e7271-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e7271-111">-Force</span></span>
<span data-ttu-id="e7271-112">Datei überschreiben, falls vorhanden, ohne zu Fragen</span><span class="sxs-lookup"><span data-stu-id="e7271-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="e7271-113">-Instanz</span><span class="sxs-lookup"><span data-stu-id="e7271-113">-Instance</span></span>
<span data-ttu-id="e7271-114">Name der Analysis Services-Serverinstanz</span><span class="sxs-lookup"><span data-stu-id="e7271-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="e7271-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="e7271-115">-OutputPath</span></span>
<span data-ttu-id="e7271-116">Ausgabepfad zur Datei zum Exportprotokoll</span><span class="sxs-lookup"><span data-stu-id="e7271-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="e7271-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7271-117">-PassThru</span></span>
<span data-ttu-id="e7271-118">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="e7271-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e7271-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7271-119">-Confirm</span></span>
<span data-ttu-id="e7271-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7271-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7271-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7271-121">-WhatIf</span></span>
<span data-ttu-id="e7271-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7271-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7271-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7271-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7271-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7271-124">CommonParameters</span></span>
<span data-ttu-id="e7271-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7271-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7271-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7271-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7271-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7271-127">INPUTS</span></span>

### <span data-ttu-id="e7271-128">Keine</span><span class="sxs-lookup"><span data-stu-id="e7271-128">None</span></span>

## <span data-ttu-id="e7271-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7271-129">OUTPUTS</span></span>

### <span data-ttu-id="e7271-130">System. void</span><span class="sxs-lookup"><span data-stu-id="e7271-130">System.Void</span></span>

## <span data-ttu-id="e7271-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7271-131">NOTES</span></span>
<span data-ttu-id="e7271-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="e7271-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="e7271-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7271-133">RELATED LINKS</span></span>
