---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149633"
---
# <span data-ttu-id="49048-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="49048-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="49048-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49048-102">SYNOPSIS</span></span>
<span data-ttu-id="49048-103">Startet eine Instanz des Analysis Services-Servers in der aktuell in der Umgebung protokollierten Umgebung neu, wie im Add-AzAnalysisServicesAccount angegeben.</span><span class="sxs-lookup"><span data-stu-id="49048-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="49048-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49048-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49048-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49048-105">DESCRIPTION</span></span>
<span data-ttu-id="49048-106">Das Restart-AzAnalysisServicesInstance cmdlet startet eine Instanz des Azure Analysis Services-Servers neu.</span><span class="sxs-lookup"><span data-stu-id="49048-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="49048-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49048-107">EXAMPLES</span></span>

### <span data-ttu-id="49048-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="49048-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="49048-109">Mit diesem Befehl wird der Servertestserver in der im Befehl "Testserver" angegebenen Add-AzAnalysisServicesAccount neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="49048-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="49048-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49048-110">PARAMETERS</span></span>

### <span data-ttu-id="49048-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="49048-111">-Instance</span></span>
<span data-ttu-id="49048-112">Name der analysis services-Serverinstanz, die neu gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="49048-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="49048-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49048-113">-PassThru</span></span>
<span data-ttu-id="49048-114">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="49048-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="49048-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49048-115">-Confirm</span></span>
<span data-ttu-id="49048-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49048-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49048-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="49048-117">-WhatIf</span></span>
<span data-ttu-id="49048-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49048-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49048-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49048-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49048-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49048-120">CommonParameters</span></span>
<span data-ttu-id="49048-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49048-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49048-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49048-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49048-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49048-123">INPUTS</span></span>

### <span data-ttu-id="49048-124">Keine</span><span class="sxs-lookup"><span data-stu-id="49048-124">None</span></span>

## <span data-ttu-id="49048-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49048-125">OUTPUTS</span></span>

### <span data-ttu-id="49048-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49048-126">System.Boolean</span></span>

## <span data-ttu-id="49048-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="49048-127">NOTES</span></span>
<span data-ttu-id="49048-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="49048-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="49048-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="49048-129">RELATED LINKS</span></span>
