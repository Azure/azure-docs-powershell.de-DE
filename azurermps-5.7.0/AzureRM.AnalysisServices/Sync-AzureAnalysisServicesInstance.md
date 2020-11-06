---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479810"
---
# <span data-ttu-id="5e568-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="5e568-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="5e568-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e568-102">SYNOPSIS</span></span>

<span data-ttu-id="5e568-103">Synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrage dezentralen Instanzen in der aktuell angemeldeten Umgebung, wie in Add-AzureAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="5e568-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e568-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e568-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## <span data-ttu-id="5e568-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e568-105">DESCRIPTION</span></span>

<span data-ttu-id="5e568-106">Das Sync-AzureAnalysisServicesInstance-Cmdlet synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrage-dezentralen Instanzen in der aktuell angemeldeten Umgebung, wie in Add-AzureAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="5e568-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="5e568-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e568-107">EXAMPLES</span></span>

### <span data-ttu-id="5e568-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e568-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="5e568-109">Dieser Befehl synchronisiert die Datenbank mit dem Namen "SalesOrders" auf dem Server "Contoso" im Umgebungs westus.asazure.Windows.net, vorausgesetzt, der Benutzer hat sich mit Add-AzureAnalysisServicesAccount Befehl bei dieser Umgebung angemeldet.</span><span class="sxs-lookup"><span data-stu-id="5e568-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="5e568-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e568-110">PARAMETERS</span></span>

### <span data-ttu-id="5e568-111">-Instanz</span><span class="sxs-lookup"><span data-stu-id="5e568-111">-Instance</span></span>

<span data-ttu-id="5e568-112">Name der Analysis Services-Serverinstanz, die neu gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="5e568-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="5e568-113">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="5e568-113">-Database</span></span>

<span data-ttu-id="5e568-114">Identität der zu synchronisierenden Datenbank</span><span class="sxs-lookup"><span data-stu-id="5e568-114">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="5e568-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e568-115">-PassThru</span></span>

<span data-ttu-id="5e568-116">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5e568-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="5e568-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e568-117">INPUTS</span></span>

### <span data-ttu-id="5e568-118">Keine</span><span class="sxs-lookup"><span data-stu-id="5e568-118">None</span></span>
<span data-ttu-id="5e568-119">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5e568-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e568-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e568-120">OUTPUTS</span></span>

### <span data-ttu-id="5e568-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e568-121">System.Boolean</span></span>

## <span data-ttu-id="5e568-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e568-122">NOTES</span></span>

<span data-ttu-id="5e568-123">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="5e568-123">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="5e568-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e568-124">RELATED LINKS</span></span>
