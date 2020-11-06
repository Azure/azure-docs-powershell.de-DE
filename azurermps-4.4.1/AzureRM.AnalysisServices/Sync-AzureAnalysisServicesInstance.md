---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: a75ae79722fed99ce96b0a082f4f56ace998354e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479402"
---
# <span data-ttu-id="b784f-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="b784f-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="b784f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b784f-102">SYNOPSIS</span></span>
<span data-ttu-id="b784f-103">Synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrage dezentralen Instanzen in der aktuell angemeldeten Umgebung, wie in Add-AzureAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="b784f-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b784f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b784f-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b784f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b784f-105">DESCRIPTION</span></span>
<span data-ttu-id="b784f-106">Das Sync-AzureAnalysisServicesInstance-Cmdlet synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrage-dezentralen Instanzen in der aktuell angemeldeten Umgebung, wie in Add-AzureAnalysisServicesAccount Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="b784f-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="b784f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b784f-107">EXAMPLES</span></span>

### <span data-ttu-id="b784f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b784f-108">Example 1</span></span>
```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="b784f-109">Dieser Befehl synchronisiert die Datenbank mit dem Namen "SalesOrders" auf dem Server "Contoso" im Umgebungs westus.asazure.Windows.net, vorausgesetzt, der Benutzer hat sich mit Add-AzureAnalysisServicesAccount Befehl bei dieser Umgebung angemeldet.</span><span class="sxs-lookup"><span data-stu-id="b784f-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="b784f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b784f-110">PARAMETERS</span></span>

### <span data-ttu-id="b784f-111">-Instanz</span><span class="sxs-lookup"><span data-stu-id="b784f-111">-Instance</span></span>
<span data-ttu-id="b784f-112">Name der Analysis Services-Serverinstanz, die neu gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="b784f-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="b784f-113">-Datenbank</span><span class="sxs-lookup"><span data-stu-id="b784f-113">-Database</span></span>
<span data-ttu-id="b784f-114">Identität der zu synchronisierenden Datenbank</span><span class="sxs-lookup"><span data-stu-id="b784f-114">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="b784f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b784f-115">-PassThru</span></span>
<span data-ttu-id="b784f-116">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b784f-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b784f-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b784f-117">-Confirm</span></span>
<span data-ttu-id="b784f-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b784f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b784f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b784f-119">-WhatIf</span></span>
<span data-ttu-id="b784f-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b784f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b784f-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b784f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b784f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b784f-122">CommonParameters</span></span>
<span data-ttu-id="b784f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b784f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b784f-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b784f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b784f-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b784f-125">INPUTS</span></span>

## <span data-ttu-id="b784f-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b784f-126">OUTPUTS</span></span>

### <span data-ttu-id="b784f-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b784f-127">System.Boolean</span></span>

## <span data-ttu-id="b784f-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="b784f-128">NOTES</span></span>
<span data-ttu-id="b784f-129">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="b784f-129">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="b784f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b784f-130">RELATED LINKS</span></span>

