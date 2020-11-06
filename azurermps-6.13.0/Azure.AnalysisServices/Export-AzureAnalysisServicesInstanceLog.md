---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: dad0e14b72c256706456ed3c923b966323fd7dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480706"
---
# <span data-ttu-id="a2b0e-101">Export-AzureAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="a2b0e-101">Export-AzureAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="a2b0e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b0e-103">Exportiert ein Protokoll aus einer Instanz des Analysis Services-Servers in der aktuell angemeldeten Umgebung, wie in Add-AzureAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2b0e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2b0e-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog -Instance <String> -OutputPath <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2b0e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2b0e-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b0e-106">Das Export-AzureAnalysisServicesInstance-Cmdlet exportiert das Protokoll aus einer Instanz von Azure Analysis Services-Server in eine Datei</span><span class="sxs-lookup"><span data-stu-id="a2b0e-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="a2b0e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2b0e-107">EXAMPLES</span></span>

### <span data-ttu-id="a2b0e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2b0e-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="a2b0e-109">Mit diesem Befehl wird das Protokoll aus dem Server "Testserver" in der im Add-AzureAnalysisServicesAccount-Befehl angegebenen Umgebung exportiert und in der in OutputPath "C:\path\to\log\testserver.log" angegebenen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="a2b0e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2b0e-110">PARAMETERS</span></span>

### <span data-ttu-id="a2b0e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a2b0e-111">-Force</span></span>
<span data-ttu-id="a2b0e-112">Datei überschreiben, falls vorhanden, ohne zu Fragen</span><span class="sxs-lookup"><span data-stu-id="a2b0e-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="a2b0e-113">-Instanz</span><span class="sxs-lookup"><span data-stu-id="a2b0e-113">-Instance</span></span>
<span data-ttu-id="a2b0e-114">Name der Analysis Services-Serverinstanz</span><span class="sxs-lookup"><span data-stu-id="a2b0e-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="a2b0e-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="a2b0e-115">-OutputPath</span></span>
<span data-ttu-id="a2b0e-116">Ausgabepfad zur Datei zum Exportprotokoll</span><span class="sxs-lookup"><span data-stu-id="a2b0e-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="a2b0e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2b0e-117">-Confirm</span></span>
<span data-ttu-id="a2b0e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b0e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b0e-119">-WhatIf</span></span>
<span data-ttu-id="a2b0e-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2b0e-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2b0e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b0e-122">CommonParameters</span></span>
<span data-ttu-id="a2b0e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b0e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2b0e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b0e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2b0e-125">INPUTS</span></span>

### <span data-ttu-id="a2b0e-126">Keine</span><span class="sxs-lookup"><span data-stu-id="a2b0e-126">None</span></span>

## <span data-ttu-id="a2b0e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2b0e-127">OUTPUTS</span></span>

### <span data-ttu-id="a2b0e-128">System. void</span><span class="sxs-lookup"><span data-stu-id="a2b0e-128">System.Void</span></span>

## <span data-ttu-id="a2b0e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2b0e-129">NOTES</span></span>
<span data-ttu-id="a2b0e-130">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="a2b0e-130">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="a2b0e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2b0e-131">RELATED LINKS</span></span>
