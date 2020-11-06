---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 0a89ee592e6f6f6d4d9e56df6d7e4df32b010524
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496693"
---
# <span data-ttu-id="77a45-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="77a45-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="77a45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77a45-102">SYNOPSIS</span></span>
<span data-ttu-id="77a45-103">Startet eine Instanz des Analysis Services-Servers in der aktuell angemeldeten Umgebung neu, wie in Add-AzureAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="77a45-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77a45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77a45-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="77a45-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77a45-105">DESCRIPTION</span></span>
<span data-ttu-id="77a45-106">Das Restart-AzureAnalysisServicesInstance-Cmdlet startet eine Instanz des Azure Analysis Services-Servers neu</span><span class="sxs-lookup"><span data-stu-id="77a45-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="77a45-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77a45-107">EXAMPLES</span></span>

### <span data-ttu-id="77a45-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="77a45-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="77a45-109">Mit diesem Befehl wird der Server "Testserver" in der im Add-AzureAnalysisServicesAccount-Befehl angegebenen Umgebung neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="77a45-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="77a45-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="77a45-110">PARAMETERS</span></span>

### <span data-ttu-id="77a45-111">-Instanz</span><span class="sxs-lookup"><span data-stu-id="77a45-111">-Instance</span></span>
<span data-ttu-id="77a45-112">Name der Analysis Services-Serverinstanz, die neu gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="77a45-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="77a45-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77a45-113">-PassThru</span></span>
<span data-ttu-id="77a45-114">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="77a45-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="77a45-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77a45-115">-Confirm</span></span>
<span data-ttu-id="77a45-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77a45-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a45-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77a45-117">-WhatIf</span></span>
<span data-ttu-id="77a45-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77a45-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77a45-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77a45-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="77a45-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77a45-120">INPUTS</span></span>

### <span data-ttu-id="77a45-121">Keine</span><span class="sxs-lookup"><span data-stu-id="77a45-121">None</span></span>
<span data-ttu-id="77a45-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="77a45-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77a45-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77a45-123">OUTPUTS</span></span>

### <span data-ttu-id="77a45-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77a45-124">System.Boolean</span></span>

## <span data-ttu-id="77a45-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="77a45-125">NOTES</span></span>
<span data-ttu-id="77a45-126">Alias: Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="77a45-126">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="77a45-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77a45-127">RELATED LINKS</span></span>

