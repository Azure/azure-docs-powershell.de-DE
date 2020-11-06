---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: e93e38ef2914635cab61bf225c0d905d011ae643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479818"
---
# <span data-ttu-id="9ac38-101">Export-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="9ac38-101">Export-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="9ac38-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ac38-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac38-103">Exportiert ein Protokoll aus einer Instanz des Analysis Services-Servers in der aktuell angemeldeten Umgebung, wie in Add-AzureAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="9ac38-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ac38-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ac38-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## <span data-ttu-id="9ac38-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ac38-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac38-106">Das Export-AzureAnalysisServicesInstance-Cmdlet exportiert das Protokoll aus einer Instanz von Azure Analysis Services-Server in eine Datei</span><span class="sxs-lookup"><span data-stu-id="9ac38-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="9ac38-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ac38-107">EXAMPLES</span></span>

### <span data-ttu-id="9ac38-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ac38-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="9ac38-109">Mit diesem Befehl wird das Protokoll aus dem Server "Testserver" in der im Add-AzureAnalysisServicesAccount-Befehl angegebenen Umgebung exportiert und in der in OutputPath "C:\path\to\log\testserver.log" angegebenen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9ac38-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="9ac38-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ac38-110">PARAMETERS</span></span>

### <span data-ttu-id="9ac38-111">-Instanz</span><span class="sxs-lookup"><span data-stu-id="9ac38-111">-Instance</span></span>
<span data-ttu-id="9ac38-112">Name der Analysis Services-Serverinstanz</span><span class="sxs-lookup"><span data-stu-id="9ac38-112">Name of the Analysis Services server instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ac38-113">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="9ac38-113">-OutputPath</span></span>
<span data-ttu-id="9ac38-114">Ausgabepfad zur Datei zum Exportprotokoll</span><span class="sxs-lookup"><span data-stu-id="9ac38-114">Output path to file to export log</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ac38-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9ac38-115">-Force</span></span>
<span data-ttu-id="9ac38-116">Datei überschreiben, falls vorhanden, ohne zu Fragen</span><span class="sxs-lookup"><span data-stu-id="9ac38-116">Overwrite file if exists without asking</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="9ac38-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ac38-117">INPUTS</span></span>

### <span data-ttu-id="9ac38-118">Keine</span><span class="sxs-lookup"><span data-stu-id="9ac38-118">None</span></span>
<span data-ttu-id="9ac38-119">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9ac38-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ac38-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ac38-120">OUTPUTS</span></span>

## <span data-ttu-id="9ac38-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ac38-121">NOTES</span></span>
<span data-ttu-id="9ac38-122">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="9ac38-122">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="9ac38-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ac38-123">RELATED LINKS</span></span>

