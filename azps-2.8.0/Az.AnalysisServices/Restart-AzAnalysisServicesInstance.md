---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 623b7c84b29e5e64a47beeff6c9f7dba88edf32b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658367"
---
# <span data-ttu-id="a3235-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="a3235-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="a3235-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3235-102">SYNOPSIS</span></span>
<span data-ttu-id="a3235-103">Startet eine Instanz des Analysis Services-Servers in der aktuell angemeldeten Umgebung neu, wie in Add-AzAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="a3235-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="a3235-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3235-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3235-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3235-105">DESCRIPTION</span></span>
<span data-ttu-id="a3235-106">Das Restart-AzAnalysisServicesInstance-Cmdlet startet eine Instanz des Azure Analysis Services-Servers neu</span><span class="sxs-lookup"><span data-stu-id="a3235-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="a3235-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3235-107">EXAMPLES</span></span>

### <span data-ttu-id="a3235-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3235-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="a3235-109">Mit diesem Befehl wird der Server "Testserver" in der im Add-AzAnalysisServicesAccount-Befehl angegebenen Umgebung neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="a3235-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="a3235-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3235-110">PARAMETERS</span></span>

### <span data-ttu-id="a3235-111">-Instanz</span><span class="sxs-lookup"><span data-stu-id="a3235-111">-Instance</span></span>
<span data-ttu-id="a3235-112">Name der Analysis Services-Serverinstanz, die neu gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="a3235-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="a3235-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3235-113">-PassThru</span></span>
<span data-ttu-id="a3235-114">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a3235-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a3235-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3235-115">-Confirm</span></span>
<span data-ttu-id="a3235-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3235-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3235-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3235-117">-WhatIf</span></span>
<span data-ttu-id="a3235-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3235-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3235-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3235-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3235-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3235-120">CommonParameters</span></span>
<span data-ttu-id="a3235-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3235-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3235-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3235-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3235-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3235-123">INPUTS</span></span>

### <span data-ttu-id="a3235-124">Keine</span><span class="sxs-lookup"><span data-stu-id="a3235-124">None</span></span>

## <span data-ttu-id="a3235-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3235-125">OUTPUTS</span></span>

### <span data-ttu-id="a3235-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3235-126">System.Boolean</span></span>

## <span data-ttu-id="a3235-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3235-127">NOTES</span></span>
<span data-ttu-id="a3235-128">Alias: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="a3235-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="a3235-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3235-129">RELATED LINKS</span></span>
