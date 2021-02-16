---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149612"
---
# <span data-ttu-id="68796-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="68796-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="68796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68796-102">SYNOPSIS</span></span>

<span data-ttu-id="68796-103">Synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrageskaloutinstanzen in der aktuell in der Umgebung protokollierten Umgebung, wie im Befehl "Add-AzAnalysisServicesAccount" angegeben.</span><span class="sxs-lookup"><span data-stu-id="68796-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="68796-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68796-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68796-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68796-105">DESCRIPTION</span></span>

<span data-ttu-id="68796-106">Das Sync-AzAnalysisServicesInstance Cmdlet synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrageskaloutinstanzen in der aktuell in der Umgebung protokollierten Umgebung, wie im Befehl "Add-AzAnalysisServicesAccount" angegeben.</span><span class="sxs-lookup"><span data-stu-id="68796-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="68796-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="68796-107">EXAMPLES</span></span>

### <span data-ttu-id="68796-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="68796-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="68796-109">Mit diesem Befehl wird die Datenbank mit dem Namen "SalesOrders" im Server "contoso" in der Umgebung synchronisiert westus.asazure.windows.net vorausgesetzt, der Benutzer hat sich mit dem Befehl "Add-AzAnalysisServicesAccount" bei dieser Umgebung angemeldet.</span><span class="sxs-lookup"><span data-stu-id="68796-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="68796-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68796-110">PARAMETERS</span></span>

### <span data-ttu-id="68796-111">-Database</span><span class="sxs-lookup"><span data-stu-id="68796-111">-Database</span></span>

<span data-ttu-id="68796-112">Identität der datenbank, die synchronisiert werden soll</span><span class="sxs-lookup"><span data-stu-id="68796-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="68796-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="68796-113">-Instance</span></span>

<span data-ttu-id="68796-114">Name der analysis services-Serverinstanz, die neu gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="68796-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="68796-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68796-115">-PassThru</span></span>

<span data-ttu-id="68796-116">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="68796-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="68796-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68796-117">-Confirm</span></span>
<span data-ttu-id="68796-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68796-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68796-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="68796-119">-WhatIf</span></span>
<span data-ttu-id="68796-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68796-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68796-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68796-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68796-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68796-122">CommonParameters</span></span>
<span data-ttu-id="68796-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68796-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68796-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68796-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68796-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="68796-125">INPUTS</span></span>

### <span data-ttu-id="68796-126">System.String</span><span class="sxs-lookup"><span data-stu-id="68796-126">System.String</span></span>

## <span data-ttu-id="68796-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="68796-127">OUTPUTS</span></span>

### <span data-ttu-id="68796-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="68796-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="68796-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="68796-129">NOTES</span></span>

<span data-ttu-id="68796-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="68796-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="68796-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="68796-131">RELATED LINKS</span></span>
