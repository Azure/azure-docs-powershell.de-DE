---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 2c7162f5a93c112a3f67b308941b56b698792fa3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658353"
---
# <span data-ttu-id="43da4-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="43da4-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="43da4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43da4-102">SYNOPSIS</span></span>

<span data-ttu-id="43da4-103">Synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrage dezentralen Instanzen in der aktuell angemeldeten Umgebung, wie in Add-AzAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="43da4-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="43da4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43da4-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43da4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43da4-105">DESCRIPTION</span></span>

<span data-ttu-id="43da4-106">Das Sync-AzAnalysisServicesInstance-Cmdlet synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrage-dezentralen Instanzen in der aktuell angemeldeten Umgebung, wie in Add-AzAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="43da4-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="43da4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43da4-107">EXAMPLES</span></span>

### <span data-ttu-id="43da4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43da4-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="43da4-109">Mit diesem Befehl wird die Datenbank mit dem Namen "SalesOrders" auf dem Server "Contoso" im Umgebungs westus.asazure.Windows.net synchronisiert, vorausgesetzt, der Benutzer hat sich mit Add-AzAnalysisServicesAccount Befehl bei dieser Umgebung angemeldet.</span><span class="sxs-lookup"><span data-stu-id="43da4-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="43da4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="43da4-110">PARAMETERS</span></span>

### <span data-ttu-id="43da4-111">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="43da4-111">-Database</span></span>

<span data-ttu-id="43da4-112">Identität der zu synchronisierenden Datenbank</span><span class="sxs-lookup"><span data-stu-id="43da4-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="43da4-113">-Instanz</span><span class="sxs-lookup"><span data-stu-id="43da4-113">-Instance</span></span>

<span data-ttu-id="43da4-114">Name der Analysis Services-Serverinstanz, die neu gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="43da4-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="43da4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43da4-115">-PassThru</span></span>

<span data-ttu-id="43da4-116">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="43da4-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="43da4-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43da4-117">-Confirm</span></span>
<span data-ttu-id="43da4-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43da4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43da4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43da4-119">-WhatIf</span></span>
<span data-ttu-id="43da4-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43da4-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43da4-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43da4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43da4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43da4-122">CommonParameters</span></span>
<span data-ttu-id="43da4-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43da4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43da4-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43da4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43da4-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43da4-125">INPUTS</span></span>

### <span data-ttu-id="43da4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="43da4-126">System.String</span></span>

## <span data-ttu-id="43da4-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43da4-127">OUTPUTS</span></span>

### <span data-ttu-id="43da4-128">Microsoft. Azure. Commands. AnalysisServices. dataplane. Models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="43da4-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="43da4-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="43da4-129">NOTES</span></span>

<span data-ttu-id="43da4-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="43da4-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="43da4-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43da4-131">RELATED LINKS</span></span>
