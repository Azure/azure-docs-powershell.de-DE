---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: c5ffd95cb3bd5e902e2e9edadfa9c96dd441c744
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922227"
---
# <span data-ttu-id="8ba6f-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="8ba6f-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="8ba6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ba6f-102">SYNOPSIS</span></span>

<span data-ttu-id="8ba6f-103">Synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrageskaloutinstanzen in der aktuell angemeldeten Umgebung, wie im Befehl Add-AzAnalysisServicesAccount angegeben</span><span class="sxs-lookup"><span data-stu-id="8ba6f-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8ba6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ba6f-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ba6f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ba6f-105">DESCRIPTION</span></span>

<span data-ttu-id="8ba6f-106">Das Sync-AzAnalysisServicesInstance-Cmdlet synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrageskaloutinstanzen in der aktuell angemeldeten Umgebung, wie im Befehl Add-AzAnalysisServicesAccount angegeben</span><span class="sxs-lookup"><span data-stu-id="8ba6f-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8ba6f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8ba6f-107">EXAMPLES</span></span>

### <span data-ttu-id="8ba6f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8ba6f-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="8ba6f-109">Mit diesem Befehl wird die Datenbank mit dem Namen "SalesOrders" auf dem Server namens "contoso" in der Umgebung synchronisiert westus.asazure.windows.net vorausgesetzt, der Benutzer hat sich mit dem Befehl "Add-AzAnalysisServicesAccount" bei dieser Umgebung angemeldet.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="8ba6f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8ba6f-110">PARAMETERS</span></span>

### <span data-ttu-id="8ba6f-111">-Database</span><span class="sxs-lookup"><span data-stu-id="8ba6f-111">-Database</span></span>

<span data-ttu-id="8ba6f-112">Identität der zu synchronisierende Datenbank</span><span class="sxs-lookup"><span data-stu-id="8ba6f-112">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba6f-113">-Instanz</span><span class="sxs-lookup"><span data-stu-id="8ba6f-113">-Instance</span></span>

<span data-ttu-id="8ba6f-114">Name der Analysis Services-Serverinstanz, die neu gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="8ba6f-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="8ba6f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ba6f-115">-PassThru</span></span>

<span data-ttu-id="8ba6f-116">Wenn der Befehl erfolgreich war, gibt die Angabe "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8ba6f-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ba6f-117">-Confirm</span></span>
<span data-ttu-id="8ba6f-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ba6f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba6f-119">-WhatIf</span></span>
<span data-ttu-id="8ba6f-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ba6f-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ba6f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba6f-122">CommonParameters</span></span>
<span data-ttu-id="8ba6f-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba6f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba6f-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba6f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba6f-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8ba6f-125">INPUTS</span></span>

### <span data-ttu-id="8ba6f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8ba6f-126">System.String</span></span>

## <span data-ttu-id="8ba6f-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8ba6f-127">OUTPUTS</span></span>

### <span data-ttu-id="8ba6f-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="8ba6f-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="8ba6f-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8ba6f-129">NOTES</span></span>

<span data-ttu-id="8ba6f-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="8ba6f-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="8ba6f-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8ba6f-131">RELATED LINKS</span></span>
