---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303235"
---
# <span data-ttu-id="d41f9-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="d41f9-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="d41f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d41f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d41f9-103">Exportiert ein Protokoll aus einer Instanz des Analysis Services-Servers in der aktuell in der Umgebung angemeldeten Umgebung, wie im Befehl Add-AzAnalysisServicesAccount angegeben.</span><span class="sxs-lookup"><span data-stu-id="d41f9-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="d41f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d41f9-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d41f9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d41f9-105">DESCRIPTION</span></span>
<span data-ttu-id="d41f9-106">Das Export-AzAnalysisServicesInstance exportiert das Protokoll aus einer Instanz des Azure Analysis Services-Servers in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="d41f9-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="d41f9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d41f9-107">EXAMPLES</span></span>

### <span data-ttu-id="d41f9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d41f9-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="d41f9-109">Mit diesem Befehl wird das Protokoll vom Server "testserver" in der im Befehl Add-AzAnalysisServicesAccount angegebenen Umgebung exportiert und in der in OutputPath "C:\path\to\log\testserver.log" angegebenen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d41f9-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="d41f9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d41f9-110">PARAMETERS</span></span>

### <span data-ttu-id="d41f9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d41f9-111">-Force</span></span>
<span data-ttu-id="d41f9-112">Datei überschreiben, wenn sie vorhanden ist, ohne sie zu fragen</span><span class="sxs-lookup"><span data-stu-id="d41f9-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="d41f9-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="d41f9-113">-Instance</span></span>
<span data-ttu-id="d41f9-114">Name der Analysis Services-Serverinstanz</span><span class="sxs-lookup"><span data-stu-id="d41f9-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="d41f9-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="d41f9-115">-OutputPath</span></span>
<span data-ttu-id="d41f9-116">Ausgabepfad der zu exportierende Datei</span><span class="sxs-lookup"><span data-stu-id="d41f9-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="d41f9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d41f9-117">-PassThru</span></span>
<span data-ttu-id="d41f9-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d41f9-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d41f9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d41f9-119">-Confirm</span></span>
<span data-ttu-id="d41f9-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d41f9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d41f9-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d41f9-121">-WhatIf</span></span>
<span data-ttu-id="d41f9-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d41f9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d41f9-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d41f9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d41f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d41f9-124">CommonParameters</span></span>
<span data-ttu-id="d41f9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d41f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d41f9-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d41f9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d41f9-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d41f9-127">INPUTS</span></span>

### <span data-ttu-id="d41f9-128">Keine</span><span class="sxs-lookup"><span data-stu-id="d41f9-128">None</span></span>

## <span data-ttu-id="d41f9-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d41f9-129">OUTPUTS</span></span>

### <span data-ttu-id="d41f9-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="d41f9-130">System.Void</span></span>

## <span data-ttu-id="d41f9-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d41f9-131">NOTES</span></span>
<span data-ttu-id="d41f9-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="d41f9-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="d41f9-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d41f9-133">RELATED LINKS</span></span>
