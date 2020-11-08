---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996747"
---
# <span data-ttu-id="5d2f2-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="5d2f2-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="5d2f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d2f2-102">SYNOPSIS</span></span>
<span data-ttu-id="5d2f2-103">Startet eine Instanz des Analysis Services-Servers in der aktuell angemeldeten Umgebung neu, wie in Add-AzAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="5d2f2-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="5d2f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d2f2-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d2f2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d2f2-105">DESCRIPTION</span></span>
<span data-ttu-id="5d2f2-106">Das Restart-AzAnalysisServicesInstance-Cmdlet startet eine Instanz des Azure Analysis Services-Servers neu</span><span class="sxs-lookup"><span data-stu-id="5d2f2-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="5d2f2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d2f2-107">EXAMPLES</span></span>

### <span data-ttu-id="5d2f2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d2f2-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="5d2f2-109">Mit diesem Befehl wird der Server "Testserver" in der im Add-AzAnalysisServicesAccount-Befehl angegebenen Umgebung neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="5d2f2-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="5d2f2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d2f2-110">PARAMETERS</span></span>

### <span data-ttu-id="5d2f2-111">-Instanz</span><span class="sxs-lookup"><span data-stu-id="5d2f2-111">-Instance</span></span>
<span data-ttu-id="5d2f2-112">Name der Analysis Services-Serverinstanz, die neu gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="5d2f2-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="5d2f2-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d2f2-113">-PassThru</span></span>
<span data-ttu-id="5d2f2-114">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5d2f2-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5d2f2-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d2f2-115">-Confirm</span></span>
<span data-ttu-id="5d2f2-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d2f2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d2f2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d2f2-117">-WhatIf</span></span>
<span data-ttu-id="5d2f2-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d2f2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d2f2-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d2f2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d2f2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d2f2-120">CommonParameters</span></span>
<span data-ttu-id="5d2f2-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d2f2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d2f2-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d2f2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d2f2-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d2f2-123">INPUTS</span></span>

### <span data-ttu-id="5d2f2-124">Keine</span><span class="sxs-lookup"><span data-stu-id="5d2f2-124">None</span></span>

## <span data-ttu-id="5d2f2-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d2f2-125">OUTPUTS</span></span>

### <span data-ttu-id="5d2f2-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d2f2-126">System.Boolean</span></span>

## <span data-ttu-id="5d2f2-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d2f2-127">NOTES</span></span>
<span data-ttu-id="5d2f2-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="5d2f2-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="5d2f2-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d2f2-129">RELATED LINKS</span></span>
