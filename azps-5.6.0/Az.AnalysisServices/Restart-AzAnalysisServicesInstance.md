---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: b0bb5d90fe304d2663671fdc8a2277d2adb18322
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930595"
---
# <span data-ttu-id="361a1-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="361a1-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="361a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="361a1-102">SYNOPSIS</span></span>
<span data-ttu-id="361a1-103">Startet eine Instanz des Analysis Services-Servers in der aktuell angemeldeten Umgebung neu, wie im Befehl Add-AzAnalysisServicesAccount angegeben</span><span class="sxs-lookup"><span data-stu-id="361a1-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="361a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="361a1-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="361a1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="361a1-105">DESCRIPTION</span></span>
<span data-ttu-id="361a1-106">Das Restart-AzAnalysisServicesInstance cmdlet startet eine Instanz des Azure Analysis Services-Servers neu.</span><span class="sxs-lookup"><span data-stu-id="361a1-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="361a1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="361a1-107">EXAMPLES</span></span>

### <span data-ttu-id="361a1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="361a1-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="361a1-109">Mit diesem Befehl wird der Servertestserver in der im Befehl "Add-AzAnalysisServicesAccount" angegebenen Umgebung neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="361a1-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="361a1-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="361a1-110">PARAMETERS</span></span>

### <span data-ttu-id="361a1-111">-Instanz</span><span class="sxs-lookup"><span data-stu-id="361a1-111">-Instance</span></span>
<span data-ttu-id="361a1-112">Name der Analysis Services-Serverinstanz, die neu gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="361a1-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="361a1-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="361a1-113">-PassThru</span></span>
<span data-ttu-id="361a1-114">Wenn der Befehl erfolgreich war, gibt die Angabe "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="361a1-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="361a1-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="361a1-115">-Confirm</span></span>
<span data-ttu-id="361a1-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="361a1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="361a1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="361a1-117">-WhatIf</span></span>
<span data-ttu-id="361a1-118">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="361a1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="361a1-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="361a1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="361a1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="361a1-120">CommonParameters</span></span>
<span data-ttu-id="361a1-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="361a1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="361a1-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="361a1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="361a1-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="361a1-123">INPUTS</span></span>

### <span data-ttu-id="361a1-124">Keine</span><span class="sxs-lookup"><span data-stu-id="361a1-124">None</span></span>

## <span data-ttu-id="361a1-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="361a1-125">OUTPUTS</span></span>

### <span data-ttu-id="361a1-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="361a1-126">System.Boolean</span></span>

## <span data-ttu-id="361a1-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="361a1-127">NOTES</span></span>
<span data-ttu-id="361a1-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="361a1-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="361a1-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="361a1-129">RELATED LINKS</span></span>
